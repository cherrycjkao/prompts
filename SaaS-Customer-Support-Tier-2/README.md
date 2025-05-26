# 🛠 SaaS Customer Support Prompts (Tier 2)

This section features prompt templates specifically designed for **Tier 2 SaaS support specialists**.  
Whether you're triaging complex issues, replicating bugs, or optimizing internal workflows, these prompts help you stay structured, consistent, and customer-first.

Each prompt is modular, editable, and optimized for clarity, speed, and empathy—supporting fast-paced technical environments.

---

## How to use:

1. Copy the **Prompt** sections into your preferred AI platform.  
2. Fill in your **User Input** (e.g., product module, bug description, system version, etc.).  
3. Use the AI-generated draft to guide your communication or investigation flow.  
4. Modify output based on context or platform constraints (e.g., Zendesk, Salesforce, Intercom).

---

## Table of Contents

- [1. Diagnostic Prompts](#1-diagnostic-prompts)  
- [2. Troubleshooting Prompts](#2-troubleshooting-prompts)  
- [3. Workflow Structuring Prompts](#3-workflow-structuring-prompts)  
- [4. Common Issues Prompts](#4-common-issues-prompts)  
- [5. Customer Satisfaction Prompts](#5-customer-satisfaction-prompts)  
- [6. Follow-Up Prompts](#6-follow-up-prompts)  

---

## 1. **Diagnostic Prompts**

> For information gathering  
> Use this when a customer reports a vague or unclear issue.

### 👤 Prompt Input (User Input):

You are a Tier 2 technical support agent for a SaaS product. Your task is to investigate a reported issue by asking the customer 3 to 5 smart, specific, and technically relevant follow-up questions to help isolate the root cause. Use the following customer-provided information to guide your questions:

- **Product Version**: `[e.g., hardware model, software version, firmware version]`
- **Serial or License Number**: `[e.g., avaialbe on USB dongle or license information on the software]` 
- **Reported Behavior**: `[Brief description including any error codes, error messages, screenshots, or logs]`
- **Steps Taken Before the Issue Occurred**: `[Specific actions the user took]`
`[When the issue occurs (always, intermittently, only in certain cases)]`
- **Customer Environment**: `[Device type, operating system, browser, application version]`
- **Recent Changes**: `[Any updates, configuration changes, deployments, or integrations made recently]`
- **Scope and Impact**: `[How often does the issue occur? / Does it block critical workflows or deadlines?]`
- **Project Deadline**: `[if applicable]`  
- **Known Constraints** (optional): `[e.g., Mobile only / Restricted browser / location-based restrictions]`

Your tone should be:
- Professional and empathetic
- In plain, user-friendly language
- Avoid making wrong assumptions about permissions

### Output Format:

[Provide a numbered list of 3–5 follow-up questions tailored to the information above.]

📌 Example 1
Input:
- Product Version: Web App v3.1
- Serial or License Number: ABC-1234
- Reported Behavior: User sees a blank page when accessing the Billing tab. No error message.
- Project Deadline: Next Tuesday
- Known Constraints: User is on Safari on iOS 16

Response:
- Does this issue occur every time you access the Billing tab, or only intermittently?
- Have you tried accessing the Billing tab on a different browser or device? If yes, does the problem persist?
- Was the Billing tab working previously, or is this your first time using it?
- Have there been any recent updates or changes to the app before this issue started?
- Are other users in your organization experiencing the same issue?

📌 Example 2
Input:
- Product Version: API v2.4
- Serial or License Number: N/A
- Reported Behavior: API returns 401 Unauthorized when calling the /invoices endpoint. Logs attached.
- Project Deadline: ASAP
- Known Constraints: Requests originate from a server hosted in EU-West

Response:
- Has your API key or token recently expired, been rotated, or revoked?
- Are you able to successfully authenticate with other API endpoints using the same credentials?
- Have there been any recent changes to your account permissions or access scopes?
- Are all requests coming from the same server, or is this error seen from multiple environments?
- Does the issue persist when you make the request via a tool like Postman or curl?

> **🛠 Techniques Used:**  
> - Instruction-based: clear instructions on task, tone, output format, prioritization.
> - Few-shot prompting: two detailed examples showing inputs and corresponding questions.
> - Schema prompting: Ensures the model focuses on the most diagnostic fields.
> - Combined prompting: Brings together instructions + examples + structured inputs for maximum reliability.

[↩️ Back to Table of Contents](#table-of-contents)

---

## 2. **Troubleshooting Prompts**

> For clear, step-by-step troubleshooting  
> Use this when the issue is known and you want to guide the customer to a solution.

### 👤 Prompt Input (User Input):

You are a Tier 2 technical support agent for a SaaS product. Your task is to provide the customer with a **clear, actionable resolution path** based on the following issue details. Include all necessary steps to troubleshoot, validate, and roll back any changes safely.

Use the customer-provided information to structure your resolution steps:

- **Issue Summary**: `[Brief description of the issue]`
- **Environment**: `[Device / Browser / OS / App Version / API Version]`
- **Steps Already Tried**: `[What has already been attempted]`
- **Known Constraints**: `[e.g., No dev tools / Slow network / Mobile-only / Limited permissions]`

Your response must include:

- A **numbered list** of step-by-step instructions
- **Conditional steps** or alternatives if a step fails
- **Rollback guidance** for reversible actions
- **Verification steps** to confirm resolution

Your tone should be:
- Clear and professional
- Friendly and supportive
- Technically accurate but accessible to a non-expert

### Output Format:

[Provide a structured, numbered resolution path. Each step should include an action, expected result, and fallback if applicable.]

📌 Example
Input:  
- Issue Summary: User can’t log in to the web app  
- Environment: Chrome 91 on Windows 10  
- Steps Already Tried: Cleared cache, tried another browser  
- Known Constraints: No access to developer console  

Response:

1. **Check Browser Version**  
   - Open Chrome → “Help” → “About Google Chrome”  
   - *If outdated, update the browser and restart*  
   - *If up to date, continue to Step 2*

2. **Clear Cache and Cookies**  
   - Press `Ctrl+Shift+Del` → Select “Cookies” and “Cached Images” → Clear  
   - *Expected: removes potential corrupted session data*

3. **Try Incognito Mode**  
   - Open a new incognito window → Visit the login page  
   - *If successful, issue is likely caused by extensions or stored data*

4. **Rollback (if settings changed)**  
   - If browser settings were modified, reset via: Settings → Advanced → “Reset settings”  
   - *This will undo any problematic configuration changes*

5. **Verify Resolution**  
   - Attempt to log in again  
   - *If successful, issue is resolved; if not, collect error messages or screenshots for escalation*

---

### 💡 Techniques Used

- **Instruction-based prompting**: Clear structure with input schema and expected output  
- **Few-shot prompting**: Example provided to guide agent behavior  
- **Schema prompting**: Ensures consistency by aligning input and output formats  
- **Fallback & rollback logic**: Supports multiple user environments and safe recovery  
- **Verification emphasis**: Confirms success criteria and avoids premature closure

[↩️ Back to Table of Contents](#table-of-contents)

---

## 3. **Workflow Structuring Prompts**

> For structured internal workflow generation
> Use this when a Tier 2 agent needs to create an actionable support plan from a ticket, when organizing your thinking before working a complex ticket.

### 👤 Prompt Input (User Input):

You are a Tier 2 SaaS technical support agent. Based on the provided ticket context, populate an internal workflow using a structured format to ensure:

- Timely resolution of the issue
- Efficient coordination with other teams
- Transparent communication with the customer
- Proper escalation when necessary

### 🗂 Ticket Context:

- **Issue Type**: [e.g., Data sync error / Permissions bug / API failure]  
- **Brief Description**: [Symptoms, error messages, screenshots, logs, etc.]  
- **Dependencies**: [e.g., Backend service, third-party vendor, QA team]  
- **Ticket Priority**: [Low / Medium / Urgent]  
- **Customer Sentiment**: [Neutral / Frustrated / VIP account]  
- **Your Goal**: [e.g., Triage & replicate / Escalate to engineering / Provide workaround]

### 📤 Output Format:

**Structured Action Plan**

#### ✅ Immediate Next Steps:
1. **Action**: [Specific first action, e.g., "Replicate the issue in staging"]  
   - **Responsibility**: [Assigned to you or teammate]  
   - **Expected Outcome**: [e.g., confirm the issue is reproducible]

2. **Action**: [Second step, if escalation is likely or needed]  
   - **Responsibility**: [...]  
   - **Expected Outcome**: [...]

#### 🗒 Internal Notes to Document:
- Troubleshooting steps taken  
- Sentiment and urgency indicators  
- Cross-team dependencies and interactions  
- Relevant logs, screenshots, links, diagnostics

#### 📣 Communication Milestones:

**Customer Communication:**  
- Acknowledge receipt: [e.g., within 15 minutes]  
- First update: [e.g., after 1 hour of triage]  
- Resolution follow-up: [e.g., with ETA and outcome]

**Internal Communication:**  
- Notify dependent teams after initial triage  
- Escalate with full context if unresolved within SLA window

#### 🔺 Escalation Process:

- **Criteria for Escalation**: [e.g., Unreproducible issue, systemic impact, SLA violation]  
- **Pre-Escalation Actions**: [Standard resets, diagnostics, user confirmation]  
- **Escalation Package**: [Logs, steps taken, reproduction instructions, urgency tags]

---

### 📌 Example 1

**Ticket Context:**  
- Issue Type: Permissions Bug  
- Dependencies: Backend permissions API  
- Ticket Priority: Urgent  
- Customer Sentiment: Frustrated, VIP  
- Your Goal: Triage and replicate, then escalate if needed

**Structured Action Plan:**

#### ✅ Immediate Next Steps:
1. **Action**: Replicate issue in staging  
   - **Responsibility**: Tier 2 Support Agent  
   - **Expected Outcome**: Confirm if bug is reproducible in test environment

2. **Action**: Analyze permissions logs  
   - **Responsibility**: Tier 2 Support Agent  
   - **Expected Outcome**: Identify failed API calls or access patterns

#### 🗒 Internal Notes:
- Document VIP status and urgency  
- Log exact replication steps  
- Contact backend team with findings if escalation is needed

#### 📣 Communication Milestones:

- **Customer:**  
  - Acknowledge in 15 minutes  
  - Update within 1 hour  
  - Notify if escalation is initiated  

- **Internal:**  
  - Contact Backend/API team after triage  
  - Escalate within 4 hours if unresolved

#### 🔺 Escalation Process:

- **Criteria:** Issue persists after initial diagnostics  
- **Pre-Escalation:** Confirm it’s not a misconfiguration or expired permission  
- **Package:** Logs, screenshot, test results, customer sentiment noted

---

### 📌 Example 2

**Ticket Context:**  
- Issue Type: Data Sync Error  
- Dependencies: External CRM integration team  
- Ticket Priority: Medium  
- Customer Sentiment: Neutral  
- Your Goal: Provide a temporary workaround and escalate if unresolved after triage

**Structured Action Plan:**

#### ✅ Immediate Next Steps:
1. **Action**: Verify synchronization logs and check for error patterns  
   - **Responsibility**: Tier 2 Support Agent  
   - **Expected Outcome**: Identify if sync failures are consistent or intermittent

2. **Action**: Apply a known temporary workaround to resume partial syncing  
   - **Responsibility**: Tier 2 Support Agent  
   - **Expected Outcome**: Customer operations can continue while issue is investigated

#### 🗒 Internal Notes:
- Document sync failure timestamps and error messages  
- Note any related CRM system outages reported by the vendor  
- Track workaround applied and customer impact

#### 📣 Communication Milestones:

- **Customer:**  
  - Acknowledge receipt within 30 minutes  
  - Provide workaround instructions within 2 hours  
  - Update on vendor investigation status daily

- **Internal:**  
  - Notify CRM integration team immediately after log review  
  - Escalate to engineering if issue persists beyond 24 hours

#### 🔺 Escalation Process:

- **Criteria:** Issue unresolved after temporary workaround and vendor coordination  
- **Pre-Escalation:** Confirm logs reviewed, workaround applied, and vendor status checked  
- **Package:** Sync logs, workaround steps, vendor communication, customer sentiment

---

> **🛠 Techniques Used:**  
> - Schema prompting: Enforces a structured action plan  
> - Role-based instruction: Sets tone and responsibility as Tier 2 agent  
> - Few-shot prompting: Two detailed examples showing inputs and structured outputs  
> - Milestone-driven thinking: Emphasizes time-sensitive communications  
> - Escalation filtering: Prevents unnecessary handoffs with clear criteria and pre-escalation steps

[↩️ Back to Table of Contents](#table-of-contents)

---

## 4. **Common Issues Prompts**

> For speed and consistency  
> Use this to respond to known repetitive issues (e.g., 500 errors, login loops, UI glitches).

### 👤 Prompt Input (User Input):

You're responding to a recurring Tier 2 issue. Write a reusable message explaining the known problem and temporary solution:

- **Issue Title**: `[e.g., 500 error when updating payment info]`  
- **Root Cause (if known)**: `[e.g., backend service rate-limiting]`  
- **ETA for Fix**: `[e.g., Engineering deploying hotfix in 12 hours]`  
- **Suggested Workaround**: `[Steps user can take while waiting]`  
- **Tone**: `[Professional / Friendly / Transparent]`

### Output Format:

[A clear, empathetic message that can be reused, including an apology, optional workaround, and assurance of updates.]

> **🛠 Techniques Used:**  
> - Prewritten template adaptation  
> - Context-sensitive empathy  
> - Explaining known issues with clarity  

[↩️ Back to Table of Contents](#table-of-contents)

---

## 5. **Customer Satisfaction Prompts**

> For human-centered service  
> Use this to craft language that makes customers feel heard—even in technical contexts.

### 👤 Prompt Input (User Input):

You’re closing out a Tier 2 support issue. Write a short message to reinforce trust and satisfaction:

- **Issue Type**: `[Bug fix / Feature request / Escalation follow-up]`  
- **Outcome**: `[Resolved / Workaround provided / Still under investigation]`  
- **Customer Effort**: `[e.g., Spent time testing, provided logs]`  
- **Tone**: `[Empathetic / Grateful / Upbeat]`

### Output Format:

[A human, thoughtful closing message that acknowledges customer effort and builds long-term trust.]

> **🛠 Techniques Used:**  
> - Empathy injection  
> - Trust language modeling  
> - Positive closure phrasing  

[↩️ Back to Table of Contents](#table-of-contents)

---

## 6. **Follow-Up Prompts**

> For proactive support  
> Use this to follow up after a case is closed or pending.

### 👤 Prompt Input (User Input):

Write a proactive follow-up message that checks in with the customer and invites further feedback:

- **Case ID / Topic**: `[e.g., API timeout fix #4532]`  
- **Time Since Last Contact**: `[e.g., 2 days / 1 week]`  
- **Status**: `[Resolved / In monitoring / Waiting for confirmation]`  
- **Tone**: `[Friendly / Casual / Formal]`  
- **Optional CTA**: `[e.g., “Let us know if this still happens”]`

### Output Format:

[A short, polite follow-up message that encourages customer response and maintains open communication.]

> **🛠 Techniques Used:**  
> - Polite persistence  
> - Reassurance-first messaging  
> - CTA for re-engagement  

[↩️ Back to Table of Contents](#table-of-contents)

---

> **Note:** These prompt templates are built for SaaS environments with modular components (e.g., APIs, billing systems, admin consoles, end-user workflows). For multi-product organizations, adapt **Module** and **Issue Type** inputs to your architecture.
