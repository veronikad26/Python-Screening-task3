# Reasoning

1. Suitability: A model is suitable for high-level competence analysis if it can go beyond syntax checking to identify misconceptions, explain reasoning, and phrase prompts in a way that fosters student reflection rather than spoon-feeding answers.

2. Testing meaningful prompts: I would validate by comparing model-generated hints against expert-teacher prompts, assessing whether they push students toward the right concepts without giving solutions directly.

3. Trade-offs: Larger models (Code LLaMA 34B) may produce more accurate, nuanced prompts but are harder to deploy in real classrooms due to cost and latency. Smaller models (Mistral-7B) are cheaper and faster but may miss deeper misconceptions. StarCoder provides strong coverage of code structures but may need fine-tuning for pedagogical alignment.

4. Why chosen: I focused on Code LLaMA, StarCoder, and Mistral because they are leading open-source models in code analysis and educational applications. Code LLaMA’s Python specialization is a major strength, StarCoder’s context handling is valuable for longer code, and Mistral has evidence of strong performance in feedback generation. Their limitations lie in either resource demands (LLaMA), instruction alignment (StarCoder), or domain specialization (Mistral).

--- 

# Example

**Student submission:**

<pre>
  ```python
   def factorial(n):
     if n == 0:
       return 0   # it should return 1
    else:
        return n * factorial(n-1) ```` 
</pre>

1. Expected teacher feedback:
The student misunderstands the base case of factorial. Instead of returning 0, the correct return value should be 1. A good prompt would guide the student to reconsider what factorial(0) means mathematically.

2. Model-style feedback:
Code LLaMA (Python-Instruct):
“Notice how your function defines the factorial of 0. Does 0! equal 0 or something else in mathematics? Think carefully about the definition before adjusting your base case.”

StarCoder (base):
“The base case looks incorrect. The factorial of 0 is 1, not 0. You should return 1 instead.”
(Direct correction, less pedagogical.)

Mistral-7B (general LLM):
“You’ve got the recursive structure right! But what happens when you call factorial(0) with your current code? Try running it and see if the result matches the mathematical definition of factorial.”

3. Comparison:
Code LLaMA gives a guided prompt encouraging reflection, StarCoder provides a direct correction (good for accuracy but less for competence building), and Mistral encourages experimentation but may be less precise.
