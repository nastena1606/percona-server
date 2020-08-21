.. _PS-8.0.NEXT:

================================================================================
*Percona Server for MySQL* 8.0.NEXT
================================================================================

:Date: September 9, 2020
:Installation: `Installing Percona Server for MySQL <https://www.percona.com/doc/percona-server/8.0/installation.html>`_

`Percona Server for MySQL <https://www.percona.com/software/mysql-database/percona-server>`_ 8.0.NEXT
includes all the features and bug fixes available in
`MySQL 8.0.NEXT Community Edition <https://dev.mysql.com/doc/relnotes/mysql/8.0/en/news-8-0-NEXT.html>`_
in addition to enterprise-grade features developed by Percona.

Improvements
================================================================================

* :jirabug:`PS-7132`: Make default value of rocksdb_wal_recovery_mode compatible with InnoDB
* :jirabug:`PS-5730`: Change SELECT rotate_system_key to ALTER INSTANCE for percona system key rotation.
* :jirabug:`PS-7199`: Document Coredumper functionality
* :jirabug:`PS-7114`: Enhance crash artifacts (core dumps and stack traces) to provide additional information to the operator
* :jirabug:`PS-5635`: Introduce crypt_schema 2 for better error checking in encryption threads.
* :jirabug:`PS-7245`: block enable/disable redo log with lock tables for backup



Bugs Fixed
================================================================================

* :jirabug:`PS-7203`: Modify open_tables to skip the test triggered if the thread originating it is a SQL thread or any replication thread (in the case of Multi thread replication)
* :jirabug:`PS-6067`: Provide a fix for upstream bug #97001 in Percona Server (Upstream :mysqlbug:`97001`)
* :jirabug:`PS-7221`: Modify get_int_sort_key_for_item_inline to return UTC string (Upstream :mysqlbug:`100402`)
* :jirabug:`PS-7076`: Modify to not update Cardinality after setting tokudb_cardinality_scale_percent
* :jirabug:`PS-7025`: Fix reading ahead of insert buffer pages by dispatching of buffered AIO transfers (Upstream :mysqlbug:`100086`)
* :jirabug:`PS-7010`: Modify to Lock buffer blocks before sanity check in btr_cur_latch_leaves
* :jirabug:`PS-6995`: Introduce a new optimizer switch to allow the user to reduce the cost of a range scan to determine best execution plan for Primary Key lookup
* :jirabug:`PS-7220`: Fix activity counter update in purge coordinator and workers
* :jirabug:`PS-7169`: Set rocksdb_validate_tables to disabled RocksDB while upgrading the server from 5.7 to 8.0.20
* :jirabug:`PS-5741`: Incorrect use of memset_s in keyring_vault
* :jirabug:`PS-5323`: Align Keyring encryption with Master Key encryption
* :jirabug:`PS-7234`: Modify PS minimal tarballs to remove COPYING.AGPLv3
* :jirabug:`PS-7140`: crypt redo logs are not applied correctly
* :jirabug:`PS-7120`: Handle doublewrite buffer encryption for keyring key tablespaces
* :jirabug:`PS-7119`: Tests encryption.innodb_encryption_aborted_rotation* sometime fail.
* :jirabug:`PS-6987`: encryption threads report space unencrypted while there are some pages still encrypted in it.
* :jirabug:`CUSTOM-54`: PS-6990-Server doesn't restart after crash when there are too many gaps in the mysql.gtid_executed table.
* :jirabug:`PS-7143`: ACL Cache Lock waits in PS 8.0.18


