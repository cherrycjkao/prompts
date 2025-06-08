# 📑 Support Use Case - Example Outputs

## How to use:
1. Copy the **Prompt** sections from `SaaS-Customer-Support-Tier-2/README.md` (excluding the **💡 Note** sections).  
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
- Serial or License Number: ABC-1234
- Reported Behavior: User sees a blank page when accessing the Testing tab. No error message.
- Steps Taken Before the Issue Occurred: Clicked “Start” button in left panel from Testing window
- Customer Environment: Chrome broswer on Windows 11
- Recent Changes: Windows update
- Scope and Impact: Only appears with office network, it works fine with personal network at home.
- Project Deadline: May 31, 2025
- Known Constraints (optional): User is on Chrome broswer on Windows 11

### 🤖 AI Output:
Thanks for providing those details. Based on what you've shared, here are a few questions to help us narrow down the root cause:
- Are there any browser console errors or blocked requests shown in the Network tab of Chrome’s Developer Tools when the Testing tab loads on the office network?
(This can help identify if certain scripts or resources are being blocked.)
- Is your office network using a firewall, proxy, or VPN that might restrict specific domains or ports?
(These often interfere with web apps depending on their configuration.)
- Have you recently cleared your browser cache or tried accessing the Testing tab in Incognito mode while on the office network?
(This can rule out browser-side caching or extension conflicts.)
- Do other colleagues on the same office network experience the same issue when accessing the Testing tab?
(This helps determine if it’s a device-specific or network-wide issue.)
- Does the issue still occur when temporarily disabling any antivirus or endpoint security software running on your office machine?
(Some security tools can block scripts or web requests silently.)

Let me know what you find from the above, and we’ll go from there.

