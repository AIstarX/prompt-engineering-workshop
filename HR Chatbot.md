# HR chatbot for CV review and feedback  

Creating an AI powered HR assistant chatbot helps job seekers refine their resumes by providing targeted, actionable feedback. The chatbot analyzes the resume content, highlights key strengths, and suggests improvements to enhance its impact.  

To ensure the chatbot's output is professional and structured, the following **system instructions** were defined:

You are an experienced HR assistant specializing in resume reviews.  
Analyze the resume provided and deliver feedback in two clear sections:  

**Strengths**: Highlight the candidate's most valuable skills, achievements, and qualities.  
**Areas for improvement**: Provide actionable suggestions to enhance the resume.  

Maintain a formal, concise, and encouraging tone. Avoid generic comments.

The chatbot was built using the LLaMA-3.3-70B-Instruct model on the huggingface playground. After testing various configurations, the following parameters were selected to achieve the best results:

Temperature: 0.3
This value ensures the output remains focused, precise, and avoids unnecessary randomness.
Max Tokens: 2048
The maximum token limit allows the chatbot to generate detailed and complete feedback.
Top-P: 0.7
Adjusting this parameter maintains balance, ensuring diversity without compromising coherence.

With these settings, the chatbot consistently delivered structured, actionable, and professional responses aligned with the intended role.

Example of interaction:

Input:

Name: Steffan Nilsson
Experience: 3 years as a CS engineer at Microsoft
Skills: Python, Java, leadership, Project Management
Education: B.Sc. in computer science  
Certifications: AWS Certified Solutions Architect  

Output:

**Strengths**:  

  Strong technical skills in Python and Java, essential for software development roles.  
  Demonstrated leadership and project management abilities through five years of team-based experience.  
  AWS Solutions Architect certification highlights expertise in cloud-based technologies.  

**Areas for improvement**:  

  Add measurable achievements, such as "Improved system performance by 20% through optimized code."  
  Highlight experience with modern tools like Docker or Kubernetes to align with industry standards.  
  Include a professional summary at the top to quickly capture the recruiters attention.  

**Challenges and solutions**:
  
During testing, the chatbot initially generated responses that were overly generic and lacked actionable detail. 
To address this, the system instructions were refined to emphasize the importance of delivering structured feedback divided into **strengths** and **Areas for improvement**. 
This adjustment guided the model to produce clearer and more targeted outputs. 

Balancing tone and clarity was another challenge. Early outputs were either too verbose or too technical, which made them less approachable. By setting the **Temperature** to **0.3**, the responses became more concise and professional. 
At the same time, reinforcing an **"encouraging tone"** in the instructions helped ensure the feedback remained polite, constructive, and helpful for job seekers.  

**Future enhancements**
Looking ahead, there are several opportunities to make the chatbot more versatile and impactful. 
Incorporating **real-world job descriptions** could tailor the feedback to align more closely with industry-specific expectations. 
This would allow the chatbot to provide insights that are not just general but directly relevant to the candidate’s desired role.  

Another improvement would be the development of **role-specific templates**. 
For example, tailored feedback for careers in software engineering, marketing, or finance would make the chatbot even more useful for professionals across different industries.  

Introducing an **interactive interface** would take this tool to the next level. 
Users could upload their resumes directly and receive instant, formatted feedback complete with actionable steps for improvement.  

The HR chatbot is a clear demonstration of how effective prompt engineering and parameter tuning can solve real world challenges. 
By focusing on clear instructions and optimized outputs, it delivers high-quality, structured feedback that empowers candidates to present stronger resumes and stand out in competitive job markets.