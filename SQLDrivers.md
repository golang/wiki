---
title: SQL Database Drivers
---

The database/sql and database/sql/driver packages are designed for using databases from Go and implementing database drivers, respectively.

See the design goals doc:

> http://golang.org/src/pkg/database/sql/doc.txt

## Drivers

Drivers for Go's sql package include:

  * **Amazon AWS Athena**: https://github.com/uber/athenadriver
  * **AWS Athena**: https://github.com/segmentio/go-athena
  * **AWS DynamoDB**: https://github.com/btnguyen2k/godynamo
  * **Apache Avatica/Phoenix**: https://github.com/apache/calcite-avatica-go
  * **Apache H2**: https://github.com/jmrobles/h2go
  * **Apache Hive**: https://github.com/sql-machine-learning/gohive
  * **Apache Ignite/GridGain**: https://github.com/amsokol/ignite-go-client
  * **Apache Impala**: https://github.com/bippio/go-impala
  * **Azure Cosmos DB**: https://github.com/btnguyen2k/gocosmos
  * **ClickHouse** (uses [HTTP API](https://clickhouse.tech/docs/en/interfaces/http/)): https://github.com/mailru/go-clickhouse
  * **ClickHouse** (uses [native TCP interface](https://clickhouse.tech/docs/en/interfaces/tcp/)): https://github.com/ClickHouse/clickhouse-go
  * **CockroachDB**: Use any PostgreSQL driver
  * **Couchbase N1QL**: https://github.com/couchbase/go_n1ql
  * **DB2 LUW** (uses cgo): https://github.com/asifjalil/cli
  * **DB2 LUW** and **DB2/Z with DB2-Connect**: https://bitbucket.org/phiggins/db2cli (Last updated 2015-08)
  * **DB2 LUW, z/OS, iSeries and Informix**: https://github.com/ibmdb/go_ibm_db
  * **Databricks**: https://github.com/databricks/databricks-sql-go
  * **DuckDB**: https://github.com/marcboeker/go-duckdb
  * **Exasol**: (pure Go): https://github.com/exasol/exasol-driver-go
  * **Firebird SQL**: https://github.com/nakagami/firebirdsql
  * **Genji** (pure go): https://github.com/genjidb/genji
  * **Google Cloud BigQuery**: https://github.com/solcates/go-sql-bigquery
  * **Google Cloud Spanner**: https://github.com/googleapis/go-sql-spanner
  * **Google Cloud Spanner**: https://github.com/rakyll/go-sql-driver-spanner
  * **MS ADODB**: https://github.com/mattn/go-adodb
  * **MS SQL Server** (pure go): https://github.com/microsoft/go-mssqldb
  * **MS SQL Server** (uses cgo): https://github.com/minus5/gofreetds
  * **MaxCompute**: https://github.com/sql-machine-learning/gomaxcompute
  * **MySQL**: https://github.com/go-sql-driver/mysql/ ` [*] `
  * **MySQL**: https://github.com/siddontang/go-mysql/ ` [**] ` (also handles replication)
  * **MySQL**: https://github.com/ziutek/mymysql ` [*] `
  * **ODBC**: https://bitbucket.org/miquella/mgodbc (Last updated 2016-02)
  * **ODBC**: https://github.com/alexbrainman/odbc
  * **Oracle** (pure go): https://github.com/sijms/go-ora
  * **Oracle** (uses cgo): https://github.com/godror/godror
  * **Oracle** (uses cgo): https://github.com/mattn/go-oci8
  * **Oracle** (uses cgo): https://gopkg.in/rana/ora.v4
  * **Postgres** (pure Go): https://github.com/jackc/pgx ` [*] `
  * **Postgres** (pure Go): https://github.com/lib/pq ` [*] `
  * **Postgres** (uses cgo): https://github.com/jbarham/gopgsqldriver
  * **Presto**: https://github.com/prestodb/presto-go-client
  * **QL**: https://pkg.go.dev/modernc.org/ql
  * **SAP ASE** (pure go): https://github.com/SAP/go-ase
  * **SAP ASE** (uses cgo): https://github.com/SAP/cgo-ase
  * **SAP HANA** (pure go): https://github.com/SAP/go-hdb
  * **SAP HANA** (uses cgo): https://help.sap.com/viewer/0eec0d68141541d1b07893a39944924e/2.0.03/en-US/0ffbe86c9d9f44338441829c6bee15e6.html
  * **SQL over REST**: https://github.com/adaptant-labs/go-sql-rest-driver
  * **SQLite** (uses cgo): https://github.com/gwenn/gosqlite - Supports SQLite dynamic data typing
  * **SQLite** (uses cgo): https://github.com/mattn/go-sqlite3 ` [*] `
  * **SQLite** (uses cgo): https://github.com/mxk/go-sqlite
  * **SQLite**: (pure go): https://modernc.org/sqlite
  * **SQLite**: (pure go): https://github.com/ncruces/go-sqlite3
  * **SQLite**: (uses cgo): https://github.com/rsc/sqlite
  * **SingleStore**: Use any MySQL driver
  * **Snowflake** (pure Go): https://github.com/snowflakedb/gosnowflake
  * **Sybase ASE** (pure go): https://github.com/thda/tds
  * **Sybase SQL Anywhere**: https://github.com/a-palchikov/sqlago
  * **TiDB**: Use any MySQL driver
  * **Trino**: https://github.com/trinodb/trino-go-client
  * **Vertica**: https://github.com/vertica/vertica-sql-go
  * **Vitess**: https://pkg.go.dev/vitess.io/vitess/go/vt/vitessdriver
  * **YDB** (pure go): https://github.com/ydb-platform/ydb-go-sdk
  * **YQL (Yahoo! Query Language)**: https://github.com/mattn/go-yql

Drivers marked with ` [*] ` are both included in and pass the compatibility test suite at https://github.com/bradfitz/go-sql-test.
Drivers marked with ` [**] ` pass the compatibility test suite but are not currently included in it.

