# Create-Lambda-function-to-automate-S3-file-processing.


## Full  Step-by-Step guide with snapshots to describe and illustrate how to create a Lambda function to automate S3 file processing.

### This project demonstrates how to create a Lambda function to automate S3 file processing.

* Create an S3 Bucket

* Upload a test object to your bucket.

* Create an IAM policy that lets Lambda read from S3 and write logs to Cloudwatch.

#### Step-by-Step Instructions on how to create a Lambda function to automate S3 file processing.
UPLOAD FILE TO S3 BUCKET
*Type & Select S3 from the Amazon Search Bar.

* Select Create Bucket.

* Select General Purpose for your Bucket and Give Your Bucket a name.

* Select the bucket that you just created.

* Select the Upload Button.

* Select the add files button and additionally select the file that you want to upload.

* Select Upload at the bottom.


CREATE IAM POLICY & ROLE TO ALLOW LAMBDA TO GET OBJECTS FROM AN S3 BUCKET AND TO WRITE TO AMAZON CLOUD WATCH


* Search and select IAM from the AWS search bar

* Select Policies from the left-hand options bar. 

* Select Create Policy Button.

* Select the JSON Tab.

* Paste the below JSON Policy into the JSON Policy Editor.

*Click Next at the bottom of the page.

* Give your policy a name.

* Select Create Policy at the bottom of the page.

* Select Roles from the left-handed options bar

* Click Create Role

* Select AWS service as the trusted entity type.

* Select Lambda for the roles use case.

* Select Next at the bottom of the select trusted entity page.

* In the search box, type the policy that was created earlier and select it.

* Select Next at the bottom of the add permissions page.

* Give your Role a Name.

* Select Create Role at the bottom of the page.





##### Contribution Policy

This project is not accepting external contributions, including pull requests or feature requests.

It serves as a personal archive of my learning journey in applying foundational concepts in software development and version control. Active development is not ongoing, and external changes will not be integrated.

Thank you for your understanding.
