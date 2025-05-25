📂 AI Output Templates for SaaS Tier 2 Support

This document provides clear, reusable output formats for each AI prompt type listed in the SaaS Customer Support Prompts (Tier 2) README. All formats are modular and can be adapted to your tools (e.g., Zendesk, Salesforce, Intercom).

1. Diagnostic Output

Used after collecting vague or partial reports.

Output Format:

**🔍 Clarification Questions**

**Environment**
- Can you confirm which browser and device you're using?
- Are there any browser extensions enabled?

**Reproduction Steps**
- What exact steps are you taking before the issue appears?
- Is the issue reproducible every time?

**Expected vs Actual Behavior**
- What did you expect to happen?
- What happened instead?

**Additional Context**
- Has this occurred before?
- Are other users in your team seeing the same issue?

💡 Tailor question order based on urgency and known constraints.

2. Troubleshooting Output

Used to walk customers through resolution steps.

Output Format:

**🛠 Steps to Resolve**

1. Log out of your account and clear your browser cache.
2. Log back in and attempt the same action.
3. If the issue persists, try accessing via Incognito/Private mode.
4. Still facing the issue? Please collect a HAR file using [these steps](https://example.com).

**✔️ Verification**
- Let us know if the issue is resolved after step 3.
- If not, share your HAR file and the timestamp of your last attempt.

📌 Customize tone: reassuring, technical, or friendly based on context.

3. Internal Workflow Structuring Output

Used to organize your next actions internally.

Output Format:

**🧭 Internal Plan for Ticket #[Ticket ID]**

**Immediate Steps**
- Reproduce issue using reported inputs.
- Check logs from [Timestamp / User ID].

**Dependencies**
- API Team (auth headers)
- Billing System (sync check)

**Priority**: Medium
**Customer Sentiment**: Frustrated (VIP)
**Goal**: Replicate & prepare pre-escalation packet

**Next Touchpoint**: Update customer within 2 business hours.

🧠 Keeps thinking organized for complex multi-stakeholder issues.

4. Common Issues Output

Used for known problems with workaround.

Output Format:

**📣 Known Issue: 500 Error on Payment Update**

Hi [Customer Name],

We’re aware of an issue where customers encounter a 500 error when updating their payment information. This is due to a temporary rate-limiting conflict in our backend service.

**Temporary Solution**
Please try updating your info after 15–20 minutes, or use a different browser.

**ETA for Fix**
Engineering is deploying a hotfix within 12 hours. We'll notify you once resolved.

Apologies for the disruption, and thank you for your patience!

📣 Ideal for copy-pasting into tickets or mass status updates.

5. Customer Satisfaction Output

Used when closing tickets with a human tone.

Output Format:

**🎉 Issue Resolved – Thank You!**

Hi [Customer Name],

Thanks again for your patience while we worked on the [issue type]. We’ve now confirmed it’s resolved.

Really appreciate the logs and steps you shared—it helped a lot!

If you need anything else, don’t hesitate to reach out.

Warm regards,  
[Agent Name]  
Tier 2 Support

❤️ Keep it short, real, and appreciative.

6. Follow-Up Output

Used to maintain proactive communication.

Output Format:

**🔄 Just Checking In – [Case Topic]**

Hi [Customer Name],

Just following up on your case regarding [topic]—we wanted to make sure everything is still working well on your end.

If anything unexpected happens again, feel free to reply to this message. We’re here to help!

Warmly,  
[Agent Name]  
Tier 2 Support

📬 Useful for re-engaging quietly closed or pending cases.

✅ Usage Notes

These output templates are mapped directly to the input formats listed in the README for SaaS Tier 2 Prompts.

They are optimized for copy-paste use and modular editing.

To localize or scale, consider parameterizing with variables or integrating into macros.
