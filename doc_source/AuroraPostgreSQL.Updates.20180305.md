# Amazon Aurora PostgreSQL Database Engine Updates 2018\-03\-05<a name="AuroraPostgreSQL.Updates.20180305"></a>

The following updates are available for Aurora PostgreSQL\.

## Version 1\.0\.11<a name="AuroraPostgreSQL.Updates.20180305.1011"></a>

You can find the following improvements in this engine update:

+ Fixes an issue with parallel query execution that can lead to incorrect results\.

+ Fixes an issue with visibility map handling during replication from Amazon RDS for PostgreSQL that can cause the Aurora storage volume to become unavailable\. 

+ Corrects the pg\-repack extension\.

+ Implements improvements to maintain fresh nodes\.

+ Fixes issues that can lead to an engine crash\.

## Version 1\.0\.10<a name="AuroraPostgreSQL.Updates.20180305.1010"></a>

This update includes a new feature\. You can now replicate an Amazon RDS PostgreSQL DB instance to Aurora PostgreSQL\. For more information, see [Replication with Amazon Aurora PostgreSQL](AuroraPostgreSQL.Replication.md)\.

You can find the following improvements in this engine update:

+ Adds error logging when a cache exists and a parameter change results in a mismatched buffer cache, storage format, or size\.

+ Fixes an issue that causes an engine reboot if there is an incompatible parameter value for huge pages\. 

+ Improves handling of multiple truncate table statements during a replay of a write ahead log \(WAL\) on a read node\.

+ Reduces static memory overhead to reduce out\-of\-memory errors\.

+ Fixes an issue that can lead to out\-of\-memory errors while performing an insert with a GiST index\.

+ Improves snapshot import from RDS PostgreSQL, removing the requirement that a vacuum be performed on uninitialized pages\.

+ Fixes an issue that causes prepared transactions to return to the previous state following an engine crash\.

+ Implements improvements to prevent read nodes from becoming stale\.

+ Implements improvements to reduce downtime with an engine restart\.

+ Fixes issues that can cause an engine crash\.

## Version 1\.0\.9<a name="AuroraPostgreSQL.Updates.20180305.109"></a>

In this engine update, we fix an issue that can cause the Aurora storage volume to become unavailable when importing a snapshot from RDS PostgreSQL that contained uninitialized pages\.

## Version 1\.0\.8<a name="AuroraPostgreSQL.Updates.20180305.108"></a>

You can find the following improvements in this engine update:

+ Fixes an issue that prevented the engine from starting if the `shared_preload_libraries` instance parameter contained `pg_hint_plan`\. 

+ Fixes the error "Attempt to fetch heap block XXX is beyond end of heap \(YYY blocks\)," which can occur during parallel scans\. 

+ Improves the effectiveness of prefetching on reads for a vacuum\.

+ Fixes issues with snapshot import from RDS PostgreSQL, which can fail if there are incompatible pg\_internal\.init files in the source snapshot\.

+ Fixes an issue that can cause a read node to crash with the message "aurora wal replay process \(PID XXX\) was terminated by signal 11: Segmentation fault"\. This issue occurs when the reader applied a visibility map change for an uncached visibility map page\.

## Version 1\.0\.7<a name="AuroraPostgreSQL.Updates.20180305.107"></a>

This is the first generally available release of Amazon Aurora with PostgreSQL compatibility\.