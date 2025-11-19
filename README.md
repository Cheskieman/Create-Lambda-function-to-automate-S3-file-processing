# Create-Lambda-function-to-automate-S3-file-processing.


## Full  Step-by-Step guide with snapshots to describe and illustrate how to create a Lambda function to automate S3 file processing.

### This project demonstrates how to create a Lambda function to automate S3 file processing.

* Create an S3 Bucket  

* Upload a test object to your bucket.

* Create an IAM policy & role that lets Lambda read from S3 and write logs to CloudWatch.

* Create and deploy a Lambda Function to be triggered when objects are uploaded to the S3 Bucket.

 

#### Step-by-Step Instructions on how to create a Lambda function to automate S3 file processing.
UPLOAD FILE TO S3 BUCKET
*Type & Select S3 from the AWS Search Bar.
<p align="center">  
  <img src="resources/S3 Search AWS Search Bar s3.png" alt="Select S3 from AWS Search Bar" />  
</p>  
* Select Create Bucket.
  <p align="center">  
  <img src="resources/S3 Select Create Bucket Initial.png" alt="Create an S3 Bucket" width="900" />  
</p
* Select General Purpose for your Bucket and Give Your Bucket a name.
<p align="center">  
  <img src="resources/s3 general configuration s3 info.png" alt="Select General Purpose & Give Bucket a Name" width="900" />  
</p>  
* Select the bucket that you just created.
<p align="center">  
  <img src="resources/S3 Select rececntly cereated bucket.png" alt="Select Recently Created Bucket" width="900" />  
</p>  
* Select the Upload Button.
<p align="center">  
  <img src="resources/S3 upload file to s3 buxket initial.png" alt="Select Initial Upload Bucket" width="900" />  
</p>  
* Select the add files button and additionally select the file that you want to upload.
<p align="center">  
  <img src="resources/S3 select add files button .png" alt="Select the Add Files Button" width="900" />  
</p>  
* Select Upload at the bottom.
<p align="center">  
  <img src="resources/s3 select the upload button end.png" alt="Select at Bottom Upload Button." width="900" />  
</p>  

CREATE IAM POLICY & ROLE TO ALLOW LAMBDA TO GET OBJECTS FROM AN S3 BUCKET AND TO WRITE TO AMAZON CLOUDWATCH


* Search and select IAM from the AWS search bar
<p align="center">  
  <img src="resources/IAM Select iam from aws search bar.png" alt=" Select IAM from AWS Searchbar" width="900" />  
</p>  
* Select Policies from the left-hand options bar. 
<p align="center">  
  <img src="resources/iam select policies from left handed options.png" alt="Select Policies from left hand options." width="900" />  
</p>  
* Select the Create Policy Button.
<p align="center">  
  <img src="resources/IAM Select Create Policy button initial.png" alt="Select the intial Create Policy Button." width="900" />  
</p>  
* Select the JSON Tab.
<p align="center">  
  <img src="resources/IAM select the JSON TAB .png" alt="Select the JSON Policy Tab" width="900" />  
</p>  
* Paste the below JSON Policy into the JSON Policy Editor.
<p align="center">  
  <img src="resources/IAM Actual JSON Policy.png" alt="Actual JSON Policy" width="900" />  
</p>  
*Select Next at the bottom of the page.
<p align="center">  
  <img src="resources/IAM Click the next button bottom JSON Polcy Editor Page.png" alt=" Select Next at the Bottom of the page" width="900" />  
</p>  
* Give your policy a name.
<p align="center">  
  <img src="resources/IAM Give Policy Name .png" alt=" Give your Policy a name." width="900" />  
</p>  
* Select Create Policy at the bottom of the page.
<p align="center">  
  <img src="resources/IAM create policy button end.png" alt=" Select Create Policy at bottom of page" width="900" />  
</p>  
* Select Roles from the left-handed options bar
<p align="center">  
  <img src="resources/ROLES Select Roles from left handed options.png" alt=" Select Roles from left-handed-options" width="900" />  
</p>  
* Click Create Role
<p align="center">  
  <img src="resources/ROLES Click Create Role Button initial.png" alt=" Select Inital Create Role" width="900" />  
