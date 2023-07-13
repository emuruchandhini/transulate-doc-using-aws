# S3 Translation Lambda

This script translates the text in a file stored in an Amazon S3 bucket using Amazon Translate. The translated text is then saved back to another S3 bucket.

## Prerequisites

- Python 3.x
- AWS account with appropriate permissions
- Boto3 library

## Installation

1. Clone the repository or download the code files.

2. Install the required dependencies by running the following command:

pip install boto3

## Setup

1. Set up AWS credentials by configuring the AWS CLI or using environment variables. Refer to the [AWS CLI Configuration] documentation for instructions.

2. Create two S3 buckets: one for input files and another for output files.

3. Configure the input S3 bucket to trigger an AWS Lambda function. Refer to the [Configuring Amazon S3 Event Notifications] documentation for instructions.

4. Update the `lambda_handler` function in the code to specify the target language code. Currently, it is set to 'bn' (Bengali). You can change it to your desired language code. Refer to the [Amazon Translate Language Codes](https://docs.aws.amazon.com/translate/latest/dg/what-is.html#what-is-languages) documentation for available language codes.

5. Deploy the code as an AWS Lambda function. You can use the AWS Management Console, AWS CLI, or AWS SDKs. Refer to the [AWS Lambda Developer Guide] for detailed instructions on creating and deploying Lambda functions.

## Usage

1. Upload a text file to the input S3 bucket. Make sure the bucket is configured to trigger the AWS Lambda function.

2. The Lambda function will automatically be triggered and execute the translation process.

3. The translated text will be saved to the output S3 bucket with the same file name.


