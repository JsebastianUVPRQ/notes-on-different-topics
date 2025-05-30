As with PostgreSQL, there are many tools available to connect to MySQL that enable you to create and run scripts of SQL commands. You can use the mysql command-line utility, which is also available in the Azure Cloud Shell, or you can use graphical tools from the desktop such as MySQL Workbench. 

In this reading, you'll see how to connect to Azure Database for MySQL using MySQL Workbench. 

|**Note**|
|---|
|**Currently, there are no extensions available for connecting to MySQL from Azure Data Studio.**|

## **Retrieve connection information for Azure Database for MySQL** 

Like SQL Database and PostgreSQL, you require the name of the server, and the credentials for an account that has access rights to connect to the server. You can find the server name and the name of the default administrator account on the **Overview** page for the Azure Database for MySQL instance in the Azure portal. Contact your administrator for the password.
![[Pasted image 20240228002513.png]]
You must also open the MySQL firewall to enable client applications to connect to the service. For detailed information, see [Azure Database for MySQL server firewall rules](https://learn.microsoft.com/en-us/azure/mysql/single-server/concepts-firewall-rules?wt.mc_id=azsql_mysqulfrwlrules_webpage_extlp). 

## **Use MySQL Workbench to query a database** 

You can download and install MySQL Workbench from the [MySQL Community Downloads](https://dev.mysql.com/downloads/workbench) page. 

To connect to Azure MySQL Server by using MySQL Workbench, perform the following steps: 

1. Start MySQL Workbench on your computer.
    
2. On the **Welcome** page, select **Connect to Database**.
![[Pasted image 20240228002533.png]]

3. In the **Connect to Database** dialog box, enter the following information on the **Parameters** tab:
![[Pasted image 20240228002550.png]]

|**Setting**|**Description**|
|---|---|
|**Stored connection**|Leave blank|
|**Connection Method**|Standard (TCP/IP)|
|**Hostname**|Specify the fully qualified server name from the Azure portal|
|**Port**|3306|
|**Username**|Enter the server admin login username from the Azure portal, in the format <username><databasename>|
|**Password**|Select **Store in Vault**, and enter the administrator password specified when the server was created|
4. Select **OK** to create the connection. If the connection is successful, the query editor will open
![[Pasted image 20240228002622.png]]

You can use this editor to create and run scripts of SQL commands. The following example creates a database named _quickstartdb_, and then adds a table named _inventory_. It inserts some rows, then reads the rows. It changes the data with an update statement, and reads the rows again. Finally it deletes a row, and then reads the rows again.
```sql
-- Create a database
-- DROP DATABASE IF EXISTS quickstartdb;
CREATE DATABASE quickstartdb;

USE quickstartdb;
-- Create a table and insert rows

DROP TABLE IF EXISTS inventory;
CREATE TABLE inventory (id serial PRIMARY KEY, name VARCHAR(50), quantity INTEGER);
INSERT INTO inventory (name, quantity) VALUES ('banana', 150);
INSERT INTO inventory (name, quantity) VALUES ('orange', 154);
INSERT INTO inventory (name, quantity) VALUES ('apple', 100);

-- Read
SELECT * FROM inventory;

-- Update
UPDATE inventory SET quantity = 200 WHERE id = 1;
SELECT * FROM inventory;

-- Delete
DELETE FROM inventory WHERE id = 2;
SELECT * FROM inventory;
```
6. To run the sample SQL Code, select the lightning bolt icon in the toolbar
![[Pasted image 20240228002856.png]]
The query results appear in the **Result Grid** section in the middle of the page. The **Output** list at the bottom of the page shows the status of each command as it is run.

# EXERCISE: Use SQL to query Azure SQL Database​

This exercise requires a sandbox to complete. A sandbox gives you access to free resources. Your personal subscription will not be charged. The sandbox may only be used to complete training on Microsoft Learn. Use for any other reason is prohibited and may result in permanent loss of access to the sandbox. 

Contoso has provisioned the SQL database and has imported all the inventory data into the data store. As lead developer, you've been asked to run some queries over the data. 

In this exercise, you'll query the database to find how many products are in the database, and the number of items in stock for a particular product. 

## **Setup** 

To save time, the database is provisioned and populated running a script. You'll download the script from a GitHub repository. The script performs the following operations: 

- Creates an Azure SQL Database server. 
    
- Creates an Azure SQL database attached to the server. 
    
- Opens the firewall to allow SQL traffic from the internet. 
    
- Connects to the database and runs a SQL script to create a table and insert data. 
    

**You can access this exercise by clicking on the link below:** 

[https://learn.microsoft.com/en-us/training/modules/query-relational-data/6-exercise-perform-query?wt.mc_id=azsql_ex6prfmquery_webpage_extlp](https://learn.microsoft.com/en-us/training/modules/query-relational-data/6-exercise-perform-query?wt.mc_id=azsql_ex6prfmquery_webpage_extlp)