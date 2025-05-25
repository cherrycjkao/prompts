# 📑 Support Use Case - Example Outputs

## How to use:
1. Copy the **Prompt** sections from `support_prompts/supportREADME.md` (excluding the **💡 Note** sections).  
2. Provide the required inputs (e.g., issue type, tool name, ticket priority) based on your case.  
3. Use the AI-generated output for ticket triage, response drafts, root cause summaries, customer satisfaction messages, or follow-up communications.

---

## Table of Contents:
1. [Diagnostic Prompt Example](#1-diagnostic-prompt-example)  
2. [Troubleshooting Prompt Example](#2-troubleshooting-prompt-example)  
3. [Workflow Structuring Prompt Example](#3-workflow-structuring-prompt-example)  
4. [Common Issues Prompt Example](#4-common-issues-prompt-example)  
5. [Customer Satisfaction Prompt Example](#5-customer-satisfaction-prompt-example)  
6. [Follow-Up Prompt Example](#6-follow-up-prompt-example)

---

> **💡 Note**:  
> - Each section shows one prompt’s **User Input** and a sample **🤖 AI Output**.  
> - Outputs are structured for clarity, brevity, and consistent tone.  
> - Mix and match examples to build multi-step workflows.

---

## 1. **Diagnostic Prompt Example**  
> For gathering detailed issue context

### 👤 User Input:
- Product Version: Web App v3.1
- Reported Behavior: User sees a blank page when accessing the Testing tab. No error message.
- Serial or License Number: ABC-1234
- Project Deadline: May 31, 2025
- Known Constraints (optional): User is on Chrome broswer on Windows 11

### 🤖 AI Output:
Thanks for providing those details. To help us pinpoint the root cause of the blank page on the Testing tab, here are a few follow-up questions:

Does the blank page appear every time you access the Testing tab, or does it happen only occasionally?

Have you tried accessing the Testing tab in a different browser (e.g., Edge or Firefox) or using Chrome in incognito mode? If so, does the issue still occur?

Was the Testing tab working previously, or is this your first time using it?

Have there been any recent changes to your account, settings, or application environment (e.g., browser extensions, network policies, app updates)?

Could you open the browser’s Developer Tools (F12), go to the Console tab, and let us know if there are any error messages or warnings displayed when you try to open the Testing tab?

Once we have these details, we can investigate more precisely.

↩️ [Back to Table of Contents](#table-of-contents)

---

## 2. **Troubleshooting Prompt Example**  
> For step-by-step resolution guidance

### 👤 User Input:
You need to write resolution steps for:
- **Issue Summary**: “504 gateway timeout when saving record”  
- **Environment**: Browser / Windows 10  
- **Steps Already Tried**: Cleared cache, logged out/in  
- **Technical Limitation**: No console access  
- **Tone**: Reassuring  

### 🤖 AI Output:
**🛠 Steps to Resolve**

1. Please retry saving the record after refreshing the page.  
2. If the error persists, open an Incognito window and attempt the same action.  
3. Still seeing the timeout? Clear your browser’s cookies for our domain and try again.  
4. If it still fails, share the exact timestamp and any on-screen messages.

✔️ *Let us know once step 3 is complete or if you encounter new errors.*

↩️ [Back to Table of Contents](#table-of-contents)

---

## 3. **Workflow Structuring Prompt Example**  
> For internal action planning

### 👤 User Input:
Generate an internal plan for:
- **Issue Type**: Permissions bug  
- **Dependencies**: IAM team, Database admins  
- **Ticket Priority**: Urgent  
- **Customer Sentiment**: Frustrated (VIP)  
- **Your Goal**: Triage & prepare escalation packet  

### 🤖 AI Output:
🧭 **Immediate Steps**  
- Reproduce permissions error using VIP user account.  
- Collect screenshots and API logs.

🔁 **Dependencies**  
- Loop in IAM team for policy review.  
- Notify DB admins to check ACL settings.

📌 **Documentation**  
- Add details to ticket #12345: user role, timestamps, error codes.

🎯 **Goal**  
- Confirm root cause & assemble escalation summary for Engineering within 1 hour.

↩️ [Back to Table of Contents](#table-of-contents)

---

## 4. **Common Issues Prompt Example**  
> For known-issue messages

### 👤 User Input:
Create a reusable response for:
- **Issue Title**: 500 error on payment update  
- **Root Cause**: backend rate-limiting  
- **ETA for Fix**: 4 hours  
- **Suggested Workaround**: retry after 15 minutes  
- **Tone**: Transparent  

### 🤖 AI Output:
Hi [Customer Name],

We’re aware of a 500 error affecting payment updates due to backend rate-limiting.

🔧 **Workaround**  
Please retry your update after 15 minutes.

🛠 **ETA for Fix**  
Our team is deploying a fix within the next 4 hours. We will notify you once it’s live.

Thank you for your patience!

↩️ [Back to Table of Contents](#table-of-contents)

---

## 5. **Customer Satisfaction Prompt Example**  
> For post-resolution feedback

### 👤 User Input:
Write a satisfaction message using:
- **Agent Name**: Alex  
- **Case ID**: 7890  
- **Outcome**: Resolved  
- **Preferred Tone**: Friendly  

### 🤖 AI Output:
Hi there,

Thanks for giving us the opportunity to help with your issue (Case #7890). I’m glad we could get everything resolved for you!

If you have a moment, would you mind sharing feedback on your experience? Your input helps us improve.

Cheers,  
Alex

↩️ [Back to Table of Contents](#table-of-contents)

---

## 6. **Follow-Up Prompt Example**  
> For proactive check-ins

### 👤 User Input:
Draft a follow-up for:
- **Customer Name**: Jamie  
- **Original Issue**: Login errors  
- **Last Action**: Fix deployed 2 days ago  
- **Next ETA**: Monitoring ongoing  
- **Ticket #**: 4567  

### 🤖 AI Output:
Hi Jamie,

Just checking in on Ticket #4567 regarding your login errors. We deployed a fix 2 days ago and are still monitoring performance.

Please let us know if you’re seeing any further issues—or if everything’s running smoothly—so we can close out your case.

Thanks again for your patience!

↩️ [Back to Table of Contents](#table-of-contents)