</p>  
* Select AWS service as the trusted entity type.
<p align="center">  
  <img src="resources/ROLES Select Trusted Entity for Role.png" alt=" Select Trusted Entity" width="900" />  
</p>  
* Select Lambda for the roles use case.
<p align="center">  
  <img src="resources/AWS Select Lambda as Use Case for role.png" alt=" Select Lambda as Use Case" width="900" />  
</p>  
* Select Next at the bottom of the select trusted entity page.
<p align="center">  
  <img src="resources/ROLE Click Next bottom of Select trusted entity page .png" alt=" Select Next bottom of page" width="900" />  
</p>  
* In the search box, type the policy that was created earlier and select it.
<p align="center">  
  <img src="resources/ROLE Search and Select policy created earlier.png" alt=" Select Policy Created Earlier" width="900" />  
</p>  
* Select Next at the bottom of the add permissions page.
<p align="center">  
  <img src="resources/ROLES Select Next add permissions page.png" alt=" Select Next Bottom of Permissions Page" width="900" />  
</p>  
* Give your Role a Name.
<p align="center">  
  <img src="resources/ROLES give your role a name.png" alt=" Give Role a Name" width="900" />  
</p>  
* Select the Create Role button at the bottom of the page.
<p align="center">  
  <img src="resources/ROLES Click Create Role Button initial.png" alt=" Select Create Role" width="900" />  
</p>  

CREATING A LAMBDA FUNCTION:

* Search and select Lambda from the AWS search bar
<p align="center">  
  <img src="resources/LAMBDA Select Lamabda from AWS Search bar.png" alt=" Select Lambda from AWS Searchbar " width="900" />  
</p>  

* Select Create Function
<p align="center">  
  <img src="resources/LAMBDA Select create function initial.png" alt=" Select Create Function" width="900" />  
</p>  
 

* Give your function a name.
<p align="center">  
  <img src="resources/LAMBDA give your function a name.png" alt=" Give your function a name" width="900" />  
</p>  

* Select Python 3.13 from the runtime dialog box.
<p align="center">  
  <img src="resources/LAMBDA choose python as runtime.png" alt=" Choose Python as runtime" width="900" />  
</p>  

* Select X86_64 from architecture.
<p align="center">  
  <img src="resources/LAMBDA choose architecture.png" alt=" Select Architecture" width="900" />  
</p>  

* Select Use an existing role from the Change default execution role section.
<p align="center">  
  <img src="resources/LAMBDA choose use an existing role.png" alt=" Select Use an Existing Role" width="900" />  
</p>  

* Select the role you created earlier as the existing role.
<p align="center">  
  <img src="resources/LAMBDA Select the existing role created earlier.png" alt=" Select Create Role" width="900" />  
</p>  

* Select the Create Function button at the bottom.
<p align="center">  
  <img src="resources/LAMBDA Select the Create Function button end.png" alt="Select Create Function button" width="900" />  
</p>  

* Select the Function recently created.
<p align="center">  
  <img src="resources/LAMBDA Select the Function just created.png" alt=" Select Function Recently Created." width="900" />  
</p>  

* In the code source, paste the below Python code into the Lambda Code Editor Box.
<p align="center">  
  <img src="resources/lambda python code .png" alt="Python Code" width="900" />  
</p>  

* Select Deploy from the Deploy Section.
<p align="center">  
  <img src="resources/LAMBDA Select Deploy .png" alt=" Select Deploy" width="900" />  
</p>  


CREATING AN AMAZON S3 TRIGGER EVENT NOTIFICATION USING LAMBDA
  
* Type & Select S3 from the Amazon Search Bar.
<p align="center">  
  <img src="resources/S3 Search AWS Search Bar s3.png" alt=" Select S3 Bucket from AWS Searchbar" width="900" />  
</p>  

* Select the Bucket that was created earlier.
<p align="center">  
  <img src="resources/BACKINS3 select the earlier created bucket.png" alt=" Select earlier created bucket." width="900" />  
</p>  

* Select the Properties Tab.
 <p align="center">  
  <img src="resources/BACKINS3select the properties tab.png" alt=" Select Properties Tab" width="900" />  

 * Scroll down to Event Notification and select Create Event Notification.
