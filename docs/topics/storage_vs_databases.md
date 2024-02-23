# Storage vs Databases

## Introduction

this does not discuss exactly what a database is, but instead compares with file storage.   If you want to keep your files around, you need to store is somewhere.  We don't usually lump databases in the same category as file storage, but in many ways it has the same function for research data: a way to keep data around between bouts of analysis.   

## Definitions

**Storage** refers to the persistent retention of data in a computer system (local or cloud). Storage devices and media provide capacity to save and retrieve data as needed.  Common examples of storage include hard drives, SSDs, optical discs, and flash drives.  For these, the operating system of the computer handles the retrieval.   Examples of cloud storage (see below) or a shared storage system, there is a server computer and operating system that manages the storage and allows you to connect remotely.   If you want to work with data from a file in storage, traditionally that file must be loaded into memory and the your program manipulates the data inside`*`.  

Databases are structured sets of data that are optimized for querying, analyzing, and manipulating data. Databases include software functionality like querying languages, access control, transactions, and analytics capabilities that storage devices lack. SQL and NoSQL are common database approaches.  Databases typically require a remote server that has special software just for organizing, storing, analyzing and retreiving data for you.   The computer program accessing the database server is a client, and does very little processing.   If you want to work with data in a database server, you send the command describing the data you want, and the database server returns just that data.  A database server can also calculate sorting , calculate transformations (math), and summaries (counts, averages, etc).    You don't need to load the whole 'table' as you may have to for a CSV file.  

`*` There are exceptions to this of course, new data storage libraries and file formats like Apache Arrow that allow you to load only part of file, OR in-memory database libraries that let you treat local files like databases.  

## Comparison

| **Storage** | **Database** |
|---|---|
|Storage provides raw data capacity|structured for efficient querying and analysis|
| Storage systems see data as an opaque blob or block. The storage system has no visibility into the contents or structure of data. | **Databases** impose structure on data through schemas and modeling. This enables efficient querying and enforcing integrity constraints |
|Storage is accessed through raw read/write operations to locations like blocks or files by the operating system |Databases allow declarative access through query languages like SQL as well as APIs. the physical location is hidden from the user as the database server manages efficient disk access automatically |
|Durable very long-term persistence/retention for data files that may be infrequently accessed.| fast and frequent data accessed by record(row) (though database systems can live for decades) |
| A file can be opened by one process at a time | can read/write different rows to thousands of clients, but a process can 'lock' a row for writing to it to avoid contention | 
| good for direct binary file access (images, videos, documents) | good for Multi-user applications and for managing transactions (all data operations must complete before committing) |

## Summary

Storage and databases both persist data but are optimized for different purposes. Storage provides durable capacity while databases structure data for efficient access. Storage suits long-term file retention while databases enable interactive applications. Both remain essential components of a complete data architecture.

**Stolen and adapted from the ad-laden website [DatabaseTown](https://databasetown.com/storage-vs-database-a-comparative-analysis/)
