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