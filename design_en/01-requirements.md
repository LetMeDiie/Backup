

## System Requirements

1. **Database Connection and Testing**  
   The system must allow connections to multiple types of databases and verify the success of the connection.

2. **Supported Database Types**  
   The system must support the following database types:
    - PostgreSQL
    - MySQL
    - MongoDB
    - SQLite

3. **Database Connection Parameters**  
   The following parameters must be specified for connecting to a database:
    - Host (hostname)
    - Port (port)
    - Database name
    - Username
    - Password

4. **Backup Types**  
   The system must support three types of backups depending on the user’s preferences and the type of database:
    - Full backup
    - Incremental backup
    - Differential backup

5. **Backup Compression**  
   To save disk space, the system must support compression of backup files.

6. **Local Storage**  
   The system must allow users to store backups locally on their devices.

7. **Selective Restoration**  
   The system must support selective restoration of data: restoring individual tables or collections, if supported by the respective DBMS.

8. **Backup Operation Logging**  
   The system must maintain a log of all backup operations to ensure traceability and data security.
