

## Functional Capabilities of the System

1. **Adding a Database**  
   The ability to add a new database to the system by specifying all necessary connection parameters.

2. **Establishing a Database Connection**  
   The system must ensure the establishment of a connection to the selected database and verify its availability.

3. **Testing Database Connection**  
   The ability to test the connection to the database to ensure the correctness of connection parameters and the availability of the DBMS.

4. **Backup Management**
    1. **Selecting Backup Type**:  
       The user can choose between a full, incremental, or differential backup depending on their preferences and the database type.
    2. **Automatic Backup Execution**:  
       The system must support the configuration of automatic backup execution at specified time intervals.

5. **Restoring Backups**
    1. **Restoring the Entire Database**:  
       The ability to restore all data from a backup.
    2. **Restoring Specific Parts of the Database**:  
       If supported by the DBMS, the system must provide the ability to restore individual tables or collections from backups.

6. **Data Storage**
    1. **Storing Database Information**:  
       The system must support storing information about connected databases, such as connection parameters, database name, and other metadata.
    2. **Storing Backups in Compressed Format**:  
       All backups must be stored in a compressed format to save disk space.

7. **Operation Logging**  
   The system must log all backup operations, including execution time, backup type, and any errors that occurred during the process. This is necessary for analysis and troubleshooting potential issues in the future.
