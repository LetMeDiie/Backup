

# Backup (EN)

## System Description

It is necessary to create a system for **automatic database backup** of any type. The system will support various **database management systems (DBMS)** such as:
- **MySQL**
- **PostgreSQL**
- **MongoDB**
- **SQLite**
- and others.

The system will include:

- **Automatic backup scheduling** — for performing backups on a set schedule.
- **Backup file compression** — to save disk space.
- **Storage options** — both **local** and **cloud**.
- **Backup operation logging** — for tracking all actions related to backups.

The client will be able to:

- Add new databases to the system.
- Manage the backup process.

## System Design
The system design is located in the `design_en` folder.





--------------------------------------------------------------------------------------------------------------------------------------------




# Backup (RU)

## Описание системы

Необходимо создать систему для **автоматического резервного копирования** любого типа базы данных. Система будет поддерживать различные **системы управления базами данных (СУБД)**, такие как:
- **MySQL**
- **PostgreSQL**
- **MongoDB**
- **SQLite**
- и другие.

Система будет включать:

- **Автоматическое планирование резервного копирования** — для выполнения копирования по расписанию.
- **Сжатие файлов** резервных копий — для экономии места на диске.
- **Параметры хранения** — как **локальные**, так и **облачные**.
- **Ведение журнала операций** — для отслеживания всех действий, связанных с резервным копированием.

Клиенту будет предоставлена возможность:

- Добавлять новые базы данных в систему.
- Управлять процессом резервного копирования.

## Проектирование системы
Проектирование системы находится в папке `design_ru`.
