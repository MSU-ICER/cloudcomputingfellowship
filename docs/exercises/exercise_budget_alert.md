---
title: Setting up Budget Alerts
---
# MSU Cloud Computing Fellowship: Costs and Budgets with Microsoft Azure
# ARCHIVE: see current website https://icer.msu.edu/cloud-computing

(Almost) everything you do in Azure has a cost, and costs for resources often acrue over time, wether the resource is in use or not.   This is a 
short excercise to recieve an email when you have spent a certain amount of money.   This can be valuable if you are experimenting and forget to 
delete a resource that you no longer need. 

For this work, You must first have a 'budget' in your resource group.  We created a budget for 2022 for all fellowship participants that you can use for creating alerts.  

If you have not yet, please go through the "Intro to the Azure portal" exercise for more context about what we are doing.   

### Background

See the "costs" section in the topics for details. 

In Azure you can set a 'budget' for a single resource (like a virtual machine), your whole resource group, or we could set on for the whole fellowship.    However setting a budget doesn't stop you from spending anything or invoke any action.  

Once you set a budget or maximum dollar amount you'd like to spend, you need to to then add either actions or alerts when some threshold within that budget is reached.  

We have set budgets for your resource group in the fellowship.  However you need to now set an alert to send you an email when you reach a spending amount.   You can set multiple alerts.  for example, we will set an alert when you reach a certain threshold.  

For details about this service, see the [Azure Cost Management + Billing documentation](https://learn.microsoft.com/en-us/azure/cost-management-billing/).   This specific exercise works with budgets and assumes there is one in your resource group.  If you do not have a budget on your account, or if you'd like to create a new kind of budget please contact us and we will assist you.  However if you are comfortable with Azure concepts, see this advanced [Azure Budget Tutorial

 https://learn.microsoft.com/en-us/azure/cost-management-billing/costs/tutorial-acm-create-budgets

### Steps to add a  "cost alert" to an existing budget your resource group.  

**Find the Premade Budget**

  - Log into https://portal.azure.com
  - You should see a single resource group, or be put into one automatically.  
  - Open your resource group if is not already
  - The left side bar had properties for the resource group. 
  - In the left side-bar, select "budgets" (scroll down)
  - You should see a single budget named with netid, like this "ccf23_sparty_budget"
  - Click on that budget
  - click 'edit budget' link near the top left
  - review the information

**Add an 'alert' to that budget**

  - in the edit budget form, 
  - alert condition: type = Actual
  - enter 50 percent
  - under action group, leave it as 'none' (alerts are different from actions)
  - in email, put your preferred email address (I don't know if gmail etc will work)
  - add a second email to inform the instructors for the cloud fellowship: billspat@msu.edu
  - select your preferred language, if it's available (the default is US English)
  - click 'Save'

You may add additional alerts if you want to be reminded at different thresholds of spending, e.g. 25%, 50%, 80%.   One advantage to setting a low threshold like 20% of your budget is to help you learn how much things cost or to be alerted if there are resources you've created but didn't realize they still existed or were costing anything.  

---

I hope these instructions were clear but again, any questions please contact us using email or MS Teams.  