<p align="center">  
  <img src="resources/BACKINS3CLICKCREATEEVENTNOTIFICATION.png" alt=" Select Deploy" width="900" />  

 * Select the checkbox that says all objects create events in the events type section.
<p align="center">  
  <img src="resources/BACKINS3CLICKCREATEEVENTNOTIFICATION.png" alt=" Select Deploy" width="900" />  

 * Select the Lambda Function that was created earlier from the Lambda Function dropdown box.
<p align="center">  
  <img src="resources/backins3 select lambda function created earlier.png" alt=" Select Lambda Function Created Earlier" width="900" />  

 * Select Save Changes at the bottom of the page.
<p align="center">  
  <img src="resources/BACKINS3 select save changes.png" alt=" Save Changes at the bottom of the page." width="900" />  

TEST THE LAMBDA FUNCTION USING A DUMMY EVENT

* Search and select Lambda from the AWS search bar
<p align="center">  
  <img src="resources/LAMBDA Select Lamabda from AWS Search bar.png" alt=" Save Changes at the bottom of the page." width="900" />  

 * Select the earlier created Lambda Function.

<p align="center">  
  <img src="resources/TESTYOURLAMBDAFUNCTION select earlier created function.png" alt=" Select the earlier created Lambda Function." width="900" />  

* Select Test from the options.

<p align="center">  
  <img src="resources/TESTYOURLAMBDAFUNCTION select test from options.png" alt=" Select test from options." width="900" />  

* Scroll down and give your test a name in the Event Name box.

  <p align="center">  
  <img src="resources/TESTYOURLAMBDAFUNCTION give event name name.png" alt=" Give your test a name." width="900" />  

 * Paste the below Test Event JSON Policy into the Event JSON Policy Editor. Replace the following values:

   * Replace us-east-1 with the region where you are located.
   * Replace upload-trigger-bucket1 with the name of the S3 Bucket that you created.
   * Replace happyface.jpg with the name of the test object that you created.
  
      <p align="center">  
  <img src="resources/TESTYOURLAMBDAFUNCTION paste code into JSON for testing.png" alt=" Test JSON Policy." width="900" />   

  * Select the Save button when you scroll up.

   <p align="center">  
  <img src="resources/TESTYOURLAMBDAFUNCTION click save button.png" alt=" Click Save" width="900" />  
  
  * Select the Test button that is directly to the right of Save.
  <p align="center">  
  <img src="resources/TESTYOURLAMBDAFUNCTION click TEST button.png" alt=" Select the Test Button." width="900" />  

TEST THE LAMBDA FUNCTION WITH THE AMAZON S3 TRIGGER

* Type & Select S3 from the AWS Search Bar.
  <p align="center">  
  <img src="resources/S3 Search AWS Search Bar s3.png" alt=" Search and Select S3 ." width="900" />  

* Select the Bucket that was created earlier.
  <p align="center">  
  <img src="resources/BACKINS3 select the earlier created bucket.png" alt=" Select the S3 Bucket created earlier." width="900" />  

* Select the Upload Button
  <p align="center">  
  <img src="resources/s3 select the upload button end.png" alt=" Select the Upload Bucket." width="900" />  

* Select the add files button and additionally select the file that you want to upload.
  <p align="center">  
  <img src="resources/S3 select add files button .png" alt=" Select the Add Files Button." width="900" />  

*  Select Upload at the bottom.
  <p align="center">  
  <img src="resources/TESTYOURLAMBDAFUNCTION click TEST button.png" alt=" Select the Test Button." width="900" />  

VERIFY THE FUNCTION WAS TRIIGERED USING CLOUDWATCH LOGS

*  Search and select CloudWatch from the AWS search bar.

*  Select Log groups under logs on the left-hand side of the page.

*  Select the log group for your function by clicking on it

*  Select the most recent log stream.

* If the function was triggered correctly, the log stream will look something similar to below photo.
      




* Select the Lambda Function
<p align="center">  
  <img src="" alt=" Select Create Role" width="900" />  
</p> 


##### Contribution Policy

This project is not accepting external contributions, including pull requests or feature requests.

It serves as a personal archive of my learning journey in applying foundational concepts in software development and version control. Active development is not ongoing, and external changes will not be integrated.

Thank you for your understanding.
