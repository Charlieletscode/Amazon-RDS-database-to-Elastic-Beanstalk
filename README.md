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
Review the default settings and adjust these settings according to your specific requirements. Pay attention to the following options:
DB instance class – Choose an instance size that has an appropriate amount of memory and CPU power for your workload.
Multi-AZ deployment – For high availability, set this to Create an Aurora Replica/Reader node in a different AZ. (do this first to edit db name)
Master username and Master password – The database username and password. Make a note of these settings because you will use them later.
ex:postgres, 0000000
Verify the default settings for the remaining options, and then choose Create database.

<br>
<br>
To modify the inbound rules on the security group that's attached to your RDS instance
1. Open the Amazon RDS console.
2. Choose Databases.
3. Choose the name of your DB instance to view its details.
4. In the Connectivity section, make a note of the Subnets, Security groups, and
Endpoint that are displayed on this page. This is so you can use this information later.
5. Under Security, you can see the security group that's associated with the DB instance.
Open the link to view the security group in the Amazon EC2 console.
6. In the security group details, choose Inbound.
7. Choose Edit.
8. Choose Add Rule.
9. For Type, choose the DB engine that your application uses.
10. For Source, type sg- to view a list of available security groups. Choose the security
group that's associated with the Auto Scaling group that's used with your Elastic
Beanstalk environment. This is so that Amazon EC2 instances in the environment can
have access to the database.
11. then save
![image](https://github.com/Charlieletscode/Amazon-RDS-database-to-Elastic-Beanstalk/blob/main/img1.png)

## install wordpress

## To launch an environment (console)
1. Open the Elastic Beanstalk console using this preconfigured link: console.aws.amazon.com/elasticbeanstalk/home#/newApplication?applicationName=tutorials&environmentType=LoadBalanced

2. For Platform, select the platform and platform branch that match the language used by your application.

3. For Application code, choose Sample application.

4. Choose Review and launch.

5. Review the available options. Choose the available option you want to use, and when you're ready, choose Create app.

