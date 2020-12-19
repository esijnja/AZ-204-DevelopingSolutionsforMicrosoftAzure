#### Task 3: Import an SQL database

1.  Go to the blade for the **polysqlsrvr*[yourname]*** SQL server resource that you created earlier in this lab.

1.  Import the database from your Azure Storage account into the SQL server instance by using the following details:

    -   Storage account: **polystor*[yourname]***

    -   Database backup blob: **databases\AdventureWorks.bacpac**

    -   Database name: **AdventureWorks**

    -   Server admin login: **testuser**

    -   Password: **TestPa55w.rd**

    > **Note**: Wait for the database to be created before you continue with this lab. If you receive a firewall-related error on the import step, it means you did not correctly configure the **Allow Azure services to access server** setting on your SQL Server earlier in the lab.  Review your settings, delete the empty **AdventureWorks** database, and then attempt your import again.