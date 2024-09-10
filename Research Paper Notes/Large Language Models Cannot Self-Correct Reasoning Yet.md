# Large Language Models Cannot Self-Correct Reasoning Yet

## My Thoughts
They distinguish early on the difference between intrinsic self-correction, where the LLM self-corrects without any external feedback, anf self-correction which includes external feedback. In a multi-agent model it is unclear if they would consider feedback from another agent using the same LLM as being external or intrinsic.

Interestingly, they do find that self-correction can be helpful where the initial prompt is subpar.

TODO: Need to expierment with building self-correction into the initial prompt
 This could be as simple as "Explain your reasoning and if you realise there is an error in your initial respponse, go back and start again."
### Internal Links

## Research Paper
[Large Language Models Cannot Self-Correct Reasoning Yet](https://arxiv.org/abs/2402.08906)

### Summary
Large Language Models (LLMs) have emerged as a groundbreaking technology with their unparalleled text generation capabilities across various applications. Nevertheless, concerns persist regarding the accuracy and appropriateness of their generated content. A contemporary methodology, self-correction, has been proposed as a remedy to these issues. Building upon this premise, this paper critically examines the role and efficacy of self-correction within LLMs, shedding light on its true potential and limitations. Central to our investigation is the notion of intrinsic self-correction, whereby an LLM attempts to correct its initial responses based solely on its inherent capabilities, without the crutch of external feedback. In the context of reasoning, our research indicates that LLMs struggle to self-correct their responses without external feedback, and at times, their performance even degrades after self-correction. Drawing from these insights, we offer suggestions for future research and practical applications in this field.

### Key Contributions
1. **Empirical Analysis**: The paper presents empirical analysis of LLMs' self-correction capabilities, revealing that while self-correction can improve performance, it is not a universal panacea.
2. **Limitations**: It highlights the limitations of self-correction, such as the inability to correct reasoning errors and the potential for performance degradation.
3. **Future Directions**: The authors suggest that future research should focus on developing more sophisticated self-correction mechanisms that can better mimic human-like reasoning.

### Empirical Analysis
The paper provides empirical evidence to support its claims. It uses a variety of datasets and benchmarks to test the self-correction capabilities of several popular LLMs. The results show that while self-correction can improve performance, it is not a universal panacea.