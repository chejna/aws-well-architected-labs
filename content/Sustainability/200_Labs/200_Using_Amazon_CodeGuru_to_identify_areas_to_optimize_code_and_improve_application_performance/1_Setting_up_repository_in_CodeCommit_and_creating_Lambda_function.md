---
title: "Setting up repository in CodeCommit and creating Lambda function"
date: 2021-05-31T11:16:08-04:00
chapter: false
pre: "<b>1. </b>"
weight: 1
---

### 1.1. Setting up a Repository in CodeCommit

You will start by setting up a code repository in CodeCommit.

1. Within the console, search up CodeCommit and enter the CodeCommit console. While in the Repositories section, click on Create repository

![Section1 Picture1](/Sustainability/images/chejna-lab-pics/section1pic1.png)

2. On the Create repository page, name the repository “lab-repository”.
Check the box labeled "Enable Amazon CodeGuru Reviewer for Java and Python".
Click Create.
![Section1 Picture2](/Sustainability/images/chejna-lab-pics/section1pic2.png)

3. While in lab-repository, press upload file and upload a file with the code below.
```
#invocation code
import json
import boto3
from codeguru_profiler_agent import with_lambda_profiler

#handler code
def lambda_handler(event, context):
  client = boto3.client('dynamodb')
  #simple codeblock for demonstration purposes  
  output = 'Hello World'
  print(output)
  #handler function return

  return output
```
![Section1 Picture18](/Sustainability/images/chejna-lab-pics/section1pic18.png)

    Add Author name and Email address and press Commit changes
![Section1 Picture19](/Sustainability/images/chejna-lab-pics/section1pic19.png)

3. Within the console, search up IAM and enter the IAM console. In the left panel, click on Users. Once in the Users section, click Create User
![Section1 Picture3](/Sustainability/images/chejna-lab-pics/section1pic3.png)

4. Name the user "lab-user" and click Next.
![Section1 Picture4](/Sustainability/images/chejna-lab-pics/section1pic4.png)

5. Under Permissions options, check the Attach policies directly box. In the list of Permission policies, type in AWSCodeCommitPowerUser and select the Policy that shows. Click next, leave everything as default, and create the user.
![Section1 Picture5](/Sustainability/images/chejna-lab-pics/section1pic5.png)

6. In the Users section within IAM click on the lab-user we just created and specifically move to the Security credentials tab. 
![Section1 Picture6](/Sustainability/images/chejna-lab-pics/section1pic6.png)

Within the Security credentials tab, scroll down to the section labeled HTTPS Git credentials for AWS CodeCommit and click Generate credentials.

![Section1 Picture7](/Sustainability/images/chejna-lab-pics/section1pic7.png)

7. A pop-up with a username and password will appear. Make sure to note these credentials separately for future use!
![Section1 Picture8](/Sustainability/images/chejna-lab-pics/section1pic8.png)
![Section1 Picture9](/Sustainability/images/chejna-lab-pics/section1pic9.png)

### 1.2. Creating a Lambda Function

Next we will, create a Lambda function for CodeGuru Profiler to analyze

1. Within the console, search up Lambda and click into the Lambda console. While in the Functions section, click on Create function.
![Section1 Picture10](/Sustainability/images/chejna-lab-pics/section1pic10.png)


2. Remain in the Author from scratch tab and name the function “Lab-function”. Select Python 3.9 under runtime and leave x86_64 checked under Architecture. Expand Advanced Settings and check Enable function URL, then specify AWS_IAM under Auth type (leave everything else as default). 
![Section1 Picture11](/Sustainability/images/chejna-lab-pics/section1pic11.png)
![Section1 Picture12](/Sustainability/images/chejna-lab-pics/section1pic12.png)

3. Click Create function and in the code editor tab, copy and paste the following code (Make sure that all indentations are accurate). Save, Deploy, and Test the code.
```
#invocation code
import json
import boto3
from codeguru_profiler_agent import with_lambda_profiler

#handler code
def lambda_handler(event, context):
  client = boto3.client('dynamodb')
  #simple codeblock for demonstration purposes  
  output = 'Hello World'
  print(output)
  #handler function return

  return output
```
![Section1 Picture13](/Sustainability/images/chejna-lab-pics/section1pic13.png)

4. Click into the Configuration tab, and select Monitoring and operations tools in the left side panel and in the top right click Edit.
![Section1 Picture14](/Sustainability/images/chejna-lab-pics/section1pic14.png)

    At the bottom of the Edit Monitoring tools page, check the Code Profiling button within the Amazon CodeGuru Profiler section, then click Save.

![Section1 Picture15](/Sustainability/images/chejna-lab-pics/section1pic15.png)
___
**END OF SECTION 1**
___
