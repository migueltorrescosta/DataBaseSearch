# DataBaseSearch
Graphic Tool for Visualizing DataBase Storage

# TODO

- [ ] Do daily checks to ensure that all contact emails are still valid (i.e. we don't get orphaned contacts)

# Structure of the DataBases

This tool is meant to connect data across a large corporation, making it easier to connect the dots. This is done by reading four local tables:

### Table / Column Information

**Kept as:** csv

This table has columns
- table_name : The name of the table
- column_name : The name of the column in the table
- column_short_description : The name used to describe the column ( if different column_names are used in different tables for the same information, then both columns must have the same short_description ).

### Table Description

**Kept as:** Markdown files, one per table_name

This table contains
- table_name: the name of the table
- owner: The team responsible for mantaining this table
- table_description: A summary of why this table exists ad the business need it is satisfying.

### Owner Description

**Kept as:** Markdown files, one per owner

This table contains :
- owner: the name of the team.
- contact: email used to reach out to this team.
- role: The purpose of the team inside the company

### Column Informaton

**Kept as:** Markdown files, one file per column_short_description

- column_short_description:
- ground_truth_table: The table that contains the "ground truth" of this table. If different tables with this information disagree on the information contain, the ground_truth_table should be taken as the valid value.
- column_technical_description: A description of how this table's value is computed. It might vary from "imported as is from an external vender" to formulae 