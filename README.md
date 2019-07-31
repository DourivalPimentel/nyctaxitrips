# Data Analysis of a New York City taxi trips dataset

The analysis was built inside a Spark - Databricks cluster with direct access to a s3 Storage inside AWS.

The script runs over the pre-built instalation of Apache Spark and use Databricks connection libraries to read and writes files on AWS s3. It's possible to re-run the script anytime from any databricks account, since the s3 bucket where the files are stored is set as public, and the tokens used for access are hardcoded in the script.
The security issues were overlook only because this was a simple study over a public dataset and because it would be harder to replicate without a good amount of set ups in a safer enviroment. So the access tokens are only hardcoded for simplicity and are hardly an option for a comercial solution.

## To run the script

Any Databricks account can import the same code with the link bellow throguht the databricks pannel. A quick guide to do it is also shown in the second link bellow. To create a free community databricks account you'll only need an email account. 

<a href="https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/1536705237491348/498675988431179/6882450809162848/latest.html">Link to import the script with the analysis.</a> 

<a href="https://docs.databricks.com/user-guide/notebooks/notebook-manage.html#import-a-notebook">Quick guide to import the script if needed.</a>

<a href="https://databricks.com/signup/signup-community">Link to create a community databricks account.</a>

<a href="https://docs.databricks.com/getting-started/quick-start.html#step-2-create-a-cluster">Quick guide to start a cluster inside Databricks Community Edition if needed.</a>

Although it may seem like a lot, every step is quite simple and fast. The longer one being the wait for the start of the cluster which may take up to 5 minutes.

After creating and starting the cluster, and importing the script to your databricks account, you can assign that script to the cluster and press the button "Run All" to re-run the analysis yourself. It won't take more than 15 minutes to re-run everything inside the cluster provided for community databricks accounts.

## Analysis Results

The results of the analysis are being displayed on this <a href="https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/1536705237491348/498675988431179/6882450809162848/latest.html">link</a>.

## Replicate and Preproccess the dataset using databricks

The following script download the dataset from a public link and reupload them into my s3 bucket. At the same time, to simulate a real streaming data, the 2009 trips dataset was sorted and saved as individual records inside the same bucket. The script to do that can be imported through this <a href="https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/1536705237491348/3558946588555567/6882450809162848/latest.html">link.</a> <strong> Any change in this script will change the files inside the s3 bucket and may affect further analysis.</strong> 
This script does not set the newly uploaded data as public, this configuration will be added in the future and still need to be done manually.
