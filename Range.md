---
title: Range Clauses
---

Spec: https://go.dev/ref/spec#For_statements

## Summary

A range clause provides a way to iterate over an array, slice, string, map, channel, integer, or function.

## Example

```go
for k, v := range myMap {
	log.Printf("key=%v, value=%v", k, v)
}

for v := range myChannel {
	log.Printf("value=%v", v)
}

for i, v := range myArray {
	log.Printf("array value at [%d]=%v", i, v)
}

// Range over integer (Go 1.23+)
for i := range myInteger {
	log.Printf("i=%d", i) // 0, 1, ..., myInteger-1
}

// Range over function (Go 1.23+)
for k, v := range myIter {
	log.Printf("key=%v, value=%v", k, v)
}
```

## Reference

If only one value is used on the left of a range expression, it is the 1st value in this table.

| Range expression                             | 1st value      | 2nd value (optional) | notes                                                                    |
| :------------------------------------------- | :------------- | :------------------- | :----------------------------------------------------------------------- |
| array or slice a `[n]E`, `*[n]E`, or `[]E`   | index `i  int` | `a[i]` E             |                                                                          |
| string s string type                         | index `i  int` | rune `int`           | range iterates over Unicode code points, not bytes                       |
| map m `map[K]V`                              | key `k  K`     | value `m[k]` V       |                                                                          |
| channel c `chan E`, `<-chan E`               | element `e  E` | _none_               |                                                                          |
| integer value n integer type, or untyped int | value `i  T`   | _none_               | `T` is the type of `n`. If n <= 0, the loop does not run any iterations. |
| function, 0 values f `func(func() bool)`     | _none_         | _none_               |                                                                          |
| function, 1 value f `func(func(V) bool)`     | value `v  V`   | _none_               |                                                                          |
| function, 2 values f `func(func(K, V) bool)` | key `k  K`     | value `v  V`         |                                                                          |

## Gotchas

When iterating over a slice or map of values, one might try this:

```go
items := make([]map[int]int, 10)
for _, item := range items {
	item = make(map[int]int, 1) // Oops! item is only a copy of the slice element.
	item[1] = 2                 // This 'item' will be lost on the next iteration.
}
```

The `make` and assignment look like they might work, but the value property of `range` (stored here as `item`) is a _copy_ of the value from `items`, not a pointer to the value in `items`. The following will work:

```go
items := make([]map[int]int, 10)
for i := range items {
	items[i] = make(map[int]int, 1)
	items[i][1] = 2
}
```
