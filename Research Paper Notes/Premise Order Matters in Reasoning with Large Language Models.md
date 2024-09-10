# Premise Order Matters in Reasoning with Large Language Models

## My Thoughts

In logical reasoning we normally order the premises in the order in which they are used to get to the conclusion. This paper finds that it is easy to confuse an LLM by mixing the order up whereas humans are in general much more resilient to this.

Interesting side point in the paper is that irrelevent context distracts and confuses the LLM. In this case, the irrelevent context is premises that are not used in the final conclusion..

### Internal Links

## Research Paper
[Premise Order Matters in Reasoning with Large Language Models](https://arxiv.org/abs/2402.08939)

### Summary
Large language models (LLMs) have accomplished remarkable reasoning performance in various domains. However, in the domain of reasoning tasks, we discover a frailty: LLMs are surprisingly brittle to the ordering of the premises, despite the fact that such ordering does not alter the underlying task. In particular, we observe that LLMs achieve the best performance when the premise order aligns with the context required in intermediate reasoning steps. For example, in deductive reasoning tasks, presenting the premises in the same order as the ground truth proof in the prompt (as opposed to random ordering) drastically increases the model's accuracy. We first examine the effect of premise ordering on deductive reasoning on a variety of LLMs, and our evaluation shows that permuting the premise order can cause a performance drop of over 30%. In addition, we release the benchmark R-GSM, based on GSM8K, to examine the ordering effect for mathematical problem-solving, and we again observe a significant drop in accuracy, relative to the original GSM8K benchmark.

### Key Contributions
1. **Empirical Analysis**: The paper presents empirical analysis of LLMs' self-correction capabilities, revealing that while self-correction can improve performance, it is not a universal panacea.
2. **Limitations**: It highlights the limitations of self-correction, such as the inability to correct reasoning errors and the potential for performance degradation.
3. **Future Directions**: The authors suggest that future research should focus on developing more sophisticated self-correction mechanisms that can better mimic human-like reasoning.

### Empirical Analysis
The paper provides empirical evidence to support its claims. It uses a variety of datasets and benchmarks to test the self-correction capabilities of several popular LLMs. The results show that while self-correction can improve performance, it is not a universal panacea.