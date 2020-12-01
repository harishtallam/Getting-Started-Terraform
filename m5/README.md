## Here, we will be using provisioners to perform post activities
Activities:
* Creation of S3 bucket
* IAM instance profile to access S3 bucket
* Provide permissions to S3 bucket to read files from EC2 instance
* Provide permissions to EC2 instance to write files to S3 bucket
* Upload files from EC2 instance to S3 bucket

## Commands to execute:
* "terraform init" - To initiate the configuration
* "terraform -out "m5.plan" - To generate the plan
* "terraform apply "m5.tfplan" - To apply the plan
