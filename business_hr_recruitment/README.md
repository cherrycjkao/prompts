# Business: HR & Recruitment Prompts

This section contains AI prompt frameworks designed for HR professionals and recruiters.  
The prompts assist in creating job descriptions, screening resumes, generating interview questions, and summarizing candidate profiles. Each prompt can be customized to fit any position.

## 1. **Job Description Generator prompt**  
> Generate clear and comprehensive job descriptions tailored to the role and requirements
### **Prompt:**
Generate a comprehensive job description for the role of [Role Title], which is part of the [Department] department. The ideal candidate should have [Experience] of experience in [Role Title] with expertise in [Skills]. Preferred qualifications include [Preferred Qualifications]. Ensure the job description includes key responsibilities and qualifications for the position.

> Techniques Used:
> - **Chain of Thought**: The prompt logically leads the AI to generate all necessary sections (job title, responsibilities, qualifications) based on input criteria.
> - **Few-shot**: The example of a "Product Manager" role gives the AI context for how to format the output.
> - **System Prompt**: The AI is instructed to generate specific parts of the job description (Responsibilities and Qualifications) while incorporating the user input.

## 2. **Resume Screening Assistant**  
> Assist in screening resumes and matching qualifications to job requirements.
### **Prompt:**
Analyze the resume of [Candidate's Name] with respect to the job requirements for the position of [Job Title]. Include the following details in the analysis:

Resume: [Candidate's Resume (personal info, work experience, skills, etc.)]

Job Requirements: [Job Title, Skills, Experience, Qualifications]

Provide an analysis that includes:

- **Matches**: Highlight the skills and experiences from the resume that align with the job requirements.
- **Missing**: List any qualifications or skills that are missing from the candidate's resume.
- **Recommendation**: Based on the matches and missing skills, provide a recommendation whether to proceed with the candidate or not.

> Techniques Used:
> - **Chain of Thought**: This technique allows the AI to systematically analyze the resume against the job requirements, ensuring it identifies matches, missing qualifications, and provides a coherent recommendation.
> - **Few-shot**: By giving the AI a structured example (even without full details), it learns how to process similar inputs and generate relevant outputs.
> - **System Prompt**: This directs the AI to produce a structured output based on specific categories (Matches, Missing, and Recommendation) while focusing on user-provided inputs for resume and job requirements.

## 3. **Interview Question Builder**  
> Generate a list of customized interview questions based on the job description and candidate profile.
### **Prompt:**
You are an HR assistant designed to generate tailored interview questions. When generating questions, follow this thought process:
1. Start by understanding the key responsibilities and required skills of the role.
2. Think about potential challenges the candidate will face in this role and how they might approach them.
3. Consider the candidate’s background and how it aligns with the job description.

Here are some example questions for a Product Manager:
1. How do you prioritize competing product features when resources are limited?
2. Can you describe a time when you led a product development project and had to manage stakeholders with different priorities?

Now, based on the following details, generate interview questions:
- Role: [Role]
- Job Description: [Detailed Job Description]
- Candidate Profile: [Candidate’s Background Information]

> Techniques Used:
> - **Chain of Thought**: Explicitly outlines a thought process that the AI should follow before generating interview questions. This chain of reasoning helps guide the AI step-by-step, ensuring that it logically considers key aspects of the role, potential challenges, and the candidate’s background.
> - **Few-shot**: Involves providing a few examples to guide the AI’s understanding of the task. These examples help the AI learn how to generate relevant and high-quality outputs even with limited data.
> - **System Prompt**: Sets the context and behavior of the AI throughout the task. It instructs the AI on how to approach the task and what priorities to focus on.

## 4. **Candidate Summary Writer**  
> Summarize candidate profiles and qualifications for quick reference.
### **Prompt:**
[Candidate's Name] is a highly qualified [Job Title] with [X] years of experience in [Key Skills/Experience]. She/he holds a [Degree/Certification] from [University/Institution] and has worked extensively with [Relevant Industry/Technology].  
Her/his technical background includes proficiency in [Skills], and she/he has a proven track record of [Key Achievements/Experience].

> **Note**: This is the AI-generated summary of the candidate's profile, highlighting key qualifications, experiences, and strengths that align with the job requirements.  
*Technique: AI output structured in a summary format based on provided user input.*

**Key Strengths:**
- [Key Strength 1]
- [Key Strength 2]
- [Key Strength 3]

> **Note**: These key strengths are generated by the AI, based on the candidate's profile and the job requirements provided by the user.  
*Technique: Highlighting key strengths based on analysis of candidate profile and job requirements.*

**Recommendation:**
[Candidate's Name] is a strong candidate for the [Job Title] role, with a deep understanding of [Specific Skill/Area] and proven success in [Related Experience]. She/he would be a valuable addition to any [Department/Team].

> **Note**: This recommendation is generated based on the AI’s analysis of the candidate's profile and their fit for the job position.  
*Technique: AI-generated recommendation based on profile analysis and job fit.*

> Techniques Used:
> - **Open-ended user input**: The user can provide detailed candidate information and job requirements, allowing for flexible customization.
> - **Contextual input**: The job description and candidate profile serve as the context for generating a tailored summary.

Recommendation: The AI provides a final recommendation based on the analysis, offering guidance on the candidate’s suitability for the role.
For detailed instructions and usage, please see the [examples.md](examples.md) file.

---
