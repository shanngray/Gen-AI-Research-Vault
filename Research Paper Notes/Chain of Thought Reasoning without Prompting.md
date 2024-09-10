# Chain of Thought Reasoning without Prompting

## My Thoughts
Interesting research paper. Provides a lot of evidence for the argument that LLMs are doing much more than just predicting the next token.

Traditionally LLMs have been used by only picking one path of top-k tokens; however, if multiple paths are inspected it is highly likely that at least one of the paths will have the correct answer arrived at through a series of reasoning steps. Furthermore the LLMs confidence in the answer is usually much higher.

The paper proposes a method to extract reasoning paths from LLMs and uses them to improve the accuracy of the model. The authors argue that the reasoning paths are not only present in the input but also in the output of the model. They introduce a method to extract the reasoning paths from the output of the model and use them to improve the accuracy of the model. (llm produced)

### Internal Links
[Chain-of-Thought - Prompting Technique](./Chain of Thought - Prompting Technique.md)
[Chain-of-Thought - Prompt Template](./Chain of Thought - Prompt Template.md)

## Research Paper
[Chain-of-Thought Reasoning Without Prompting](https://arxiv.org/abs/2402.10200)
### Summary
In enhancing the reasoning capabilities of large language models (LLMs), prior research primarily focuses on specific prompting techniques such as few-shot or zero-shot chain-of-thought (CoT) prompting. These methods, while effective, often involve manually intensive prompt engineering. Our study takes a novel approach by asking: Can LLMs reason effectively without prompting? Our findings reveal that, intriguingly, CoT reasoning paths can be elicited from pre-trained LLMs by simply altering the \textit{decoding} process. Rather than conventional greedy decoding, we investigate the top-k alternative tokens, uncovering that CoT paths are frequently inherent in these sequences. This approach not only bypasses the confounders of prompting but also allows us to assess the LLMs' \textit{intrinsic} reasoning abilities. Moreover, we observe that the presence of a CoT in the decoding path correlates with a higher confidence in the model's decoded answer. This confidence metric effectively differentiates between CoT and non-CoT paths. Extensive empirical studies on various reasoning benchmarks show that the proposed CoT-decoding effectively elicits reasoning capabilities from language models, which were previously obscured by standard greedy decoding.

### Key Contributions
1. **Novelty in Decoding**: The paper introduces a novel decoding method that allows LLMs to reason effectively without prompting. This method involves altering the decoding process to inspect the top-k alternative tokens, which are found to contain CoT paths frequently.
2. **Assessment of Intrinsic Reasoning Abilities**: By bypassing the confounders of prompting, the authors enable the assessment of LLMs' intrinsic reasoning abilities. This is crucial as it allows for a more accurate evaluation of the models' capabilities.
3. **Correlation between CoT and Confidence**: The paper finds that the presence of a CoT in the decoding path correlates with a higher confidence in the model's decoded answer. This correlation helps in differentiating between CoT and non-CoT paths.
4. **Empirical Studies**: Extensive empirical studies on various reasoning benchmarks show that the proposed CoT-decoding effectively elicits reasoning capabilities from language models, which were previously obscured by standard greedy decoding.

### Empirical Studies
The paper presents empirical studies on various reasoning benchmarks to validate the effectiveness of the proposed CoT-decoding method. The results show that the method can effectively elicit reasoning capabilities from language models, which were previously obscured by standard greedy decoding.

### Confidence in CoT-decoding
The confidence score is essentially a measure of how sure the model is about its answer. Here's how it works:
1. When the model is generating an answer, it considers multiple possible words (tokens) at each step.
2. The model assigns probabilities to these tokens. The token with the highest probability is the one it chooses.
3. The confidence score is calculated by looking at the difference between the probability of the top token (the one chosen) and the second-best token.
4. This difference is calculated for each token in the final answer.
5. These differences are then averaged to get an overall confidence score for the answer.
The key insight is that when the model uses a Chain of Thought (CoT) path to reach its answer, there's usually a bigger gap between the probability of the chosen token and the next best option. This larger gap suggests that the model is more confident in its choice.