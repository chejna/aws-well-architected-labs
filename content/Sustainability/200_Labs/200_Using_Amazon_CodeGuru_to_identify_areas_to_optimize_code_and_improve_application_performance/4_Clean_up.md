---
title: "Clean up"
date: 2021-05-31T11:16:08-04:00
chapter: false
pre: "<b>4. </b>"
weight: 4
---
The following steps will remove the services which are deployed in the lab.

### 1. Clean up all resources from the Lab

1. Navigate to the Lambda function we created and delete the "Lab-function" function.
![Section4 Picture1](/Sustainability/images/chejna-lab-pics/section4pic1.png)


2. Next, let's go to CodeGuru and delete the profiling group made for our Lambda function.
![Section4 Picture2](/Sustainability/images/chejna-lab-pics/section4pic2.png)


3. While still in CodeGuru, go to the Repositories section in the left panel and disassocite the "lab-repository" repository.
![Section4 Picture3](/Sustainability/images/chejna-lab-pics/section4pic3.png)
![Section4 Picture4](/Sustainability/images/chejna-lab-pics/section4pic4.png)


4. Move to IAM within the console and select Users in the left panel. Delete the "lab-user" user.
![Section4 Picture5](/Sustainability/images/chejna-lab-pics/section4pic5.png)
![Section4 Picture6](/Sustainability/images/chejna-lab-pics/section4pic6.png)


5. Lastly, search up Cloud9 and delete the "lab-environment" environment we created.
![Section4 Picture7](/Sustainability/images/chejna-lab-pics/section4pic7.png)
![Section4 Picture8](/Sustainability/images/chejna-lab-pics/section4pic8.png)
___
**END OF SECTION 4**
___
