# Hands-on-Lab-Populating-a-Data-Warehouse-using-PostgreSQL

The lab is designed to provide hands-on experience in creating and managing a production database using PostgreSQL. 

You will learn how to launch a PostgreSQL server instance, utilize the pgAdmin graphical user interface (GUI) for database operations, and execute essential tasks like creating a database, designing tables, and loading data. The lab focuses on building a foundation in database management by guiding learners through the process of setting up a 'Production' database and populating it with data following a star schema design.

# Software Used in this Lab

To complete this lab you will utilize the PostgreSQL Database relational database service.

![image](https://github.com/user-attachments/assets/4903573c-45dc-407d-985e-8d66dd6927f2)

# Objectives

In this lab you will:

Create production related database and tables in a PostgreSQL instance.
Populate the production data warehouse byloading the tables from Scripts.

# Lab Structure

In this lab, you will complete several tasks in which you will learn how to create tables and load data in the PostgreSQL database service using the pgAdmin graphical user interface (GUI) tool.

# Data Used in this Lab
The following are the SQL data files used in this lab.

The production database contains:

Star Schema - Use the SQL script here to create tables in the Production database (https://drive.google.com/file/d/1pzGEQ5DV2EBiEeteqDSHK7G0nHMKUYBP/view?usp=sharing )
DimCustomer - Use the SQL script here to create the DimCustomer table (https://drive.google.com/file/d/1j8M0NqeQVYecoJCWHSblY5fmtRpD-zSr/view?usp=sharing)
DimMonth - Use the SQL script here to create the DimMonth table (https://drive.google.com/file/d/1kgfe5Wq9UlQj6FzCdezMGut0Om3AHGYr/view?usp=sharing)
FactBilling - Use the SQL script here to create the FactBilling table (https://drive.google.com/file/d/1lxCnZoFqL6J9HTBMRG3KTHIiCmD_ApR_/view?usp=sharing)

# Task A: Create a database

1. Open the pgAdmin Graphical User Interface
   
2. Once the pgAdmin GUI opens, click on the Servers tab on the left side of the page. You will be prompted to enter a password.
   
![image](https://github.com/user-attachments/assets/51aa4680-d798-48e5-98f6-5bfd5aa7772b)

3. Input your password, then click OK.

![image](https://github.com/user-attachments/assets/8d7f2d64-b412-49af-9558-67acbbcbb576)

4. You will then be able to access the pgAdmin GUI tool.

5. In the left tree-view, right-click on Databases> Create > Database.

![image](https://github.com/user-attachments/assets/5fdc2ff1-98d9-4c02-9573-94551be1a9bb)

6. In the Database box, type Production as the name for your new database, and then click Save. Proceed to Task B.

![image](https://github.com/user-attachments/assets/2949f399-0869-4c7c-b97c-a3e09d0b31d7)

# Task B: Create tables

Now, that you have your PostgreSQL service active and have created the Production database using pgAdmin, 
let's go ahead and create a few tables to populate the database and store the data that we wish to eventually upload into it.

1. Click on the Production database and in the top of the page go to Query tool and then click on Open File. Next a new page pops up called Select File. Click on Upload icon as shown in the screenshot.

![image](https://github.com/user-attachments/assets/f9d6901d-ca3c-4aef-b5f5-b9d6bdbffd84)

2. In the new blank page that appears drag and drop the star-schema.sql file inside the blank page. Once the star-schema.sql file is successfully loaded, click on the X icon on the right hand side of the page as shown in the screenshot.

![image](https://github.com/user-attachments/assets/b1cbecc0-d02a-4b8a-9e67-a53b7fd1727b)

3. Once you click on the X icon a new page appears with the file star-schema.sql. Select the star-schema.sql file from the list and click the Select tab.

![image](https://github.com/user-attachments/assets/9cdfe6d3-1996-4e1f-bd8b-cd2c59b8390c)

4. Once the file opens up click on the Run option to execute the star-schema.sql file.

![image](https://github.com/user-attachments/assets/b4e77188-c827-4839-a5a0-1493be2b037b)

5. Next, right-click on the Production database and click on the Refresh option from the dropdown.

![image](https://github.com/user-attachments/assets/f5641287-7a26-4ac5-a1df-89f84870d944)

6. After the database is refreshed the 3 tables (DimCustomer, DimMonth,FactBilling) are created under the Databases > Production > Schemas > Public > Tables.

![image](https://github.com/user-attachments/assets/b2f7f91a-a5c6-4eb4-8c29-dfc19f30693d)

# Task C: Load tables

1. Click on Query tool and then click Open file and click on Upload icon.

![image](https://github.com/user-attachments/assets/df383bdd-39a6-44f3-a390-ef5625d797d8)

2. In the new blank page that appears drag and drop the DimCustomer.sql file inside the blank page. Once the DimCustomer.sql file is successfully loaded.

3. Click on the small X icon on the right hand side of the page as shown in the screenshot.

![image](https://github.com/user-attachments/assets/648bfcdf-1398-4605-81cf-88cdc44649d8)

4. Once you click on the X icon a new page appears with the file DimCustomer.sql. Select the DimCustomer.sql file from the list and click on Select tab.

![image](https://github.com/user-attachments/assets/6c5c35d0-c88d-424f-b5cc-7ab9b2acb8f8)

5. Once the file opens up, click on the Run option to execute the DimCustomer.sql file.

![image](https://github.com/user-attachments/assets/e689f14a-a63e-4173-af17-e0ea6c8eab6a)

6. Note: Repeat the steps as given in Task C to upload the remaining sql files to insert data in DimMonth and FactBilling.

# Task D: Preview the tables you just uploaded

To preview the table, right-click on the table, navigate to View > First 100 Rows

DimCustomer Table

![image](https://github.com/user-attachments/assets/86308067-7bbe-412b-9209-350f093df2f4)

DimMonth Table

![image](https://github.com/user-attachments/assets/3d397bed-43df-440a-9bb3-7c4a463e0cc1)

FactBilling Table

![image](https://github.com/user-attachments/assets/dbb4dfc2-596e-40fa-96fe-4d27a5ac0d6f)

# Task E: Solve some SQL problems

- Problem 1: Using the PostgreSQL tool, find the count of rows in the tables

  To find the count of rows in the DimCustomer Table, I issued the following query:

         select count(*) from public."DimCustomer";

![image](https://github.com/user-attachments/assets/2c95b645-2a9c-430c-9d4b-7a99577c7e21)

  To find the count of rows in the DimMonth Table, I issued the following query:

         select count(*) from public."DimMonth";

![image](https://github.com/user-attachments/assets/a2888aed-cb15-4cbf-81e3-c8ea2b1f3895)

  To find the count of rows in the FactBilling Table, I issued the following query:

         select count(*) from public."FactBilling";

![image](https://github.com/user-attachments/assets/be0dbc04-2a66-40ac-acc5-ce99bbc0b360)

- Problem 2: Using the PostgreSQL tool, create a simple Materialized views named avg_customer_bill with fields customerid and averagebillamount.

  To create a simple Materialized views, I issued the following query statement

         CREATE MATERIALIZED VIEW  avg_customer_bill (customerid, averagebillamount) AS
         (select customerid, avg(billedamount)
         from public."FactBilling"
         group by customerid
         );

 ![image](https://github.com/user-attachments/assets/e41acbe3-fade-4011-806e-e13906eb0aae)

 - Problem 3: Refresh and preview the newly created Materialized views

   Right-click on the Materialized view and then select "Refresh". After refreshing, right-click again to select View > First 100 Rows

![image](https://github.com/user-attachments/assets/1dd2d39e-e74b-4a14-a0ee-d4aed12c407b)

- Problem 4: Using the newly created Materialized views find the customers whose average billing is more than 11000.

  I solved this problem by issuing the following query statement:

         select * from avg_customer_bill where averagebillamount > 11000;

![image](https://github.com/user-attachments/assets/9903cb13-4c59-468a-849c-b210ca47c026)












