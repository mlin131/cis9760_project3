Project3: Streaming Finance Data with AWS Lambda

Author: Mingxing (Max) Lin

Date Created: 05/09/2023

Class: CIS9760

Project Objective: In this project, I am tasked with provisioning a Lambda function to generate near real time finance data records for interactive querying, data analysis and visualization.

Project Procedure:  First  step: I created a Kinesis Data and Delivery Stream connecting to Amazon S3 as file designation. Then, I created a Lambda function and added a Lambda layer by uploading a layer zip file. Later, I wrote a Lambda function to collect the stock price data from yahoo finance and push it to the Kinesis Delivery Stream using python. The queried data will be stored in pre-created S3 bucket. 

![kinesis_config](https://github.com/mlin131/cis9760_project3/assets/119923435/edf2151e-0456-45a6-a04f-0ac17a8a94df)
![exec_results](https://github.com/mlin131/cis9760_project3/assets/119923435/b730f730-72fc-4b12-baed-5735dd4e2fdb)
![screenshot_of_s3_bucket](https://github.com/mlin131/cis9760_project3/assets/119923435/02553584-e9af-4009-aa54-ca983e90e42a)


Second Step: I confiure AWS Glue and database that connect to S3 bucket I previously created. This will allow me to now interactively query previous collected stock data in AWS Athena using SQL to gain all required data for analysis.  
![results](https://github.com/mlin131/cis9760_project3/assets/119923435/7f5053ef-8c30-4cec-8801-87b120f3ff5d)

Final step: I downloaded and uploaded previous SQL queried data in excel file from AWS Athena to EMR Jupyter Notebook. I cleaned the data excel file, and generate the visualization using Pyspark for answering two questions below:

Which company is the most volatile?
COST has the most volatile.
![image](https://github.com/mlin131/cis9760_project3/assets/119923435/3b39a9cc-b10f-4401-811c-e0b3070b1612)

Do the findings from this graph support your conclusion from the first graph? 
Yes
![image](https://github.com/mlin131/cis9760_project3/assets/119923435/c0cfe6a7-588a-42a8-a613-9ab30264ad31)
