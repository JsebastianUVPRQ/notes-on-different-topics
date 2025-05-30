
Visual Studio is a popular development tool for building applications. It's available in several editions. You can download the free community edition from the  [Visual Studio Downloads](https://visualstudio.microsoft.com/downloads/) page on the Microsoft website. 

SQL Server Data Tools are available from the **Tools** menu in Visual Studio. To connect to an existing Azure SQL Database instance: 

1. In Visual Studio, on the Tools menu, select SQL Server, and then select New Query. 
    

2. In the Connect dialog box, enter the following information, and then select Connect: 

|**Setting**|**Value**|
|---|---|
|**Server name**|The fully qualified server name, from the Overview page in the **Azure portal**|
|**Authentication**|SQL Server Authentication|
|**Login**|The user ID of the server admin account used to create the server|
|**Password**|Server admin account password|
|**Database name**|Your database name.|

1. In the **Query** window, enter your SQL query, and then select the **Execute** button in the toolbar. The results appear in the **Results** pane.
![[Pasted image 20240228000957.png]]