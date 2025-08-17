# weather_pipeline
Weather Data Pipeline — Lambda → S3 → Glue Job (JSON to CSV). Can be fed to Quicksight for analytics.

The CF Template contains complete flow of Lambda fetching weather data from Open API and ingesting it to S3. Glue job(2 options- Glue Studio and Spark ETL) triggering to convert S3 contents to destination S3 bucket in csv format.
The Output S3 contents in csv can be ingesting manually into Quicksight for analytics.


Not contained in CF template:
1.	Lambda Function and its dependencies.
2.	The complete Lambda function package resides in S3 bucket.
3.	The S3 bucket and key are mentioned as parameters in CF template.
4.	For the first time, Glue job needs to be created manually for csv creation. This stores script for the conversion in S3. Once script is stored in S3, the S3 buckets- raw and processed can be deleted. As these will be created in CF.


The Folder Infra contains CF template

** Glue job not getting triggered because of Python Version.

Test2
