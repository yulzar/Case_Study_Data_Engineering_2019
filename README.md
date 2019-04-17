# Credit Card Management System

A credit card is a payment card issued to users as a system of payment. It allows the cardholder to pay for goods and services based on the holder's promise to pay for them. 

**The Credit Card Products** will include the following fields that can be adjusted and viewed by the managers of the Bank.


## 1. Transaction and Customer Details Module

- **Using the database and respective tables for the case study**

1. If not exists, create the *MySQL connection* with *MySQL workbench* with the following properties:

   •	User: root
   •	Password: password
   •	Port: 3306 (Local Instance)

   This connection is used throughout the requirements.
   PATH: `C:\Users\Students\Desktop\Case_study_deliverable\2. Customer and Transaction Details Module_db`

2. Open the existing .sql file named db.sql with MySQL Workbench found under the path above.

3. Execute the file to automatically create and populate the database cdw_sapp with records used during requirements.

- ###### Executing with Eclipse.

  PATH: `C:\Users\Students\Desktop\Case_study_deliverable\1. Customer and Transaction Details Module\Case_study_JAVA.zip`

1. Unzip Case_study_JAVA found under the path above.

2. Set the Eclipse’s default workspace to the
   path above. This is where the project contents is located.

3. On first opening the project, you may experience an error, due to a missing JDBC jar. Follow these steps to add the jar:

   - Right on Referenced Libraries in the Eclipse file explorer and navigate to Build Path > Configure Build Path.
   -  Navigate to Add External Jar.

   PATH: `/user/oozie/share/lib/lib_20161025075203/sqoop/java-json.jar`

   - Use the provided file explorer to add the JDBC jar with the above path.

   

4. Execute the code by clicking on the Run button and available options for customer and transactions.

  

## 2. Data Extraction and Transformation Module 



Employed *Sqoop* to extract the data according to the specifications found in the mapping document.

1. Open Hadoop’s local terminal on any web browser with the URL: *[http://192.168.109.131:4200](http://192.168.109.131/)*.

PATH: `C:\Users\Students\Desktop\Case_study_deliverable\Sqoop`

2. Copy and paste each sqoop job command found in the path above into terminal and execute to create the sqoop jobs.

3. Copy and paste each sqoop run command found in the path above into terminal and execute to run the sqoop jobs.

## 3. Data Loading Module



Employed *Hive* to create tables in the *Hadoop File System* and then load the data extracted via *Sqoop* into those tables.

1. Open *Ambari* by opening any web browser with the URL: 

   *[http://192.168.109.131:8888](http://192.168.109.131/)*

2. Enter login credentials for user maria_dev and navigate to Hive View.

PATH: `C:\Users\Students\Desktop\Case_study_deliverable\4. Data Loading Module`

3. Copy and paste the contents of the file in the above path into hive and execute.

## 4. Process Automation Module

​                PATH:`C:\Users\Students\Desktop\Case_study_deliverable\Oozie_unoptimized_workflow.zip`

1. Place the file located in the above path into package `\root\Documents\foldername\` on the linux virtual machine.

PATH: `C:\Users\Students\Desktop\Case_study_deliverable\Oozie_unoptimized_workflow.zip\coordinator_unopt`

PATH: `C:\Users\Students\Desktop\Case_study_deliverable\Oozie_unoptimized_workflow.zip\workflow`

2. Place the two files located in above paths into package `/user/maria_dev/credit_card_system_files/` on HDFS

3. Make sure to test the hive query specific to the non incremental *Oozie* workflow from the path C:`\Users\Students\Desktop\Case_study_deliverable\Oozie_unoptimized_workflow.zip\workflow`

## 5. Process Optimization Module 

5.1. For optimizing the process  *Sqoop* should *only import new data*. Hive should then import *only that new data*. Original data should not be deleted in this sqoop/hive process.

5.2. Modify the *Oozie Coordinator* to use this workflow rather than the original, unoptimized, workflow.

PATH: `C:\Users\Students\Desktop\Case_study_deliverable\Oozie_optimized_workflow.zip\job_opt.properties`.

1. Place the file located in the above path into package `/user/maria_dev/credit_card_system_files/` on the linux virtual machine.

PATH: `C:\Users\Students\Desktop\Case_study_deliverable\Oozie_optimized_workflow.zip\coordinator`

PATH: `C:\Users\Students\Desktop\Case_study_deliverable\Oozie_optimized_workflow.zip\workflow_opt`

2. Place the two files located in above paths into package `/user/maria_dev/credit_card_system_files/`  HDFS.

3. Execute the oozie workflow_opt with necessary changes the hive query and sqoop jobs and workflow_opt.xml as per the incremental workflow requirements

## 6. Data Visualization

PATH: `C:\Users\Students\Desktop\Case_study_deliverable\7. Data Visualization`

###### KEY TOOLS 

- Eclipse IDE for Java Developers.
- MySQL Workbench.
- Hive
- Sqoop
- Oozie
- Tableau
- Visme
- Sublime Text
- Typora