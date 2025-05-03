# Business: HR & Recruitment Prompts

This section contains AI prompt frameworks designed for HR professionals and recruiters.  
The prompts assist in drafting job descriptions, analyzing resumes, generating interview questions, and summarizing candidate profiles.  
Each prompt is designed to extract relevant information and streamline repetitive tasks, while ensuring that final hiring decisions remain fully human-led.

## How to use:
1. Copy the **Prompt** sections to your AI tool (excluding the **💡 Note** sections).
2. Provide the required inputs (e.g., role title, candidate information, etc.) based on your needs.
3. Use the AI-generated output for your HR/recruitment tasks, such as drafting job descriptions, analyzing resumes, or preparing interview questions.

## Table of Contents
- [1. Job Description Generator Prompt](#1-job-description-generator-prompt)
- [2. Resume Analyzer](#2-resume-analyzer)
- [3. Interview Question Builder](#3-interview-question-builder)
- [4. Batch Candidate Summary Generation](#4-batch-candidate-summary-generation)

---

## 1. **Job Description Generator Prompt**  
> Generate clear and comprehensive job descriptions tailored to the role and requirements.  

### 👤 **Prompt Input (User Input):**
You are the best HR assistant specializing in creating professional job descriptions.

Based on the following input, generate a clear, detailed, and structured job description including a summary, key responsibilities, and required qualifications.

**Prompt User Input:**
- **Role Title**: Product Manager
- **Department**: Product Development
- **Experience**: 3-5 years
- **Skills**: Agile methodologies, Roadmapping, Cross-functional collaboration
- **Preferred Qualifications**: MBA degree, Experience with SaaS products

**Instructions:**
1. Start with a brief summary of the role.
2. Follow with a bullet list of key responsibilities (5–7 items).
3. Include required and preferred qualifications as separate sections.
4. Use professional and concise language tailored for HR/recruitment use.

**Output Format:**

**Job Title:** [Auto-filled from Role Title]  
**Department:** [Auto-filled from Department]  

**Job Summary:**  
[Generated summary paragraph tailored to the role]

**Key Responsibilities:**  
- ...
- ...

**Required Qualifications:**  
- ...

**Preferred Qualifications:**  
- ...

> **💡 Note**: This job description template is designed to be flexible and can be easily adapted for different roles and industries.

> **Techniques Used:**
> - **Parameter-based Prompting**: Inputs are clearly structured for easier customization.
> - **Chain of Thought**: Guides the AI to logically build the job description.
> - **Instruction-based Prompting**: Defines clear generation steps and formatting.
> - **Structured Output**: Ensures consistency across different roles.

---

## 2. **Resume Analyzer**  
> Assist in analyzing resumes by extracting relevant skills, experiences, certifications, and years of experience in relation to the job requirements.  
> **💡 Note:** This analysis is informational only. Final evaluation and hiring decisions must be made by HR personnel.

### 👤 **Prompt Input (User Input):**
Analyze the resume of **[Candidate's Name]** against the job requirements for the position of **[Job Title]**.  
Extract and summarize the following details:

**Prompt User Input:**
- **Resume**: [Candidate's Resume (personal info, work experience, skills, etc.)]
- **Job Requirements**: [Job Title, Skills, Experience, Qualifications]

**Output Format:**

**Resume Review for [Candidate's Name]:**
- **Relevant Skills Identified**: List the candidate’s skills that match the job requirements.
- **Relevant Certifications**: List any certifications relevant to the job.
- **Years of Relevant Experience**: Estimate total years of experience related to the job.
- **Additional Notable Achievements**: Summarize any significant achievements that may add value.

> **💡 Note**:  
> - Do not provide any recommendation, score, or hiring decision.  
> - Maintain a neutral and factual tone focused only on information extraction.

> **Techniques Used:**
> - **Chain of Thought**: Guides the AI to systematically extract and organize information based on defined categories without subjective judgment.
> - **Few-shot Learning**: Structured examples are used to show the AI how to extract consistent and relevant data points across different resumes.
> - **System Prompting**: Ensures the AI outputs strictly within the defined informational categories to maintain neutrality and compliance.

---

## 💡 **Compliance Note**  
This Resume Analyzer is designed to comply with global AI regulations, including the EU AI Act and the U.S. EEOC's initiatives on AI fairness in employment, by avoiding automated decision-making and ensuring human oversight.  
Final hiring decisions must always be made by human HR personnel.

## References
- [EU Artificial Intelligence Act - European Commission](https://digital-strategy.ec.europa.eu/en/policies/european-approach-artificial-intelligence)
- [EEOC Launches Initiative on Artificial Intelligence and Algorithmic Fairness - U.S. Equal Employment Opportunity Commission](https://www.eeoc.gov/newsroom/eeoc-launches-initiative-artificial-intelligence-and-algorithmic-fairness)

---

## 3. **Interview Question Builder**  
> Generate a list of customized interview questions based on the job description and candidate profile.  

### 👤 **Prompt Input (User Input):**
Generate customized interview questions based on the following information:
- **Role**: [Job Title for the position, e.g., Product Manager]
- **Job Description**: [Detailed job responsibilities, required skills, qualifications]
- **Candidate Profile**: [Candidate’s background information including skills, experience, and education]

**Instructions:**
1. Tailor the questions specifically to assess the candidate's fit for the given role.
2. Cover key competencies such as role-specific skills, cross-functional collaboration, problem-solving, and industry-related experience.
3. Ensure questions reflect both the job description requirements and the candidate’s profile.

**Output Format:**
**Suggested Interview Questions:**
1. [Generated Question 1]
2. [Generated Question 2]
3. [Generated Question 3]
(...as many as appropriate)

> **💡 Note**: Focus on making each question relevant and insightful to better evaluate the candidate's suitability.

> **Techniques Used:**
> - **Few-shot**: Guide the AI to generate multiple examples (interview questions) in one go.
> - **Role Specification**: Clearly define the position title to provide context.
> - **Context Embedding**: Include job description and candidate profile for richer, more informed generation.
> - **Instruction-based Prompting**: Direct the AI with clear, step-by-step instructions.

---

## 4. **Batch Candidate Summary Generation**  
> Summarize candidate profiles neutrally, highlighting experiences, skills, and qualifications without making any suitability assessments.

### 👤 **Prompt Input (User Input):**
You will receive multiple candidate profiles along with the same job requirements.  
For each candidate:
1. Write a professional and factual summary based on the provided candidate information.
2. Highlight the candidate’s most relevant experiences, education, certifications, and skills.
3. List 2–5 "Key Strengths" extracted from the profile.

Do **not** make any recommendation or judgment regarding the candidate’s suitability for the role.

---

## Inputs

- **Job Requirements** (shared for all candidates):  
  [Job Title, Key Skills, Required Experience, Industry-Specific Knowledge]

- **Candidate Profiles** (list of multiple candidates):  
  For each candidate, the following will be provided:
  - Name
  - Work Experience
  - Education
  - Skills
  - Certifications
  - Achievements
> **💡 Note:**  
> Continue applying the above structure for all provided candidates until the list is complete.  
> Maintain a consistent, formal, and concise writing style.  
> Slightly adjust tone depending on candidate seniority (e.g., entry-level, mid-career, executive) but stay objective.
---
## Output Format for Each Candidate

**Candidate Summary for [Candidate's Name]**

[Professional and factual summary paragraph(s) describing the candidate’s background and qualifications relevant to the job requirements.]

**Key Strengths:**
- [Strength 1]
- [Strength 2]
- [Strength 3]
- (optional more)
---

> **Techniques Used:**
> - **Batch Processing**: Process multiple profiles in one instruction loop.
> - **Loop Instruction**: Clear instruction to repeat the structure for each candidate.
> - **Context Embedding**: Summaries connect candidate backgrounds to the job context factually.
> - **Neutral Information Extraction**: No recommendations, scores, or suitability judgments.
> - **Structured Output Design**: Clear, repeatable format for easy HR team reference.
> - **Instruction-based Prompting**: Enforces neutrality and consistency throughout outputs.

---

## 💡 **Compliance Note**  
This candidate summarization approach aligns with global AI compliance standards, including the EU AI Act and U.S. EEOC initiatives, by ensuring that only human decision-makers assess candidate suitability.

## References
- [EU Artificial Intelligence Act - European Commission](https://digital-strategy.ec.europa.eu/en/policies/european-approach-artificial-intelligence)
- [EEOC Launches Initiative on Artificial Intelligence and Algorithmic Fairness - U.S. Equal Employment Opportunity Commission](https://www.eeoc.gov/newsroom/eeoc-launches-initiative-artificial-intelligence-and-algorithmic-fairness)

---

**📌 Recommendation:** The AI provides a final recommendation based on the analysis, offering guidance on the candidate’s suitability for the role. This tool provides assistance only. Final decisions must be made by HR personnel.  
For detailed instructions and usage, please see the [examples.md](examples.md) file.
