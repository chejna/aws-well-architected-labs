---
title: "Level 200: Using Amazon CodeGuru to identify areas to optimize code and improve application performance"
menutitle: "Level 200: Using Amazon CodeGuru to identify areas to optimize code and improve application performance"
date: 2021-05-31T11:16:08-04:00
chapter: false
weight: 2
---

## Authors

* **Jonathan Chen**, Partner Solutions Architect


## Introduction

Within every application is the code that allows it to perform specified actions. Often, companies develop software workflows and perform code reviews (sometimes manually) to keep thousands to millions lines of code organized. This can require a lot of bandwidth and difficult overall to maintain. This remains a significant responsibility as this can directly affect a company’s success, performance, and overall cost to function.

With this in mind, having the most optimal code can be essential from a sustainability, performance, and financial perspective. If your code performs the same actions with less CPU utilization, your cloud emissions decrease, your performance increases, and your costs lower. However, in most cases, finding those areas to optimize code can prove to be quite difficult as it requires testing, expertise, etc. 

Amazon CodeGuru Profiler solves this issue as it collects runtime performance from your live applications and provides recommendations that can help fine-tune your application performance. Using machine learning algorithms, CodeGuru Profiler can help you find your most expensive lines of code and suggest ways you can improve efficiency and remove CPU bottlenecks. CodeGuru Profiler provides different visualizations of profiling data to help you identify what code is running on the CPU, see how much time is consumed, and suggest ways to reduce CPU utilization.

Additionally Amazon CodeGuru Reviewer uses program analysis and machine learning to detect potential defects that are difficult for developers to find and offers suggestions for improving your Java and Python code. By proactively detecting code defects, CodeGuru Reviewer can provide guidelines for addressing them and implementing best practices to improve the overall quality and maintainability of your code base during the code review stage. CodeGuru Reviewer doesn't flag syntactical mistakes, as these are relatively easy to find. Instead, CodeGuru Reviewer identifies more complex problems and suggests improvements related to recommendation types such as resource leak prevention or security analysis. Within each type are several detectors that CodeGuru Reviewer uses to analyze your code.  It makes it much simpler to do analyses as a whole on repositories, something that many companies use to make changes to code.

In this lab, you will optimize application code through using the following AWS services:

* [AWS CodeCommit](https://docs.aws.amazon.com/govcloud-us/latest/UserGuide/govcloud-acc.html) - Used for hosting repository.
* [Amazon CodeGuru Profiler](https://docs.aws.amazon.com/codeguru/latest/profiler-ug/what-is-codeguru-profiler.html) - Used to analyze Lambda function and provide recommendations.
* [Amazon CodeGuru Reviewer](https://docs.aws.amazon.com/codeguru/latest/reviewer-ug/welcome.html) - Used for performing analyses on repositories.
* [AWS Lambda](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html) - Used to run code without provisioning.
* [Amazon Identity and Access Management](https://docs.aws.amazon.com/iam/) - Used for securely controlling access to AWS services

Our lab is divided into several sections as follows:

1. Setting up repository in CodeCommit and creating Lambda function
2. Enabling CodeGuru Profiler and Reviewer and analyzing results
3. Applying recommendations and viewing optimization
4. Clean up

## Prerequisites

* An [AWS account](https://portal.aws.amazon.com/gp/aws/developer/registration/index.html) that you are able to use for testing, that is not used for production or other purposes.

{{% notice note %}}
**NOTE:** You will be billed for any applicable AWS resources used if you complete this lab that are not covered in the [AWS Free Tier](https://aws.amazon.com/free/).
{{% /notice %}}

## Steps:

{{% children /%}}
