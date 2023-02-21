# Amazon-RDS-database-to-Elastic-Beanstalk

# Prerequisites Install WSL command
on Windows powershell
```
wsl --install
```

Then hop to this page
https://console.aws.amazon.com/rds/home
![image](https://github.com/Charlieletscode/Amazon-RDS-database-to-Elastic-Beanstalk/blob/main/Untitled.png)

1. In the navigation pane, choose Databases.
2. Choose Create database.
3. Choose Standard Create.
4. Under Additional configuration, for Initial database name, type ebdb.
5. Review the default settings and adjust these settings according to your specific requirements. Pay attention to the following options:
DB instance class – Choose an instance size that has an appropriate amount of memory and CPU power for your workload.
Multi-AZ deployment – For high availability, set this to Create an Aurora Replica/Reader node in a different AZ.
Master username and Master password – The database username and password. Make a note of these settings because you will use them later.
6. Verify the default settings for the remaining options, and then choose Create database.
