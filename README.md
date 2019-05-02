The created database serves a company in the telecom industry. It enables the management of
branches, clients, employees, their positions, salaries and its taxations, managers of particular
branches, stocks (phones that are to be sold in a particular branch), information about the phone
producers and their country.
The entities and relationships between them are the following:

1) Phones - Stocks - Branch, N:N relation. The primary key in the Phones table represents
its ID. Moreover, the table includes the names of particular phone models. The primary key in
the Branch table is the ID of the respective Branch. In both tables the primary keys enable the
diversification of each item (phone model and branch), which is unique. As these tables are
related to the Stocks table where pieces of particular models in distinct branches are shown,
model_of_phone and branch_of_stock are the foreign key in the Stock table - each
model_of_the phone and branch_of _stock can be repeated in the table more than once.

2) Branch – Employees – Position, N:N relation. The table Employees has two foreign keys:
the branch of each employee (branch_emp) and the position of the employees
(position_of_empl), which connect this table with two other tables: Branch and Position. ID is
a primary key in both the Branch table and Position table as a unique value. This relationship
enables to connect employees with the branch they work in and their position. There can be
multiple employees on the same position within the same branch.

3) Managers - Branch, 1:1 relation. Each manager is responsible for one branch. For that
reason, branch_ of_manager is a primary and foreign key at the same time, which is connected
with the Branch table through the ID of the branch.

4) Salary – Position, 1:1 relation. Depending on the position in the company the salary varies.
Therefore, each position is connected with one amount. The ID in the Salary table is a primary
key and the salary_for_the_position in the position table is a foreign key.

5) Clients – Branch, N:1 relation. Each Client is assigned to a particular branch (e.g. they
signed the contract in this branch). The ID of the Branch table (primary key) is connected with
branch_of_the client column, which serves as a foreign key as many clients are assigned to the
same branch.

6) Size_of_branch – Branch, 1:N relation. The area of each branch can be defined as either
very small, small, medium, big or very big. Each size has its own ID, which is the primary key,
but the area in the branch table represents its foreign key due to the fact that different branches
can be within the same area.

7) Taxation_of_salary – Salary, 1:N relation. For different amounts (salaries) the same
effective rate of tax can be implemented. The ID of taxation_of_salary is unique. Hence it
serves as a primary key. Tax in the salary table is a foreign key.

8) Country - Producers, 1:N relation. This relation enables to connect Country names in the
Country table (ID is a primary key because each value is unique) with phone producers. Few
producers can have the same country of origin. Consequently, country_of_producer is a foreign
key in the Producers table.

9) Producers – Phones, 1:N relation. The relation shows the producers of particular phones
(e.g. the iPhone 7 is produced by Apple). Each producer in the Producers table is different,
which is why ID represents a primary key. However, different phones can have the same
producers so supplier in the Phones table is a foreign key.