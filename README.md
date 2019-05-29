## Note
If you have create all foreign keys, importing will result in error.

To add data after creating all foreign keys:
* Drop the foreign key constraint of the `DEPARTMENT` table.
```sql
ALTER TABLE DEPARTMENT DROP CONSTRAINT department_fk_eid;
```
* Import data for the `DEPARTMENT` table and the `EMPLOYEE` table.
* Recreate the foreign key of the `DEPARTMENT` table.
```sql
ALTER TABLE DEPARTMENT
    ADD CONSTRAINT department_fk_eid
        FOREIGN KEY(EID) REFERENCES EMPLOYEE(EID);
```
* Import data for the remaining tables.

## Add data to a table
* Step 1: Click on the table on the left panel.
![screenshot](https://github.com/wecandoit-182/data/blob/master/screenshot/Step01.JPG)
* Step 2: Click on `Actions... -> Import Data`.
![screenshot](https://github.com/wecandoit-182/data/blob/master/screenshot/Step02.jpg)
* Step 3: Click on `Browse` and choose the `.csv` file.
![screenshot](https://github.com/wecandoit-182/data/blob/master/screenshot/Step03.jpg)
* Step 4: Click on `Next` until the end and click `Finish`.