↩️ [Back to Table of Contents](#table-of-contents)

---

## 2. **Troubleshooting Prompt Example**  
> For step-by-step resolution guidance

### 👤 User Input:
- **Issue Summary**: User sees a blank page when accessing the Testing tab. No error message. 
- **Environment**: Chrome broswer on Windows 11 + Product Version - Web App v3.1
- **Steps Already Tried**: Reboot PC doesn't work, flushed DNS also doesn't work either. 
- **Known Constraints**: User is on Chrome broswer on Windows 11, the issue only appears with office network, it works fine with personal network at home.

### 🤖 AI Output:
### 🔧 Step-by-Step Troubleshooting

1. ### ✅ **Confirm Chrome Version Is Up-to-Date**
   - Navigate to: `Chrome Menu (⋮)` → *Help* → *About Google Chrome*
   - **Expected**: Version is current (v124 or newer)
   - ⛔ **If outdated**: Update Chrome and restart before retesting  
   - ➡️ **If up-to-date**: Proceed to Step 2

---

2. ### 🕵️ **Test in Incognito Mode**
   - Open a new Incognito window: `Ctrl + Shift + N`
   - Visit the Testing tab directly
   - ✅ **If it loads**: Suggests browser extensions or cache are interfering → proceed to Step 3  
   - ⛔ **If still blank**: Skip to Step 4

---

3. ### ♻️ **Clear Browser Cache & Cookies**
   - Press `Ctrl + Shift + Del` → Time range: **All Time**
   - Check: `Cookies and other site data` + `Cached images and files` → Click **Clear Data**
   - Reload the Testing tab
   - ✅ **Expected**: Page should now render correctly  
   - ⛔ **If not resolved**: Proceed to Step 4

---

4. ### 🧪 **Check for Blocked Scripts via DevTools (if available)**
   - Press `F12` or `Right-click` → *Inspect* → Go to **Console** and **Network** tabs
   - Reload the Testing tab  
   - Look for errors like:
     - `net::ERR_BLOCKED_BY_CLIENT`
     - `403 Forbidden`, `404 Not Found`
     - `CORS` or `Mixed Content` issues  
   - 📝 **If blocked URLs are identified**: Note the domains → Go to Step 6

---

5. ### 🌐 **Manually Test CDN Access**
   - In a new tab, open this test URL:  
     `https://cdn.jsdelivr.net/npm/vue@2/dist/vue.min.js`  
   - ✅ **If accessible**: CDN access is allowed  
   - ⛔ **If blocked or failed to load**: Suggests office network restrictions → Continue to Step 6

---

6. ### 🔒 **Check Proxy, Firewall, or VPN Settings**
   - Navigate to: `Chrome Settings` → *System* → *Open your computer’s proxy settings*
   - Temporarily **disable proxy configuration** or disconnect from **VPN**
   - Retry the Testing tab
   - ✅ **If resolved**: Network policy is blocking resources → escalate to IT for whitelisting
   - ⛔ **If no change**: Proceed to Step 7

---

7. ### 🧭 **Compare DNS Resolution**
   - Open Command Prompt → Run:
     ```bash
     nslookup yourwebapp.com
     ```
   - Compare IP addresses on **office** vs **home** network  
   - 📝 **If IPs differ or fail to resolve**: Office DNS may be intercepting requests → Escalate to IT

---

8. ### 🧪 **Test with Another Device on the Same Network**
   - Ask a colleague using the same network to access the Testing tab
   - ✅ **If they also experience it**: Confirms network-wide issue  
   - ⛔ **If it works for them**: Likely device-specific → investigate antivirus or endpoint security software

---

### 🔄 Rollback Guidance

- **Browser Settings**: If proxy or VPN settings were changed, revert by:
  - Chrome → Settings → *System* → Restore automatic proxy config
- **Antivirus/Firewall**: Re-enable any security software temporarily disabled for testing
- **Browser Cache**: No rollback needed, but user may need to log in again

---

### ✅ Verification Steps

After applying the above fixes:
1. Access the **Testing tab** via Chrome on the office network
2. Confirm:
   - The page fully renders
   - No blank sections or persistent loading
   - No errors in Chrome DevTools Console or Network tab

---

### 📩 Escalation Criteria

If unresolved after completing all steps, please gather the following for Tier 3 escalation:
- Screenshot of Chrome Console or Network tab showing any errors
- List of blocked domains (if identified)
- DNS resolution output (`nslookup`) from office network
- Confirmation of whether a proxy, VPN, or firewall is used

↩️ [Back to Table of Contents](#table-of-contents)

---

## 3. **Workflow Structuring Prompt Example**  
> For internal action planning

### 👤 User Input:
- **Issue Type**: Data sync error 
- **Brief Description**: User sees a blank page when accessing the Testing tab. No error message.  
- **Dependencies**: Backend service, IT, Infrastructure  
- **Ticket Priority**: Medium
- **Customer Sentiment**: Frustrated
- **Your Goal**: Escalate to engineering

### 🤖 AI Output:
🧭 **Immediate Steps**
1. **Action**: Attempt to replicate the blank page issue on the Testing tab in a controlled environment (staging), mimicking the customer environment (Chrome on Windows 11, office network conditions if possible).  
   - **Responsibility**: Tier 2 Support Agent  
   - **Expected Outcome**: Confirm if the blank page appears under the same conditions as the customer’s environment.  

2. **Action**: Collect relevant logs from backend services, frontend console logs (including browser dev tools output), and infrastructure monitoring related to the Testing tab access during replication attempts.  
   - **Responsibility**: Tier 2 Support Agent with support from Infrastructure and Backend teams  
   - **Expected Outcome**: Gather diagnostic data to identify any silent failures, blocked requests, or service disruptions causing the blank page.  

3. **Action**: Notify IT and Infrastructure teams about the issue to verify if there are ongoing incidents, firewall/proxy rules, or resource constraints impacting the Testing tab functionality, especially related to office network conditions.  
   - **Responsibility**: Tier 2 Support Agent  
   - **Expected Outcome**: Determine if dependency services and network components are healthy or require intervention.  

4. **Action**: Prepare and package all replication steps, logs, screenshots, and customer impact details into an escalation document to send to engineering.  
   - **Responsibility**: Tier 2 Support Agent  
   - **Expected Outcome**: Engineering team receives full context and can begin an in-depth investigation without delay.  

#### 🗒 Internal Notes to Document:  
- Detailed replication attempts and environment specifics (browser version, OS, network type)  
- Collected frontend and backend logs, screenshots of blank page behavior  
- Notation of customer frustration and elevated urgency despite Medium priority  
- Dependencies notified: Backend, IT, Infrastructure teams involved and their responses  
- All timestamps of communication and diagnostic activities for audit trail  

#### 📣 Communication Milestones:

**Customer Communication:**  
- Acknowledge ticket receipt and initial investigation within 30 minutes  
- Provide detailed update after replication and log collection (within 2 hours), explaining current status and next steps  
- Inform customer when escalation to engineering is initiated, including estimated timelines if available  

**Internal Communication:**  
- Notify Backend, IT, and Infrastructure teams immediately after initial triage  
- Share escalation package with engineering within 4 hours if issue remains unresolved  
- Provide ongoing internal status updates until final resolution  

#### 🔺 Escalation Process:

- **Criteria for Escalation:**  
  - Issue is reproducible or logs reveal silent failure with no immediate fix  
  - Dependency services and network components verified as healthy  
  - Customer impact and frustration level justify engineering involvement  

- **Pre-Escalation Actions:**  
  - Confirm no local misconfiguration or transient infrastructure/network outages  
  - Verify all relevant logs, diagnostic data, and replication steps have been collected  
  - Validate and document replication process clearly  

- **Escalation Package:**  
  - Step-by-step replication guide and detailed environment information  
  - Backend, frontend, and infrastructure logs  
  - Customer sentiment and priority notes  
  - Summary of checks and findings from dependency teams

↩️ [Back to Table of Contents](#table-of-contents)

---

## 4. **Common Issues Prompt Example**  
> For known-issue messages

### 👤 User Input:
- **Customer Name**: Jane
- **Issue Title**: 500 Error When Updating Tool Setting 
- **Root Cause**: Our backend service is temporarily limiting the number of requests to ensure system stability and prevent overload. This can sometimes cause delays in processing certain actions, such as updating payment information  
- **ETA for Fix**: Hotfix being deployed in the next 12 hours
- **Suggested Workaround**: Retry after 15 minutes or use a different browser 
- **Tone**: Professional

### 🤖 AI Output:
Hi Jane,

We’re aware of the 500 error you’re encountering when updating the tool setting. Here’s what we know:

🔧 **Workaround**  
Please try again after 15 minutes or use a different browser to complete your action.

🛠 **ETA for Fix**  
Our engineering team is deploying a hotfix in the next 12 hours. We will notify you as soon as the fix is live.

We apologize for the inconvenience and appreciate your patience as we work on resolving this issue.

Thank you!

↩️ [Back to Table of Contents](#table-of-contents)

---

## 5. **Customer Satisfaction Prompt Example**  
> For post-resolution feedback

### 👤 User Input:
- **Issue Type**: Escalation follow-up
- **Resolution Status**: Still under investigation
- **Customer Effort**: logs provided, steps taken, and our R&D still needs more time for permanant solution 
- **Tone**: Empathetic

### 🤖 AI Output:
Thank you for sharing the detailed logs and walking us through the steps you took—your efforts have been instrumental in helping us move this investigation forward.

We understand how important this issue is to you, and we want to reassure you that our support and R&D teams are actively collaborating to reach a permanent resolution.

While the case remains open and under active investigation, we’ll continue to keep you updated as soon as we have meaningful progress.

We truly appreciate your patience and understanding as we work through this. Please don’t hesitate to reach out if you have any new information or questions in the meantime.

↩️ [Back to Table of Contents](#table-of-contents)

---

## 6. **Follow-Up Prompt Example**  
> For proactive check-ins

### 👤 User Input:

You are a `Technical Agent` following up on a customer support case.
- **Customer Name**: Jane  
- **Case ID / Topic**: #4532 500 Error When Updating Tool Setting  
- **Time Since Last Contact**: 2 days
- **Case Status**: Waiting for Confirmation
- **Preferred Tone**: Professional
- **Optional CTA**: Please let us know if the issue persists.

### 🤖 AI Output:
Hi Jane, 

Just checking in regarding your support case #4532 500 Error When Updating Tool Setting. It’s been 2 days since our last contact, and the case is currently marked as Waiting for Confirmation. 

Please feel free to reply if you have any updates or if there’s anything more we can assist with. Please let us know if the issue persists.

↩️ [Back to Table of Contents](#table-of-contents)
