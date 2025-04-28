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

> Techniques Used:
## 4. **Candidate Summary Writer**  
> Summarize candidate profiles and qualifications for quick reference.
### **Prompt:**

> Techniques Used:
> 

For detailed instructions and usage, please see the [examples.md](examples.md) file.

---
