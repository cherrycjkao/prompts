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
