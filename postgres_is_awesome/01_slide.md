!SLIDE

# Postgres is Awesome #

!SLIDE bullets incremental

# Why PostgreSQL?

* Incredibly stable
* Best OSS SQL database there is
* NoSQL solutions specialized and immature
* No corporate owner
* Conclusion: Awesome

!SLIDE

# Durability & Replication

* WAL shipping
* Streaming replication
* Sync-rep

!SLIDE bullets

# Write-Ahead Logs

* journalled heap
* writes first to one disk
* consolidated to heap

!SLIDE bullets

# Write-Ahead Logs

* WAL contains all changes to disk
* used for disaster recovery
* why not use it every day?

!SLIDE bullets

# Write-Ahead Logs

* ship logs to highly durable data store
* consolidate daily via new base backups
* create new databases by cloning that

!SLIDE bullets incremental

# Streaming Replication

* guaranteed accurate replication?
* follow, then fork
* minimum down-time migrations

# Fork? Follow?

* if provisioning is fast and easy
* and databases come in many sizes
* why not create a massive server for an hour?
