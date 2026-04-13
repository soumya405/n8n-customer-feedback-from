# n8n-customer-feedback-from
Purpose
The aim of this agent is to reduce manual work for the person responsible for handling customer feedback. It automatically analyzes feedback, categorizes it, and forwards it to the appropriate department, minimizing human effort and improving efficiency.

Success Criteria (How to Know It’s Working)
The agent will be considered successful if it reduces manual work by at least 30%. This can be measured by comparing the time and effort required before and after implementing the system.

Trigger
The agent is triggered when a user submits a feedback form. This submission acts as the starting point of the automation workflow.

Actions
Once triggered, the agent performs the following actions:

Analyze Feedback
The agent uses an LLM (Large Language Model) to understand the content and sentiment of the feedback.

Categorize Feedback
It classifies feedback into categories such as:

Complaint

Suggestion

Positive Feedback

Route to Department
Based on the category, the agent sends the feedback to the respective department via Slack.

Customer Response

If the feedback is negative or a complaint, the agent automatically sends a response email to the customer via Gmail.

If the feedback is positive, no response or a thank-you message can be sent.

Step-by-Step Workflow
A person fills out the feedback form.

The form data is sent to the automation agent.

The agent analyzes the feedback using an LLM.

The agent classifies the feedback into categories.

A Switch Node is used to route different categories:

Complaint → Support Team

Suggestion → Product Team

Positive → Marketing/Records

The feedback is stored in Airtable for tracking.

If required, an automatic email response is sent to the customer.

Tools Used
Slack → For sending feedback to specific departments

Airtable → For storing and managing feedback data

Gmail → For sending automated responses to customers

LLM (AI Model) → For analyzing and classifying feedback

Switch Node (n8n) → For routing logic based on feedback type
