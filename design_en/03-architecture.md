

## Architecture

### 🧩 Module 1: DatabaseConnector
**Description**:  
Responsible for establishing and verifying connections to various DBMS.

**Functions**:
1. Establishing a connection to the database using the given parameters (host, port, database, user, password).
2. Verifying the database's availability — testing the connection before adding the database to the system.
3. Encapsulating the connection logic — supporting various DBMS (PostgreSQL, MySQL, MongoDB, etc.).

---

### 🧩 Module 2: DatabaseManager
**Description**:  
Responsible for managing databases within the system: registration, connection, creation, and backup handling. Essentially, it acts as the brain that manages database operations.

**Functions**:
1. Registering a database.
2. Configuring backup settings — allowing the choice between full, incremental, or differential backups for each database.
3. Creating backups.
4. Transferring data into the DB — accepting unpacked data and inserting it into the relevant database.

---

### 🧩 Module 3: BackupStorage
**Description**:  
Responsible for storing, retrieving, and deleting backup files.

**Functions**:
1. Saving a backup (backup file or stream, along with metadata).
2. Retrieving a backup.
3. Deleting backup files.

---

### 🧩 Module 4: Compression
**Description**:  
Responsible for compressing and decompressing backup files. It encapsulates the logic for working with various compression algorithms (e.g., ZIP, GZIP, etc.).

**Functions**:
1. Compressing data.
2. Decompressing data.

---

### 🧩 Module 5: RecoveryManager
**Description**:  
Responsible for restoring data from previously created backups — both fully and selectively (by parts). It manages the full cycle, from retrieving the necessary file to transferring the data back to the database. (In fact, this module merely initiates the restoration; the actual recovery is handled by another component.)

**Functions**:
1. Full data restoration.
2. Partial data restoration (if the backup is structured).

**Additional Features**:
* If the backup is structured, RecoveryManager can offer the user:
    * A list of available items for restoration.
    * An option to choose: "Restore everything" or "Select parts."

---

### 🧩 Module 6: BackupScheduler
**Description**:  
Responsible for automatically triggering backup tasks according to a predefined schedule. It can operate based on a timer, cron expressions, or other scheduling strategies.

**Functions**:
1. Scheduling tasks — configuring schedules (time, days of the week, intervals, etc.).
2. Triggering backups — automatically calling DatabaseManager to create a backup for the specified database.
3. Managing schedules — modifying, deleting, pausing, and activating scheduled tasks.

---

### 🧩 Module 7: Logging
**Description**:  
This module manages the logging of all system operations and events. It provides a unified interface for logging at various levels (info, warn, error) and supports configuring log format and storage location.

**Functions**:
1. Writing logs.
2. Log rotation and storage.
