📑 Support Use Case - Example Outputs

How to use:

Copy the Prompt sections from support_prompts/supportREADME.md (excluding the 💡 Note sections).

Provide the required inputs (e.g., issue type, tool name, ticket priority) based on your case.

Use the AI‑generated output for ticket triage, response drafts, root cause summaries, or customer updates.

Table of Contents:

Tool Issue Triage Prompt Example

Root Cause Summary Generator Example

Support Response Writer Example

Follow-Up Email Writer Example

💡 Note:

Each section demonstrates a reusable prompt tailored to a specific support task.

Outputs are structured, clear, and follow tone guidelines for enterprise support comms.

You can mix and match modules for multi-step responses.

1. Tone Tuner for Support Tickets

Description:This prompt helps adjust the tone of support replies to match the desired level of empathy, formality, and friendliness, while keeping content intact.

🟦 User Input Format:

Raw message (agent-written)

Desired tone (e.g., friendly, neutral, apologetic)

📌 Prompt Usage Guidelines:Use this to humanize overly robotic replies or make emotional ones more professional.

🤖 Output Format:A revised message with the same content but adjusted tone.

🛠 Technologies:Tone style transfer, semantic preservation model

2. Troubleshooting Explainer Generator

Description:Generates step-by-step explanations for troubleshooting procedures in simple, clear language.

🟦 User Input Format:

Technical issue description

Steps needed to fix

User expertise level (e.g., beginner, advanced)

📌 Prompt Usage Guidelines:Use this when customers need to perform technical actions themselves.

🤖 Output Format:A plain-language message guiding the user step-by-step.

🛠 Technologies:Instruction rewriter, technical simplifier, reading level adjuster

3. Bug Acknowledgement Prompts

Description:Helps agents professionally acknowledge known bugs and explain what's being done, without sounding vague or dismissive.

🟦 User Input Format:

Bug summary

Known impact

Workaround (if any)

ETA or next update

📌 Prompt Usage Guidelines:Use when confirming an issue is a known bug. Avoid overpromising.

🤖 Output Format:A concise, polite explanation of the known issue and current status.

🛠 Technologies:Apology softener, ETA estimator, transparency-enhancer

4. Escalation Summary Prompts

Description:Helps agents summarize a case before escalating to a higher-level team, ensuring clarity and completeness.

🟦 User Input Format:

Customer issue summary

Troubleshooting already done

Relevant logs/screenshots (optional)

Urgency level

📌 Prompt Usage Guidelines:Use before escalation to reduce back-and-forth. Should include what's been tried and what’s needed.

🤖 Output Format:A 3–5 sentence escalation summary suitable for internal transfer.

🛠 Technologies:Summarization engine, context condensing module, intent classifier

5. Customer Satisfaction Prompts

Description:These prompts help support agents craft natural, polite, and non-robotic responses when collecting feedback after an interaction. Designed to encourage honest replies and improve future service quality.

🟦 User Input Format:

Agent name

Case ID or short reference

Service outcome summary

Preferred tone (e.g., friendly, professional)

📌 Prompt Usage Guidelines:Use after a case is resolved or a ticket is closed. Best sent within 24 hours of resolution. Maintain a balance between warmth and brevity.

🤖 Output Format:A short customer satisfaction message (2–3 sentences) with a CTA (e.g., feedback link or rating request).

🛠 Technologies:Tone rewriter, intent detection, conversational UX enhancer

6. Follow-Up Prompts

Description:These prompts generate empathetic follow-up messages for unresolved issues or pending fixes. Useful for checking in with customers and maintaining proactive communication without sounding repetitive.

🟦 User Input Format:

Customer name

Original issue summary

Last action taken

Next expected step or ETA

Optional: Internal ticket number

📌 Prompt Usage Guidelines:Use if more than 48 hours have passed without update. Adjust frequency depending on urgency and sensitivity of the case.

🤖 Output Format:A clear, personalized follow-up message that includes brief status, next steps, and a warm tone.

🛠 Technologies:Context retention engine, natural tone composer, message shortening logic
