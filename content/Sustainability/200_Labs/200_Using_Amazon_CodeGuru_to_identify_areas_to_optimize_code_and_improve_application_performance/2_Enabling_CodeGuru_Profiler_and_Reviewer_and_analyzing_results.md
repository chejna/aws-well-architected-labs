---
title: "Enabling CodeGuru Profiler and Reviewer and analyzing results"
date: 2021-05-31T11:16:08-04:00
chapter: false
pre: "<b>2. </b>"
weight: 2
---

Well-Architected Insights provides serverless developers with insights and recommendations to continually improve their applications and keep them secure, compliant, optimized, and efficient.

The second section of the lab will demonstrate how to automatically create a role in your AWS account, delegating read-only access to various services in your AWS account. Follow these steps to complete the configuration:

### 2.1. CodeGuru Profiler and Cloud9

1. Within the console, navigate to Amazon Cloud9 and click on Create Environment
![Section2 Picture1](/Sustainability/images/chejna-lab-pics/section2pic1.png)
    
    Once the Environment is created, under the column labeled Cloud9IDE, press the Open button
![Section2 Picture2](/Sustainability/images/chejna-lab-pics/section2pic2.png)

2. Retrieve the function URL from your lambda function and run the following command in the Cloud9 terminal
```
while true; do curl {Lambda Function URL}; sleep 0.06; done
```

3. Wait ~15 minutes for results to be generated and for the profiling group to generate and show up within the Profiling group page in the CodeGuru Profiler console. Once it appears, follow the instructions of setup for results to show.
![Section2 Picture3](/Sustainability/images/chejna-lab-pics/section2pic3.png)
    Add appropriate role and code
![Section2 Picture4](/Sustainability/images/chejna-lab-pics/section2pic4.png)

4. Once the Profiling Group gathers everything necessary, look towards the Recommendations section and see the recommendations CodeGuru has suggested.
![Section2 Picture5](/Sustainability/images/chejna-lab-pics/section2pic5.png)

    In the recommendations, it tells us we are unnecessarily creating a client every time so in the next section we will look to fix that!

    
### 2.2. CodeGuru Reviewer

1. In the CodeGuru console, navigate to the Code Reviews section in the left panel. Click on Create full repository analysis
![Section2 Picture6](/Sustainability/images/chejna-lab-pics/section2pic6.png)

    Note that the full analysis will take around 5-10 minutes
![Section2 Picture7](/Sustainability/images/chejna-lab-pics/section2pic7.png)

2. Once the analysis has completed we can go in and see the recommendation provided to us
![Section2 Picture8](/Sustainability/images/chejna-lab-pics/section2pic8.png)

    Similar to the CodeGuru Profiler Recommendations, this tells us that we are unnecessarily creating clients

___
**END OF SECTION 2**
___
