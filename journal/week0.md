## **Prerequisites:**  
In order to start this exciting bootcamp, we need to perform few actions to ensure that prerequisites are completed.
Here, I would definitely recommend to take a look of below mnetioned youtube playlist to get more idea and clarity.  
- *Create github free account. Please take a look of this sample github repository provided by Andrew and create your own repository.* 
- *Setup MFA in github account.*  
- *Create Gitpod free tier account and download gitpod extension for quick movement. That really helps to do some codes instantly without configuring much.*  
- *Open AWS free tier account which is valid for a year with some usage limitation to control billing.Please check this link for getting more info onAWS resource usage limit in free tier account [AWS Free Tier Usage](https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all)*  
- *Create Honeycomb.io free account*  
- *Create Rollbar free account*  
Once you register for above all accounts, then please go for Week 0 assignments.  
Please check the youtube video playlist for getting more updates on this bootcamp [AWS CloudProjectBootcamp](https://www.youtube.com/playlist?list=PLBfufR7vyJJ7k25byhRXJldB5AiwgNnWv)  

## Week 0 — Billing and Architecture:  
This week has been dedicated for discussing on AWS Billing, setup billing alarms, create IAM user and provide AWS CLI access by creating Access keys.Once AWS account is created, then please ensure you setup billing alarms in order to avoid unwanted charges. Billing depends on AWS regions completely, for each regions, charges would be different, also depends on resources utlization and compute specifications. For example, for an EC2 instances, t2.medium will incur more charges than t2.micro as it cosumes more CPU and memory resources.  

# **Billing Alerts, Tags, Cost Explorer:**  
This session will describe on How to setup billing alarms, budgets, cost explorers etc.  
## **Billing Alarms**:  
There are 2 ways to setup alams.  
- Using Budget. For free trier account, maximum 2 budgets we can created. Exceeding the limit will incur costs.  
- Using Cloudwatch Alarms. Here, you have to create alarm in us-east-1 region by using cloudwatch with SNS topic. Here SNS topic would be used to send an email notification. 
 
![image](https://user-images.githubusercontent.com/67305577/219559078-910c79d2-bf77-463d-934d-6757200eee71.png)
 
By setting up billing alerts, you can stay informed about your AWS costs and avoid unexpected charges.  

![image](https://user-images.githubusercontent.com/67305577/219075632-8973e54c-ea21-49dc-a955-b0484dac3fc2.png)    

## **Bills**:  
Bills option in AWS billing console provides a compact view of all consumed resources in all regions. By default it shows the crrency in USD, but from preferences setting you can also include local currrency. We can get invoices for all months and do payment based upon the total amount show in the bills. For payment , you have to choose Credit/Debit card during account setup. Later also it can be changed.

## **Cost Explorer**:  
- Cost explorer is an aws service which provides detailed analysis of costs over the time, identify cost trends and anomalies, and optimize your spending by making informed decisions about your AWS resources.  
- Also, you can prepare monthly cost report, savings plan and more. During migratios basically engineers need to understand the savings from On-prem to AWS Cloud and for this purpose we can create saving report by putting some details.  
- We can get budget report as well and make modifications based upon the utilizations. AWS also provides recommendations to secure the account.  

## **Cost Allocation Tags**:  
Tags are simple key-valur pairs which can be used for understanding the expenses for a certain environment. For example, to get an idea about the costs for Dev environment, we can create a tag with environment.

## **Pricing Calculator**:  
AWS provides a very useful pricing calculator to estimate the costs to be incurred for a certain workload. For exmaple, if yoou have a requirement to deploy 100 EC2 instances, then you can easily get an estimation of costs for 100 instances by using [Pricing Calculator](https://calculator.aws/#/).  

# **IAM User and Roles**:  
Initially during aws account setup, we do activities as a root user, then we have to ensure that we create IAM users with Administrator priviledge for further activity and do not use root user anymore. Also, setup MFA for a root user to enhance additional layer of security. please follow below steps to create IAM users -->  
- Open IAM console and create IAM user.
- Create group for categorization.
- Create a role with required admin priviledges.
- Attach the role to that particular user.  

![image](https://user-images.githubusercontent.com/67305577/219557476-452513f3-f8fb-4a56-8fd4-6ca409679765.png)

![image](https://user-images.githubusercontent.com/67305577/219076623-302d2b75-278b-44f1-9b26-d967d5d73fa6.png)

## **Access Keys**:  
For accessing AWS cli, access keys should be created by root user. Create an access key which will generate another key (secret access key), these both keys will be used while working in CLI/API. Please note once these two keys got generated, keep these in safe place like securityhub or any vault as if we lose it, then it won't be recoverd. We have to create once againthat may cause a problem. Also make sure these keys should not be written in plain text format like in notepad or any code repositories to avoid account expolitation.  

## **Cloudshell**:  
Cloudshell is basically aws managed browser based shell which provides leverage to perform administrative tasks without any requirement of distinct software sessions. This services contains some preinstalled tools like AWS CLI, python, Node.js and more with 1GB free storage per AWS region. The main advantage is persistant storage capability that defines whatever data you are going to store under home directory would be available for future sessions in same region that reduces the chances of data loss.

# **Architectural Diagram in Lucid Charts**:  

![lucid_chart](https://user-images.githubusercontent.com/67305577/219072734-d8ea7f6b-2052-4545-8fc2-c42264deb1b8.png)  

# **What is C4 Model**  

For any particular project, there should have some minor projects or targets which needs to be completed to get this job done in proper way that can lead different kind of difficulies when multiple individuals participate in the discussion from different domain or field. To make this entire discussion simple, basically we are used to create some PPT or any high level diagram and this diagram must be understandable from all point of view irrrespective of the domain. To simplify it, a new approach has been taken to visualize an entire planning, our target, what this project is all about, how it can be done and so many.  
In C4, each “C” represents a different type of model at a different level of detail. These different levels are known as  
- context
- containers
- components
- code  

The diagrams you draw for these different levels help you to tell the right story to the right audience.
