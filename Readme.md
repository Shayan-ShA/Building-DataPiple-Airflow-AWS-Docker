<h2>Overview</h2>
A music streaming company, Sparkify, has decided that it is time to introduce more automation and monitoring to their data warehouse ETL pipelines and come to the conclusion that the best tool to achieve this is Apache Airflow. I created high grade data pipelines that are dynamic and built from reusable tasks, can be monitored, and allow easy backfills. They have also noted that the data quality plays a big part when analyses are executed on top the data warehouse and want to run tests against their datasets after the ETL steps have been executed to catch any discrepancies in the datasets. The source data resides in S3 and needs to be processed in Sparkify's data warehouse in Amazon Redshift. The source datasets consist of CSV logs that tell about user activity in the application and JSON metadata about the songs the users listen to.


<h2> Files description </h2>
 <ol>
  <li>airflow</li>
	Contains dags, operators, and helpers functions 
	Also contains udacity_s3_redshift_dag.py which defines the airflow dag and all its functions 			and settings
  <li>data</li>
	sample data for testing purpose using Postgres
	stagingarea: contains already concatenated tables of events and songs
	not needed for Redshift as it will directly query S3	
  <li>Dockersetup</li>
	store Docker files to create images of Airflow and Postgres
	and sample scripts how to launch airflow and pg as stand-alone for debugging
  <li>docker-compose.yml, .env files</li>
	environment-specific files, need to be configured before launching docker-compose
</ol> 


<h2> How to run the project </h2>
Use the folder CreateRedshift to create a Redshift Warehouse and an admin ARN with access to S3
Run the Redshift cluster
Aws credentials are saved in Airflow connections under aws_credentials
Fill in the .env file with ARN and the Redshift Cluster endpoint




![This](https://www.youtube.com/watch?v=aTaytcxy2Ck) is a youtube link to setup airflow on your local computer using the airflow folder in this repository.)





Save your AWS Redshift cluster information in Airflow connections
Turn on udacity_s3_redshift_dag DAG on airflow UI interface and run it to see the results.




![Certificate.pdf](https://github.com/Shayan-ShA/Data-Modeling-with-Postgres-and-Cassandra-Projects-Udacity_DataEngineering/blob/main/Certificate.png)





