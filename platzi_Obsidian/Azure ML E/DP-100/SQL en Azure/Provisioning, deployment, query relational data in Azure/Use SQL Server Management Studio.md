
SQL Server Management Studio is another tool that you can download and run on your desktop. See [Download SQL Server Management Studio (SSMS)](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16&wt.mc_id=azsql_dwnldsqlsrvr_webpage_extlp) for details. 

To connect to a server and database, perform the following steps: 

1. Open SQL Server Management Studio. 
    

2. When the Connect to Server dialog box appears, enter the following information: 

|**Setting**|**Description**|
|---|---|
|**Server type**|Database engine|
|**Server name**|The fully qualified server name, from the Overview page in the Azure portal|
|**User name**|SQL Server Authentication|
|**Authentication**|The user ID of the server admin account used to create the server.|
|**Login**|The name of the database to which you wish to connect.|
|**Password**|Server admin account password|


3. Select **Connect**. The Object Explorer window opens. 

4. To view the database's objects, expand **Databases** and then expand your database node.

5. On the toolbar, select **New Query** to open a query window.

1. Enter your SQL statements, and then select **Execute** to run queries and retrieve data from the database tables.

![[Pasted image 20240228000714.png]]