---
# This basic template provides core metadata fields for Markdown articles on docs.superoffice.com.

# Mandatory fields.
title: mirroring_sql_server_schema       # (Required) Very important for SEO. Intent in a unique string of 43-59 chars including spaces.
description: SQL Server schema for database mirroring # (Required) Important for SEO. Recommended character length is 115-145 characters including spaces.
author: {github-id}             # Your GitHub alias.
keywords: 
so.topic: concept           # article, howto, reference, concept, guide

# Optional fields. Don't forget to remove # if you need a field.
so.envir: cloud           # cloud or onsite
so.client: online               # online, web, win, pocket, or mobile
---

# SQL Server schema for database mirroring

Microsoft SQL Server physical schemas are used on both the SuperOffice CRM Online and partner ends. This makes the mirroring independent of various functional complexities, such as dictionaries (CRM, CS extra tables).

All tables **except** a blacklist will be [mirrored][1]. This is (at least initially) a fixed set. Because the physical schema is used, we don't distinguish between *dictionary* and *normal* tables. There is also no distinction between tables belonging to Sales, Service, extra-tables in Service, or any partner-defined tables that might appear in the future.

Mirroring uses a **simplified table schema**. This means that foreign key constraints, collating sequences, and indexes are **not mirrored**.

> [!NOTE]
> We don't support row- or column-level filtering: tables are either mirrored or not.

## Default schema

The schema/prefix is not mirrored. The mirror always uses the default schema. The connection string/login user can be used to influence the default schema.

## Metadata

The client must maintain 1 table in the target database for required metadata  The `<context identifier>_mirroring` table is automatically created the first time the mirroring task runs. For example, `Cust10195_mirroring`. For each named table, the client must store a schema hash and the Log Sequence Number.

## Database index

If you need database indexes, you should create and maintain them before or after each replication cycle.

In the NuGet implementation, you can do this in one of the event-handling methods in IMirrorAdmin:

* In `OnBeforeReplicateTable`, which is called once for each table in each mirroring cycle
* In `OnReplicationCompleted`, which is called once at the end of a complete cycle

## Blacklisted tables

Database tables that fall into one of the [following categories are not mirrored][2]:

* irrelevant (`travelgeneratedtransaction`)
* not useful (`traveltransactionlog`, `countervalue`)
* confidential (`credentials`)

## When mirroring schema changes fails

This might happen if a customer creates an extra table containing a character field through SuperOffice Service.

1. A [mirroring cycle][3] is run and the table is created and populated in the mirror.
2. Later, the customer drops the table, and re-creates it with the same name… and this time adds a DateTime field with the same name as the old character field. Farfetched, but possible.
3. The mirroring system will only see that the schema has changed with one column changing the data type. **This change will fail!**
4. The client code supplied by SuperOffice will react by dropping the table in the mirror database, creating it with the new schema, and request a full repopulation.

<!-- Referenced links -->
[1]: index.md
[2]: https://community.superoffice.com/contentassets/8c09bc95f03841cd87771bc367849cf5/mirroredtables.docx
[3]: mirroring-task.md