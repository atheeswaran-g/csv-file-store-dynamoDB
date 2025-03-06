# csv-file-store-dynamoDB
	Step 1: Set Up AWS Services
  	. Create an S3 Bucket
 	 .Go to the AWS S3 console and create a new bucket.
  	.Enable event notifications for the bucket to trigger a Lambda function when a new CSV file 
  	 isuploaded.
 	 .Create a DynamoDB Table
  	.Navigate to the AWS DynamoDB console and create a new table.
  	.Define the primary key (e.g., id) and any additional attributes based on your CSV data.
	-------------------------------------------------------------------------------
	Step 2: Create the AWS Lambda Function
  	.Go to the AWS Lambda Console
  	.Click on "Create Function" → Choose "Author from Scratch."
 	 .Choose a runtime (Python, Node.js, etc.)
  	.Assign the necessary IAM role with permissions to access S3 and DynamoDB.
    	Attach Necessary IAM Permissions
  	.Add the following permissions to the Lambda IAM role:
 	 	.AmazonS3ReadOnlyAccess (to read CSV files from S3)
  	.AmazonDynamoDBFullAccess (to write data to DynamoDB)
	-----------------------------------------------------------------------
	Step 3: Implement the Lambda Function
  	.Read the CSV file from S3
  	.Use boto3 in Python to fetch the file from S3.
  	.Parse the CSV File
  	.Read the file line by line and extract relevant data.
  	.Write Data to DynamoDB
  	.Insert each row into the DynamoDB table.
	============================================================================================
	Step 4: Configure S3 Event Trigger
  	.Go to the S3 Bucket → Click on "Properties."
  	.Create an Event Notification
  	.Select "All object create events" or specify .csv file uploads.
  	.Set the destination as your Lambda function.
	=============================================================================================
	Step 5: Deploy and Test
  	.Deploy the Lambda function.
  	.Upload a test CSV file to S3.
  	.Check DynamoDB to confirm the data was inserted.
  	.Monitor logs using AWS CloudWatch for debugging.
	========     ========    =======   =======   =======   ======  ======  ======  ======..


