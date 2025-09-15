# Python Screening Task 3: Evaluating Open Source Models

This repository explores open-source AI models for analyzing student-written Python code and generating prompts that assess conceptual understanding.  
Submitted by- Veronika Dhingra

We focus on three leading open-source models:

- [Code LLaMA (Meta)](https://huggingface.co/meta-llama/CodeLlama-7b-Instruct-hf)  
- [StarCoder (BigCode Project)](https://huggingface.co/bigcode/starcoder)  
- [Mistral-7B (Mistral AI)](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.2)  

---

## Setup Instructions

To try out the models locally:

1. Install dependencies: `transformers`, `accelerate`, and `torch`.  
2. Choose one of the model checkpoints from Hugging Face (links above).  
3. Load the model and tokenizer using Hugging Face `transformers`.  
4. Provide a prompt (e.g., student Python code) to analyze.  
5. Generate the model’s output for feedback or hints.  

---

## More Information

- Research plan: [Research_plan.md](./Research_Plan.md)  
- Detailed reasoning: [Reasoning.md](./Reasoning.md)  

