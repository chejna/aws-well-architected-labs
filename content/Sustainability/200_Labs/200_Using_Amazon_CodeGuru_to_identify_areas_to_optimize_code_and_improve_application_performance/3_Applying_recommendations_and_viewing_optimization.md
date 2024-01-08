---
title: "Applying recommendations and viewing optimization"
date: 2021-05-31T11:16:08-04:00
chapter: false
pre: "<b>3. </b>"
weight: 3
---

### 3.1 Applying Recommendations 

1. Go back to the Lambda function and move the client creator line above the handler code
![Section3 Picture1](/Sustainability/images/chejna-lab-pics/section3pic1.png)
![Section3 Picture2](/Sustainability/images/chejna-lab-pics/section3pic2.png)

    Make sure to save, deploy, and test.

2. Wait around another 15+ minutes so CodeGuru Profiler can gather necessary data. Then go to the CodeGuru Profiler Group and look at the comparison of before and after the code change.

We can begin by looking at the client creator 
![Section3 Picture3](/Sustainability/images/chejna-lab-pics/section3pic3.png)
![Section3 Picture4](/Sustainability/images/chejna-lab-pics/section3pic4.png)

As you can see the ClientCreator:create_client initially showed 55.3% of total time and $64 per year

After the code change, it showed 39.6% of total time and $16 per year

This indicates a 15.7% decrease of total time and a $48 decrease per year


Next let's look at the lambda handler function
![Section3 Picture5](/Sustainability/images/chejna-lab-pics/section3pic5.png)
![Section3 Picture6](/Sustainability/images/chejna-lab-pics/section3pic6.png)

As you can see the lambda handler function initially showed 71.1% of total time and $83 per year

After the code change, it showed 74.5% of total time and $30 per year

This indicates a small 3.4% increase of total time but a significant $53 decrease per year



Lastly, let's look at the main function as a whole
![Section3 Picture7](/Sustainability/images/chejna-lab-pics/section3pic7.png)
![Section3 Picture8](/Sustainability/images/chejna-lab-pics/section3pic8.png)

As you can see the main function initially showed a cost of $116 per year

After the code change, it showed a cost of $41 per year

This indicates a significant $112 decrease per year

___
**END OF SECTION 3**
___

