# Chain of Thought Prompting Technique

The original chain of thought prompting technique was proposed by [Wei et al. (2022)](https://arxiv.org/abs/2201.11903). The technique was very heavy on examples requiring the prompter to craft example input and out that resembled the question to be answered. The original technique showed a lot of promise in getting the LLMs of the day to answer the types of logic and reasoning problems that they were traditionally bad at.. However, the large amount of overhead required in crafting a prompt makes the technique cumbersome with many real use cases.

## Automatic Chain of Thought

Automatic Chain of Thought is already built into some modern models. It is characterized by telling the LLM to think step by step and provide a detailed and logical answer. This type of reasoning is baked into the system prompts of some modern models such Claude Sonnet 3.5 "When presented with a math problem, logic problem, or other problem benefiting from systematic thinking, Claude thinks through it step by step before giving its final answer."

## Self-Consistency

Self-Consistency is a technique that involves generating multiple plausible solutions to a problem and selecting the most consistent one. This technique is characterized by telling the LLM to think step by step and provide a detailed and logical answer.

## Tree of Thoughts