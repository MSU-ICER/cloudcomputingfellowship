---
title: 7 - AI APIs
---

# Azure AI Services and APIs
# ARCHIVE: see current website https://icer.msu.edu/cloud-computing

## What is AI? 

A discussion of AI and access to AI services in the cloud

 - What is AI? Definitions and impressions from the fellowship

    - What is Machine Learning? 

> For a classification task, say 2 class, training mathematical model input is the 
> features, output is the class.  Once the model knows what kind of features will predict 
> the classes (based on hand-labeled).  Train the model to predict the category of new data.   
> Unsupervised learning does not require pre-labelling, using clustering or other techniques 
> to identify the features for classification

 - How is AI different (if at all) from Machine Learning? 

> AI is deep learning with larger data sets, faster and more reliably.  
   
 - What are the essential ingredients to create an AI system?
 - What are the bias/issues with AI
 
Would AI as we see it today be possible without cloud computing?

 - Public AI vs Private AI: Google and Facebook have been working on this for a long time. 
 - 'Cloud' versus 'Internal'

## What is AI or ML? Services via functions

- AI like Machine Learning in the end is a function with inputs and outputs
    - Simple example: linear model from least squares ( aka regression)

## Azure AI use cases

*Class Discussion*

## Azure Cognitive Services

What are these services?   Massive machine learning models developed and trained by MS for public use

 - "AI Services" : https://learn.microsoft.com/en-us/azure/ai-services/
 - Vision: Image detection
    - Object Detection https://learn.microsoft.com/en-us/azure/ai-services/computer-vision/concept-object-detection-40
    - Use case: Deer census using camera traps : https://github.com/billspat/hpcc_megadetector

Standard Practice for engagine with Azure Cognitive/AI services: 

 1. create 'account' in your resource group
 2. open 'studio' 
 3. interact visually
 4. learn how to use API (python)
 5. create code and use personal keys

## OpenAI via Azure

- What is ChatGPT and how can it be used? 
- API Services
   - Exploring using the "OpenAI Studio"
   - Azure Service https://learn.microsoft.com/en-us/azure/ai-services/openai/
   - OpenAI Service: https://openai.com/product
   - Azure vs OpenAI


## Example of using OpenAI API 

Python Program pulled from several Azure Examples: 

Azure OpenAI Demo Script: https://github.com/billspat/azure_openai_demo


## Customizing your own AI

- What is Transfer Learning?
- Custom training from Azure , differentiating your AI.  

## Acceptable Use

We have an opportunity to use these tools as part of the fellowship via the MSU Azure acccount.   Please use these tools responsibly.  Please see the following policies

 - MSU Acceptable Use Policy: https://tech.msu.edu/about/guidelines-policies/aup/
 - Azure Responsible use of AI: https://learn.microsoft.com/en-us/azure/ai-services/responsible-use-of-ai-overview


