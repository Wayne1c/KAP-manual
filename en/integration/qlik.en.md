## Integration with Qlik Sense

Qlik Sense delivers intuitive platform solutions for self-service data visualization, guided analytics applications, embedded analytics and reporting. It is a new player in the Business Intelligence (BI) tools world, with a high growth since 2013. It has connectors with Hadoop Database (Hive and Impala). Now it can be integrated with KAP. This article will guide you to connect KAP with Qlik Sense.  

### Install Kyligence ODBC Driver

For the installation information, please refer to [Kyligence ODBC Driver tutorial](../driver/kyligence-odbc.en.md).

#### Install Qlik Sense

For the installation of Qlik Sense, please visit [Qlik Sense Desktop download](https://www.qlik.com/us/try-or-buy/download-qlik-sense).

### Connection with Qlik Sense
After configuring your Local DSN and installing Qlik Sense successfully, you may go through the following steps to connect Kylin with Qlik Sense.

1. From Windows Desktop Shortcut or click **Start -> All Applications -> Qlik Sense -> Qlik Sense Desktop** to open the application **Qlik Sense Desktop**.

2. Input your Qlik account to login, then the following dialog will pop up. Click **Create New Application**.

![Create New Application](images/qlik/welcome_to_qlik_desktop.png)

You may specify any name different from existing applications and then open this application. In this example, we name it as “Kylinfortesting".

![Specify a unique name](images/qlik/create_new_application.png)

3. There are two choices in the Application View. Please select the bottom **Script Editor**.

![Select Script Editor](images/qlik/script_editor.png)

The Kylinfortesting | Data Load Editor window shows. Click **Create New Connection** in the upper right of this page.

![Create New Data Connection](images/qlik/create_data_connection.png)

Select **ODBC -> kylin**, ignore the account information, and then click **Create**. 

![ODBC Connection](images/qlik/odbc_connection.png)

4. Change the default scripts of "TimeFormat", "DateFormat" and "TimestampFormat" to:

`SET TimeFormat='h:mm:ss';`
`SET DateFormat='YYYY-MM-DD';`
`SET TimestampFormat='YYYY-MM-DD h:mm:ss[.fff]';`

5. Load columns from KAP to Qlik Sense:

As we have logged in KAP and select the project **learn_kylin** during local DSN configuration, currently we only need to new a query **select * from KYLIN_SALES** in KAP.

![Query in KAP](images/qlik/kap_query.png)

Export the query results and copy them to the script editor in Qlik Sense Desktop with comma as delimiter. 

![Script Running](images/qlik/script_run_result.png)

In the running result, the line count shall be the same as in KAP. In this case, the line count is 10,000.

![Script Running Result](images/qlik/load_data.png)

6. Load data to Qlik Sense:

After the scripts run successfully, click **Load Data** in the upper right of the window Kylinfortesting | Data Load Editor. And then open **Data Manager**.

![Open Data Manager](images/qlik/open_data_manager.png)

Now Data manager opens. Click **Load Data** in the upper right of this page, and click **Edit worksheet** once data loaded.

![Load Data in Data Manager](images/qlik/data_load2.png)

Select the charts you need, then add dimension and measurement based on your requirements. 

![Select the required charts, dimension and measure](images/qlik/add_dimension.png)

You will get your worksheet and the connection is complete. Your KAP data shows in Qlik Sense now.

![View KAP data in Qlik Sense](images/qlik/final.png)