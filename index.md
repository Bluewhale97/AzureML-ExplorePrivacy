## Introduction

Data science projects often contain some sensitive details that should be kept private, which we think that we need to provide some privacy to control the access or constraints to them. 

In this article, we are going to discuss and deploy some assignments on how to protect our tasks through privacy deployment, avoiding fully explosuring our project to the public.

Specifically we will learn how to articulate the problem of data privacy, describe how differential privacy works, configure parameters for privacy and perfrom differentially private data analysis.

## Understanding differential privacy

Differential privacy serves to protect individual datums by adding statitsical "noise" to the analysis process. It ensures the data aggregations stay statisticaly consistent with the actual data alues allowing for some random variation but make it impossible to work out the individual values from the aggregated data. 

So noise can support for differential requirement of analysis.

One of ways that we can protect the personal data is "opt-out" option, meaning that the population will not attend in the study.

There are several considerations about opt-out, the first is that even you do opt out on a study, its production finally also is possible to affect you by another side that change, if the study finds a correlation between the features that you opt-in, your "label" will be changed.

We cannot predict the impact of choosing opt-in and opt-out and even sometimes opt-in could be better, means that participation can benifit more than negative impact. 

As tutorial said, the only way for the opt-out option to work for every individual, is for every individual not to take part – which makes the whole study pointless!

The amount of variation cause by noise increments is configurable through a parameter called epsilon. This value governs the amount of additional risk that your personal data can be identified through rejecting the opt-out option and participating in a study. The key thing is that it applies this privacy principle for everyone participating in the study. A low epsilon value provides the most privacy, at the expense of less accuracy when aggregating the data. A higher epsilon value results in aggregations that are more true to the actual data distribution, but in which the individual contribution of a single individual to the aggregated value is less obscured by noise.

![image](https://user-images.githubusercontent.com/71245576/116628266-bc675880-a91c-11eb-84c5-7b1da8a97695.png)


## Reference

Build AI solutions with Azure Machine Learning, retrieved from https://docs.microsoft.com/en-us/learn/paths/build-ai-solutions-with-azure-ml-service/

