## Note
If you have create all foreign keys, importing will result in error.

To add data after creating all foreign keys:
* Drop the foreign key of the `DEPARTMENT` table.
* Import data for the `DEPARTMENT` table and the `EMPLOYEE` table.
* Recreate the foreign key of the `DEPARTMENT` table.
* Import data for the remaining tables.