# Configuring Security in Amazon Aurora<a name="UsingWithRDS"></a>

You can manage access to your Amazon RDS resources and your databases on a DB instance\. The method you use to manage access depends on what type of task the user needs to perform with Amazon RDS: 
+ Run your DB instance in an Amazon Virtual Private Cloud \(VPC\) for the greatest possible network access control\. For more information about creating a DB instance in a VPC, see [Using Amazon RDS with Amazon Virtual Private Cloud \(VPC\)](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_VPC.html)\. 
+ Use AWS Identity and Access Management \(IAM\) policies to assign permissions that determine who is allowed to manage RDS resources\. For example, you can use IAM to determine who is allowed to create, describe, modify, and delete DB instances, tag resources, or modify security groups\.

   For information on setting up an IAM user, see [Create an IAM User](CHAP_SettingUp_Aurora.md#CHAP_SettingUp_Aurora.IAM)\.
+ Use security groups to control what IP addresses or Amazon EC2 instances can connect to your databases on a DB instance\. When you first create a DB instance, its firewall prevents any database access except through rules specified by an associated security group\. 
+ Use Secure Socket Layer \(SSL\) connections with DB instances running the Aurora MySQL or Aurora PostgreSQL\. For more information on using SSL with a DB cluster, see [Using SSL to Encrypt a Connection to a DB Cluster](UsingWithRDS.SSL.md)\.
+ Use RDS encryption to secure your RDS instances and snapshots at rest\. RDS encryption uses the industry standard AES\-256 encryption algorithm to encrypt your data on the server that hosts your RDS instance\. For more information, see [Encrypting Amazon RDS Resources](Overview.Encryption.md)\.
+ Use the security features of your DB engine to control who can log in to the databases on a DB instance, just as you do if the database was on your local network\. 

**Note**  
You only have to configure security for your use cases\. You don't have to configure security access for processes that Amazon RDS manages, such as creating backups, replicating data between a master and a Read Replica, or other processes\.

For more information on managing access to Amazon RDS resources and your databases on a DB instance, see the following topics\.

**Topics**
+ [Authentication and Access Control](UsingWithRDS.IAM.md)
+ [Encrypting Amazon RDS Resources](Overview.Encryption.md)
+ [Using SSL to Encrypt a Connection to a DB Cluster](UsingWithRDS.SSL.md)
+ [Controlling Access with Security Groups](Overview.RDSSecurityGroups.md)
+ [Master User Account Privileges](UsingWithRDS.MasterAccounts.md)
+ [Using Service\-Linked Roles for Amazon RDS](UsingWithRDS.IAM.ServiceLinkedRoles.md)
+ [Amazon Virtual Private Cloud \(VPCs\) and Amazon RDS](USER_VPC.md)