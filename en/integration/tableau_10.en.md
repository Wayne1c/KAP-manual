## Integration with Tableau 10.x

### Install Kyligence ODBC Driver

For the installation information, please refer to [Kyligence ODBC Driver tutorial](../driver/kyligence-odbc.en.md).

### Connect to Kylin Server
Connect Using Driver: Start Tableau 10.1 desktop, click `Other Database(ODBC)` in the left panel and choose KylinODBCDriver in the pop-up window. 


![](images/tableau_10/1.png)

Click `Connect` button and input the server information, then click `ok`.

![](images/tableau_10/2.png)

### Mapping Data Model
In left panel, select `defaultCatalog` as Database, click `Search` button in Table search box, and all tables get listed. Drag the table to right side, then you can add this table as your data source and edit relation between tables(mapping information is shown in figure).

**NOTE: Tableau will send query "select \* from fact\_table" and it'll take a long time if the table size is extremely large. To work around the issue please refer to [Configuration](../config/basic_settings.en.md#kylinqueryforce-limit)**

![](images/tableau_10/step5.PNG)

### Connect Live

There are two types of Connection in Tableau 10.1, choose the Live option to make sure using Connect Live mode.

### Custom SQL
To use customized SQL, click `New Custom SQL` in left panel and type SQL statement in pop-up dialog.

### Visualization

Now you can start to enjou analyzing with Tableau 10.1.
![](images/tableau_10/step13.PNG)

### Publish to Tableau Server
If you want to publish local dashboards to a Tableau Server, just expand `Server` menu and select `Publish Workbook`.


