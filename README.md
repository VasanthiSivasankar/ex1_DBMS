### DDL-COMMANDS
## AIM
To study and implement DDL commands and different types of constraints.
## THEORY
```
1.CREATE:
This is used to create a new relation (table)
Syntax:
CREATETABLE(field_1 data_type(size),field_2 data_type(size), .. . );
2.ALTER:
This is used to add some extra fields into existing relation.
Syntax:
ALTERTABLErelation_name ADD(new field_1 data_type(size) );
(a)ALTERTABLE...ADD...:
ALTERTABLEstdADD(AddressCHAR(10));
(b )ALTERTABLE...MODIFY...:
ALTERTABLErelation_nameMODIFY(field_1 newdata_type(Size)
( c) ALTERTABLE..DROP....
ALTERTABLErelation_nameDROPCOLUMN(field_name);
(d)ALTERTABLE..RENAME...:
ALTERTABLErelation_name RENAMECOLUMN(OLDfield_name) to(NEW field_name);
3.DROP TABLE:
This is used to delete the structure of a relation. It permanently deletes the records in the table.
Syntax:
DROPTABLErelation_name;
4.RENAME:
It is used to modify the name of the existing database object.
Syntax:
RENAMETABLEold_relation_nameTOnew_relation_name;
CONSTRAINTS:
Constraints are used to specify rules for the data in a table. If there is any violation between the
constraint and the data action, the action is aborted by the constraint. It can be specified when the table is
created (using CREATE TABLE statement) or after the table is created (using ALTER TABLE statement).

1.NOT NULL: When a column is defined as NOTNULL, then that column becomes a mandatory
column. It implies that a value must be entered into the column if the record is to be accepted for storage in
the table.
Syntax:
CREATETABLETable_Name(column_namedata_type (size) NOT NULL, );
2.UNIQUE: The purpose of a unique key is to ensure that information in the column(s) is unique
i.e. a value entered in column(s) defined in the unique constraint must not be repeated across the column(s).
Atable may have many unique keys.
Syntax:
CREATETABLETable_Name(column_namedata_type(size)UNIQUE,….);
3.CHECK:Specifies a condition that each row in the table must satisfy. To satisfy the constraint, each
row in the table must make the condition either TRUE or unknown (due to a null).
Syntax:
CREATE TABLE Table_Name(column_name data_type(size) CHECK(logical
expression), ….);
4.PRIMARY KEY: A field which is used to identify a record uniquely. A column or combination
of columns can be created as primary key, which can be used as a reference from other tables. A table
contains primary key is known as Master Table.

● Itmust uniquely identify each record in a table.
● Itmust contain unique values.
● Itcannot be a null field.
● Itcannot be a multi port field.
● Itshould contain a minimum number of fields necessary to be called unique.
Syntax:
CREATETABLE Table_Name(column_name data_type(size) PRIMARY KEY, ….);
5.FOREIGN KEY: It is a table level constraint. We cannot add this at column level. To reference any
primary key column from other table this constraint can be used. The table in which the foreign key is
defined is called a detail table. The table that defines the primary key and is referenced by the foreign key
is called the master table.
Syntax:
CREATE TABLETable_Name(column_namedata_type(size)FOREIGN KEY(column_name)
REFERENCEStable_name);
6.DEFAULT : The DEFAULT constraint is used to insert a default value into a column. The
default value will be added to all new records, if no other value is specified.
Syntax:
CREATETABLE Table_Name(col_name1,col_name2,col_name3 DEFAULT ‘’);
```
