# LLM Role-Playing Agent Evaluation Survey

Role-Playing Agent (RPA) is an increasingly popular type of LLM Agent that simulates human-like behaviors in a variety of tasks. However, evaluating RPAs is challenging due to diverse task requirements and agent designs.This paper proposes an evidence-based, actionable, and generalizable evaluation design guideline for LLM-based RPA by systematically reviewing $1,676$ papers published between Jan. 2021 and Dec. 2024. Our analysis identifies six agent attributes, seven task attributes, and seven evaluation metrics from existing literature. Based on these findings, we present an RPA evaluation design guideline to help researchers develop more systematic and consistent evaluation methods.

![RPA evaluation design guideline. To illustrate how to use it in practice, we pretended we were selecting the evaluation metrics for the “Stanford Agent Village” (Park et al., 2023) given agent attributes (yellow) and task attributes (pink). The original authors’ selection of evaluation metrics (purple and blue) perfectly aligns with our RPA design guideline, which echoes their work’s robustness.](assets/Teaser_survey_good_example_landscape.png)

RPA evaluation design guideline. To illustrate how to use it in practice, we pretended we were selecting the evaluation metrics for the “Stanford Agent Village” [(Park et al., 2023)](https://dl.acm.org/doi/abs/10.1145/3586183.3606763) given agent attributes (yellow) and task attributes (pink). The original authors’ selection of evaluation metrics (purple and blue) perfectly aligns with our RPA design guideline, which echoes their work’s robustness.

For more details, please refer to our paper:
>[Towards a Design Guideline for RPA Evaluation: A Survey of Large Language Model-Based Role-Playing Agents]()
>
>Chaoran Chen, Bingsheng Yao, Ruishi Zou, Wenyue Hua, Weimin Lyu, Toby Jia-Jun Li, Dakuo Wang
>
>[Arxiv]() | [PDF](assets/Towards_a_Design_Guideline_for_RPA_Evaluation__A_Survey_of_Large_Language_Model_Based_Role_Playing_Agents.pdf) | [Cite](#citation)


## Table of Content
- [LLM Role-Playing Agent Evaluation Survey](#llm-role-playing-agent-evaluation-survey)
  - [Table of Content](#table-of-content)
  - [Agent Attributes](#agent-attributes)
  - [Task Attributes](#task-attributes)
  - [Metrics](#metrics)
    - [Agent- \& Task-Oriented Metrics](#agent---task-oriented-metrics)
    - [Top 3 frequently used agent-oriented metrics for each agent attribute](#top-3-frequently-used-agent-oriented-metrics-for-each-agent-attribute)
    - [Top 3 frequently used task-oriented metrics for each task attribute](#top-3-frequently-used-task-oriented-metrics-for-each-task-attribute)
    - [Agent-oriented evaluation metrics glossary](#agent-oriented-evaluation-metrics-glossary)
    - [Task-oriented evaluation metrics glossary](#task-oriented-evaluation-metrics-glossary)
  - [Citation](#citation)

## Agent Attributes

| **Agent Attributes**       | **Definition**                                                                 | **Examples** |
|------------------------|--------------------------------------------------------------------------|----------|
| **Activity History**   | A record of past actions, behaviors, and engagements, including schedules, browsing history, and lifestyle choices. | Backstory, plot, weekly schedule, browsing history, social media posts, lifestyle |
| **Belief and Value**   | The principles, attitudes, and ideological stances that shape an individual’s perspectives and decisions. | Stances, beliefs, attitudes, values, political leaning, religion |
| **Demographic Information** | Personal identifying details such as name, age, education, career, and location. | Name, appearance, gender, age, date of birth, education, location, career, household income |
| **Psychological Traits** | Characteristics related to personality, emotions, interests, and cognitive tendencies. | Personality, hobby and interest, emotional |
| **Skill and Expertise** | The knowledge level, proficiency, and capability in specific domains or technologies. | Knowledge level, technology proficiency, skills |
| **Social Relationships** | The nature and dynamics of interactions with others, including roles, connections, and communication styles. | Parenting styles, interactions with players |

## Task Attributes

| **Task Attributes**           | **Definition** |
|---------------------------|--------------------------------------------------------------|
| **Simulated Individuals** | Simulating specific individuals or groups, such as users and participants. |
| **Simulated Society**     | Simulating social interactions, such as cooperation, competition, and communication. |
| **Opinion Dynamics**      | Simulating political views, legal perspectives, and social media content. |
| **Decision Making**       | Simulating decision-making of stakeholders in investment, public policies, or games. |
| **Psychological Experiments** | Simulating human traits, including personality, ethics, emotions, and mental health. |
| **Educational Training**  | Simulating teachers and learners to enable personalized teaching and accommodate learner needs. |
| **Writing**              | Simulating readers or characters to support character development and audience understanding. |

## Metrics

### Agent- & Task-Oriented Metrics

| **Evaluation Metrics**          | **Definitions**     | **Examples**   |
|-----------------------------|---------------------------------------------------------------------------------------------|-----------------------------------|
| **Performance**             | Assess RPAs’ effectiveness in task execution and outcomes.                                  | Prediction accuracy               |
| **Psychological**           | Measure human psychological responses to RPAs and the agents’ self-awareness and emotional state. | Big Five Inventory               |
| **External Alignment**      | Evaluate how closely RPAs align with external ground truth or human behavior and judgments. | Alignment between model and human |
| **Internal Consistency**    | Assess coherence between an RPA’s predefined traits (e.g., personality), contextual expectations, and behavior. | Personality-behavior alignment   |
| **Social and Decision-Making** | Analyze RPAs’ social interactions and decision-making, including their effects on negotiation, societal welfare, markets, and social dynamics. | Social Conflict Count            |
| **Content and Textual**     | Evaluate the quality, coherence, and diversity of RPAs’ text, including semantic understanding, linguistic style, and engagement. | Content similarity               |
| **Bias, Fairness, and Ethics** | Assess biases, extreme or unbalanced content, or stereotyping behavior.                     | Factual error rate               |

### Top 3 frequently used agent-oriented metrics for each agent attribute

| **Agent Attributes**       | **Top 3 Agent-Oriented Metrics** |
|------------------------|--------------------------------------------------------------|
| **Activity History**   | External alignment metrics, internal consistency metrics, content and textual metrics |
| **Belief and Value**   | Psychological metrics, bias, fairness, and ethics metrics |
| **Demographic Info.**  | Psychological metrics, internal consistency metrics, external alignment metrics |
| **Psychological Traits** | Psychological metrics, internal consistency metrics, content and textual metrics |
| **Skill and Expertise** | External alignment metrics, internal consistency metrics, content and textual metrics |
| **Social Relationship** | Psychological metrics, external alignment metrics, social and decision-making metrics |

### Top 3 frequently used task-oriented metrics for each task attribute

| **Task Attributes**         | **Top 3 Task-Oriented Metrics** |
|-------------------------|--------------------------------------------------------------|
| **Simulated Individuals** | Psychological, performance, and internal consistency metrics |
| **Simulated Society**     | Social and decision-making metrics, performance metrics, and psychological metrics |
| **Opinion Dynamics**      | Performance metrics, external alignment metrics, and bias, fairness, and ethics metrics |
| **Decision Making**       | Social and decision-making, performance, and psychological metrics |
| **Psychological Experiment** | Psychological, content and textual, and performance metrics |
| **Educational Training**  | Psychological, performance, and content and textual metrics |
| **Writing**              | Content and textual, psychological, and performance metrics |

### Agent-oriented evaluation metrics glossary

| **Attribute Category**       | **Agent-Oriented Metrics**          | **Approach**      | **Source**                     |
|--------------------------|--------------------------------|---------------|----------------------------|
| **Belief & Value**       | Bias, fairness, ethics metrics | Exaggeration (normalized average cosine similarity) | Automatic | [Cheng et al., 2023](#) |
| **Belief & Value**       | Bias, fairness, ethics metrics | Individuation (classification accuracy) | Automatic | [Cheng et al., 2023](#) |
| **Belief & Value**       | Bias, fairness, ethics metrics | Bias (performance disparity, prevalence, magnitude, variation, attitude shift) | Automatic | [Gupta et al., 2024](#) |
| **Belief & Value**       | Bias, fairness, ethics metrics | Bias (performance disparity, prevalence, magnitude, variation, attitude shift) | Automatic | [Taubenfeld et al., 2024](#) |
| **Demographic Information** | Bias, fairness, ethics metrics | Exaggeration (normalized average cosine similarity) | Automatic | [Cheng et al., 2023](#) |
| **Demographic Information** | Bias, fairness, ethics metrics | Individuation (classification accuracy) | Automatic | [Cheng et al., 2023](#) |
| **Demographic Information** | Bias, fairness, ethics metrics | Bias (performance disparity, prevalence, magnitude, variation, attitude shift) | Automatic | [Gupta et al., 2024](#) |
| **Demographic Information** | Bias, fairness, ethics metrics | Bias (performance disparity, prevalence, magnitude, variation, attitude shift) | Automatic | [Neuberger et al., 2024](#) |
| **Demographic Information** | Bias, fairness, ethics metrics | Bias (performance disparity, prevalence, magnitude, variation, attitude shift) | Automatic | [Taubenfeld et al., 2024](#) |
| **Demographic Information** | Bias, fairness, ethics metrics | Message toxicity | Automatic | [Fang et al., 2024](#) |
| **Activity History**      | Content and textual metrics   | Coherence | LLM | [Li et al., 2024e](#) |
| **Activity History**      | Content and textual metrics   | Clarity | Human | [Chen et al., 2024b](#) |
| **Activity History**      | Content and textual metrics   | Diversity of dialog (Shannon entropy, intra-remote-clique, inter-remote-clique, semantic similarity, longest common subsequence similarity) | Automatic | [Ha et al., 2024](#) |
| **Belief & Value**       | Content and textual metrics   | Diversity of dialog (Shannon entropy, intra-remote-clique, inter-remote-clique, semantic similarity, longest common subsequence similarity) | Automatic | [Gu et al., 2024](#) |
| **Demographic Information** | Content and textual metrics | Coherence | LLM | [Li et al., 2024e](#) |
| **Demographic Information** | Content and textual metrics | Attitudes (topic term frequency) | Automatic | [Fang et al., 2024](#) |
| **Demographic Information** | Content and textual metrics | Diversity of dialog (Shannon entropy, intra-remote-clique, inter-remote-clique, semantic similarity, longest common subsequence similarity) | Automatic | [Fang et al., 2024](#) |
| **Demographic Information** | Content and textual metrics | Clarity | Human | [Chen et al., 2024b](#) |
| **Demographic Information** | Content and textual metrics | Linguistic complexity (utterance length, Kolmogorov complexity) | Automatic | [Milička et al., 2024](#) |
| **Psychological Traits**  | Content and textual metrics  | Text similarity (BLEU, ROUGE) | Automatic | [Zeng et al., 2024](#) |
| **Psychological Traits**  | Content and textual metrics  | Tone Alignment | LLM | [Zeng et al., 2024](#) |
| **Skills and Expertise**  | Content and textual metrics  | Coherence | LLM | [Li et al., 2024e](#) |
| **Activity History**      | External alignment metrics   | Hallucination | LLM | [Shao et al., 2023](#) |
| **Activity History**      | External alignment metrics   | Entailment | LLM | [Li et al., 2024e](#) |
| **Activity History**      | External alignment metrics   | Believability/Credibility (self-knowledge, memory, plans, reactions, reflections) | Human | [Park et al., 2023](#) |
| **Demographic Information** | External alignment metrics | Entailment | LLM | [Li et al., 2024e](#) |
| **Demographic Information** | External alignment metrics | Believability/Credibility (self-knowledge, memory, plans, reactions, reflections) | Human | [Park et al., 2023](#) |



### Task-oriented evaluation metrics glossary



## Citation
```
```