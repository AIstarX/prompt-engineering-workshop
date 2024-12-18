# Teacher assistant chatbot for full-stack development  

This project focuses on creating a virtual Teacher Assistant chatbot designed to support full-stack development students. Its primary goal is to explain programming concepts, review code for errors, and provide step by step solutions to coding challenges. The assistant aims to deliver clear and actionable feedback, tailored to the needs of beginner and intermediate learners.

## System instructions  

You are a Teacher Assistant specializing in full-stack development.  
Your role is to explain programming concepts in simple terms, review code to identify errors, and assist students in solving coding problems step by step.

When reviewing code:  
  Identify the errors and explain why they are incorrect.  
  Suggest practical improvements to optimize the code.  
  Provide corrected code with detailed explanations.

Maintain a friendly and encouraging tone to create a positive learning environment for students.

## Fine-tuning process  

To develop this chatbot, the **Falcon-7B-instruct** model was chosen for its efficiency in understanding instructions and generating clear outputs. The following parameters were fine-tuned for optimal performance:

  **Temperature**: Set to **0.4** to balance creativity and precision, ensuring explanations are clear yet adaptable to diverse scenarios.  
  **Max Tokens**: Limited to **1500** to allow for detailed responses without overwhelming users.  
  **Top-P**: Adjusted to **0.9** to maintain diversity in examples while ensuring coherence in the answers.

These settings allowed the chatbot to deliver responses that are structured, beginner-friendly, and practical for learning.

## Example interaction  

**Student input**:  
Can you explain how to calculate the sum of the first n numbers in Java using both a loop and a formula?

**Chatbot response**:  

Calculating the sum of the first `n` numbers can be done in two ways: using a loop and using a mathematical formula.

## Challenges and solutions  

**Challenge 1: ensuring that explanations were suitable for beginners while maintaining accuracy**  
Initially, the chatbot's responses were overly technical and included complex terminology. By refining the system instructions to focus on **clear and simple explanations**, responses became much easier for students to understand.

**Challenge 2: code reviews lacked actionable feedback**  
Early outputs identified errors but did not explain why they occurred or how to fix them. Updating the instructions to emphasize **step-by-step solutions** resolved this issue, making the chatbot’s responses both educational and practical.

---

## Future enhancements  

To make the chatbot even more valuable, the following improvements are planned:

**Interactive code execution**  
Allow students to test and debug code snippets directly within the chatbot interface, enabling hands-on practice.

**Role-specific modules**  
Mia responses for specific development areas like **backend (Node.js)**, **frontend (React)**, and **database management**. This specialization would make the feedback more targeted and useful.

**Real-time debugging**  
Enable students to paste their code and receive immediate, detailed feedback on errors, optimizations, and best practices.


By implementing these enhancements, the chatbot can evolve into a highly interactive tool that bridges the gap between learning and practical application.

**Using a loop**:  

```java
public class SumCalculator {

    public static int sumUsingLoop(int n) {
        int sum = 0;
        for (int i = 1; i <= n; i++) {
            sum += i;
        }
        return sum;
    }

    public static void main(String[] args) {
        int n = 5;
        System.out.println("Sum using loop: " + sumUsingLoop(n)); // Output: 15
    }
}
