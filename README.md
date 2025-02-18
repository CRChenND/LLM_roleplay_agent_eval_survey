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
  - [Relationships Between Agent Attributes and Downstream Tasks](#relationships-between-agent-attributes-and-downstream-tasks)

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

| **Attribute** | **Category**       | **Agent-Oriented Metrics**          | **Approach**      | **Source**                     |
|-------------------|-------------------|-------------------------------------|---------------|----------------------------|
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
| **Demographic Information** | External alignment metrics | Entailment | LLM | [Li et al., 2024e](#) |
| **Demographic Information** | External alignment metrics | Believability/Credibility (self-knowledge, memory, plans, reactions, reflections) | Human | [Park et al., 2023](#) |
| **Psychological Traits**  | External alignment metrics  | Fact Accuracy | LLM | [Zeng et al., 2024](#) |
| **Skills and Expertise**  | External alignment metrics  | Hallucination | LLM | [Shao et al., 2023](#) |
| **Skills and Expertise**  | External alignment metrics  | Entailment | LLM | [Li et al., 2024e](#) |
| **Activity History**      | Internal consistency metrics | Stability | LLM | [Shao et al., 2023](#) |
| **Activity History**      | Internal consistency metrics | Consistency of information | Human | [Chen et al., 2024b](#) |
| **Belief & Value**        | Internal consistency metrics | Attitude shift | LLM | [Wang et al., 2024e](#) |
| **Demographic Information** | Internal consistency metrics | Stability | LLM | [Shao et al., 2023](#) |
| **Demographic Information** | Internal consistency metrics | Attitude shift | LLM | [Neuberger et al., 2024](#) |
| **Demographic Information** | Internal consistency metrics | Attitude shift | LLM | [Taubenfeld et al., 2024](#) |
| **Demographic Information** | Internal consistency metrics | Behavior stability (mean, standard deviation) | Automatic | [Wang et al., 2024g](#) |
| **Demographic Information** | Internal consistency metrics | Consistency of information | Human | [Chen et al., 2024b](#) |
| **Demographic Information** | Internal consistency metrics | Consistency of psychological state / personalities | Human | [Chen et al., 2024b](#) |
| **Demographic Information** | Internal consistency metrics | Consistency of information | Human | [Zeng et al., 2024](#) |
| **Psychological Traits**  | Internal consistency metrics  | Stability | LLM | [Shao et al., 2023](#) |
| **Psychological Traits**  | Internal consistency metrics  | Consistency of information | Human | [Zeng et al., 2024](#) |
| **Psychological Traits**  | Internal consistency metrics  | Consistency of psychological state / personalities | Human | [Zeng et al., 2024](#) |
| **Psychological Traits**  | Internal consistency metrics  | Consistency of information | Human | [Cai et al., 2024](#) |
| **Psychological Traits**  | Internal consistency metrics  | Consistency of psychological state / personalities | Human | [Cai et al., 2024](#) |
| **Skills and Expertise**  | Internal consistency metrics | Stability | LLM | [Shao et al., 2023](#) |
| **Activity History**      | Performance metrics         | Memorization | LLM | [Shao et al., 2023](#) |
| **Demographic Information** | Performance metrics       | Memorization | LLM | [Chen et al., 2024b](#) |
| **Demographic Information** | Performance metrics       | Communication ability (win rates) | Automatic | [Liu et al., 2024a](#) |
| **Demographic Information** | Performance metrics       | Reaction (accuracy) | Automatic | [Liu et al., 2024a](#) |
| **Demographic Information** | Performance metrics       | Self-knowledge (accuracy) | Automatic | [Liu et al., 2024a](#) |
| **Activity History**      | Psychological metrics      | Empathy | Human | [Chen et al., 2024b](#) |
| **Belief & Value**        | Psychological metrics      | Value | LLM | [Shao et al., 2023](#) |
| **Demographic Information** | Psychological metrics     | Personality consistency | Automatic | [Wang et al., 2024c](#) |
| **Demographic Information** | Psychological metrics     | Measured alignment for personality | Human | [Wang et al., 2024c](#) |
| **Demographic Information** | Psychological metrics     | Sentiment | Automatic | [Fang et al., 2024](#) |
| **Demographic Information** | Psychological metrics     | Empathy | Human | [Chen et al., 2024b](#) |
| **Demographic Information** | Psychological metrics     | Belief (stability, evolution, correlation with behavior) | Automatic | [Lei et al., 2024](#) |
| **Psychological Traits**  | Psychological metrics  | Personality | Automatic | [Shao et al., 2023](#) |
| **Psychological Traits**  | Psychological metrics  | Belief (stability, evolution, correlation with behavior) | Automatic | [Shao et al., 2023](#) |
| **Psychological Traits**  | Psychological metrics  | Emotion responses (entropy of valence and arousal) | Automatic | [Shao et al., 2023](#) |
| **Psychological Traits**  | Psychological metrics  | Personality (Machine Personality Inventory, PsychoBench) | Automatic | [Jiang et al., 2023a](#) |
| **Psychological Traits**  | Psychological metrics  | Personality (vignette tests) | Human | [Jiang et al., 2023a](#) |
| **Belief & Value**        | Social and decision-making metrics | Social value orientation (SVO-based Value Rationality Measurement) | Automatic | [Zhang et al., 2023b](#) |


### Task-oriented evaluation metrics glossary

| **Task** | **Category**     | **Task-Oriented Metrics**    | **Approach**  | **Source**  |
|----------|---------|-------------------------|-----------|---------|
| **Decision Making** | Social and economic metrics| Negotiation (Concession Rate, Negotiation Success Rate, Average Negotiation Round) | Automatic | [Huang and Hadfi, 2024](#) |
| **Decision Making** | Social and economic metrics| Societal Satisfaction (average per-capita living area size, average waiting time, social welfare) | Automatic | [Ji et al., 2024](#) |
| **Decision Making** | Social and economic metrics| Societal Fairness (variance in per capita living area size, number of inverse order pairs in house allocation, Gini coefficient) | Automatic | [Ji et al., 2024](#) |
| **Decision Making** | Social and economic metrics| Macroeconomic (Inflation rate, Unemployment rate, Nominal GDP, Nominal GDP growth, Wage inflation, Real GDP growth, Expected monthly income, Consumption) | Automatic | [Li et al., 2024d](#) |
| **Decision Making** | Social and economic metrics| Market and Consumer (Purchase probability, Expected competing product price, Customer counts, Price consistency between competitors) | Automatic | [Gui and Toubia, 2023](#) |
| **Decision Making** | Social and economic metrics| Market and Consumer (Purchase probability, Expected competing product price, Customer counts, Price consistency between competitors) | Automatic | [Zhao et al., 2023](#) |
| **Decision Making** | Social and economic metrics| Probability weighting | Automatic | [Jia et al., 2024](#) |
| **Decision Making** | Social and economic metrics| Utility (Intrinsic Utility, Joint Utility) | Automatic | [Huang and Hadfi, 2024](#) |
| **Decision Making** | Psychological metrics| Level of trust (distribution of amounts sent, trust rate) | Automatic | [Xie et al., 2024a](#) |
| **Decision Making** | Psychological metrics| Risk preference | Automatic | [Jia et al., 2024](#) |
| **Decision Making** | Psychological metrics| Loss aversion | Automatic | [Jia et al., 2024](#) |
| **Decision Making** | Psychological metrics| Selfishness (Selfishness Index, Difference Index) | Automatic | [Kim et al., 2024](#) |
| **Decision Making** | Performance metrics| Frequency (distribution of expert type) | Automatic | [Wang et al., 2024b](#) |
| **Decision Making** | Performance metrics| Valid response rate | Automatic | [Xie et al., 2024a](#) |
| **Decision Making** | Performance metrics| Web search quality (Mean reciprocal rank, Mean reciprocal rank) | Automatic | [Ren et al., 2024a](#) |
| **Decision Making** | Performance metrics| Performance deviations/alignment from the baseline (accuracy, Jaccard Index, Cohen’s Kappa Coefficient, Percentage Agreement, overlapping ratio between prediction and targets) | Automatic | [Kim et al., 2024](#) |
| **Decision Making** | Performance metrics| Performance deviations/alignment from the baseline (accuracy, Jaccard Index, Cohen’s Kappa Coefficient, Percentage Agreement, overlapping ratio between prediction and targets) | Automatic | [Jin et al., 2024](#) |
| **Decision Making** | Performance metrics| Performance deviations/alignment from the baseline (accuracy, Jaccard Index, Cohen’s Kappa Coefficient, Percentage Agreement, overlapping ratio between prediction and targets) | Automatic | [Wang et al., 2024b](#) |
| **Decision Making** | Performance metrics| Performance deviations/alignment from the baseline (accuracy, Jaccard Index, Cohen’s Kappa Coefficient, Percentage Agreement, overlapping ratio between prediction and targets) | Automatic | [Wang et al., 2024f](#) |
| **Decision Making** | Internal consistency metrics| Behavioral alignment (lottery rate, behavior dynamic, Imitation and differentiation behavior, Proportion of similar and different dishes) | Automatic | [Xie et al., 2024a](#) |
| **Decision Making**    | Internal consistency metrics| Behavioral alignment (lottery rate, behavior dynamic, Imitation and differentiation behavior, Proportion of similar and different dishes) | Automatic | [Zhao et al., 2023](#) |
| **Decision Making**    | Internal consistency metrics| Cultural appropriateness (Alignment between persona information and its assigned nationality) | LLM | [Li et al., 2024e](#) |
| **Decision Making**    | External alignment metrics| Factual hallucinations (String matching overlap ratio) | Automatic | [Wang et al., 2024f](#) |
| **Decision Making**    | External alignment metrics| Simulation capability (Turing test) | Human | [Ji et al., 2024](#) |
| **Decision Making**    | External alignment metrics| Entailment | LLM | [Li et al., 2024e](#) |
| **Decision Making**    | External alignment metrics| Realism | LLM | [Li et al., 2024e](#) |
| **Educational Training** | Psychological metrics| Perceived reflection on the development of essential non-cognitive skills | Human | [Yan et al., 2024](#) |
| **Educational Training** | Psychological metrics| Non-cognitive skill scale | Automatic | [Yan et al., 2024](#) |
| **Educational Training** | Psychological metrics| Sense of immersion / Perceived immersion | Human | [Lee et al., 2023](#) |
| **Educational Training** | Psychological metrics| Perceived intelligence | Human | [Cheng et al., 2024](#) |
| **Educational Training** | Psychological metrics| Perceived enjoyment | Human | [Cheng et al., 2024](#) |
| **Educational Training** | Psychological metrics| Perceived trust | Human | [Cheng et al., 2024](#) |
| **Educational Training** | Psychological metrics| Perceived sense of connection | Human | [Cheng et al., 2024](#) |
| **Educational Training** | Psychological metrics| Personality (Big Five Inventory, MBTI score, SD3 score, Linguistic Inquiry and Word Count framework, HEXACO) | Automatic | [Sonlu et al., 2024](#) |
| **Educational Training** | Psychological metrics| Personality (Big Five Inventory, MBTI score, SD3 score, Linguistic Inquiry and Word Count framework, HEXACO) | Automatic | [Liu et al., 2024d](#) |
| **Educational Training** | Psychological metrics| Perceived usefulness | Human | [Cheng et al., 2024](#) |
| **Educational Training** | Performance metrics| Density of knowledge-building | Automatic | [Jin et al., 2023](#) |
| **Educational Training** | Performance metrics| Effectiveness of questioning | Human | [Shi et al., 2023](#) |
| **Educational Training** | Performance metrics| Success criterion function outputs before operation and after operation | Human | [Li et al., 2023a](#) |
| **Educational Training** | External alignment metrics| Knowledge level (reconfigurability, persistence, and adaptability) | Automatic | [Jin et al., 2023](#) |
| **Educational Training** | External alignment metrics| Perceived human-likeness | Human | [Cheng et al., 2024](#) |
| **Educational Training** | Content and textual metrics| Story Content Generation (narratives staging score) | Automatic | [Yan et al., 2024](#) |
| **Educational Training** | Content and textual metrics| Willingness to speak | Human | [Shi et al., 2023](#) |
| **Educational Training** | Content and textual metrics| Authenticity | Human | [Lee et al., 2023](#) |
| **Opinion Dynamics**    | Psychological metrics| Opinion change | Human | [Triem and Ding, 2024](#) |
| **Opinion Dynamics**    | Psychological metrics| Emotional density | Automatic | [Gao et al., 2023](#) |
| **Opinion Dynamics**    | Performance metrics| Prediction accuracy (F1 score, AUC, MSE, MAE, depression risk prediction accuracy, suicide risk prediction accuracy) | Automatic | [Gao et al., 2023](#) |
| **Opinion Dynamics** | Performance metrics| Prediction accuracy (F1 score, AUC, MSE, MAE, depression risk prediction accuracy, suicide risk prediction accuracy) | Automatic | [Mou et al., 2024c](#) |
| **Opinion Dynamics** | Performance metrics| Prediction accuracy (F1 score, AUC, MSE, MAE, depression risk prediction accuracy, suicide risk prediction accuracy) | Automatic | [Yu et al., 2024](#) |
| **Opinion Dynamics** | Performance metrics| Classification accuracy | Human | [Chan et al., 2023](#) |
| **Opinion Dynamics** | Performance metrics| Rephrase accuracy | Automatic | [Ju et al., 2024](#) |
| **Opinion Dynamics** | Performance metrics| Legal articles evaluation (precision, recall, F1) | Automatic | [He et al., 2024a](#) |
| **Opinion Dynamics** | Performance metrics| Judgment evaluation for civil and administrative cases (precision, recall, F1) | Automatic | [He et al., 2024a](#) |
| **Opinion Dynamics** | Performance metrics| Judgment evaluation for criminal cases (accuracy) | Automatic | [He et al., 2024a](#) |
| **Opinion Dynamics** | Performance metrics| Prediction error rate | Automatic | [Gao et al., 2023](#) |
| **Opinion Dynamics** | Performance metrics| Locality accuracy | Automatic | [Ju et al., 2024](#) |
| **Opinion Dynamics** | Performance metrics| Decision probability | Human | [Triem and Ding, 2024](#) |
| **Opinion Dynamics** | Performance metrics| Decision volatility | Human | [Triem and Ding, 2024](#) |
| **Opinion Dynamics** | Performance metrics| Case complexity | Human | [Triem and Ding, 2024](#) |
| **Opinion Dynamics** | Performance metrics| Alignment (compare simulation results with actual social outcomes) | Automatic | [Wang et al., 2024g](#) |
| **Opinion Dynamics** | Internal consistency metrics| Alignment (stance, content, behavior, static attitude distribution, time series of the average attitude) | Automatic | [Mou et al., 2024c](#) |
| **Opinion Dynamics** | Internal consistency metrics| Personality-behavior alignment | Human | [Navarro et al., 2024](#) |
| **Opinion Dynamics** | Internal consistency metrics| Similarity between initial and post preference (KL-divergence, RMSE) | Automatic | [Namikoshi et al., 2024](#) |
| **Opinion Dynamics** | Internal consistency metrics| Role playing | Human | [Lv et al., 2024](#) |
| **Opinion Dynamics** | External alignment metrics| Correctness | Human | [He et al., 2024a](#) |
| **Opinion Dynamics** | External alignment metrics| Accuracy (correctness) | Automatic | [Ju et al., 2024](#) |
| **Opinion Dynamics** | External alignment metrics| Logicality | Human | [He et al., 2024a](#) |
| **Opinion Dynamics** | External alignment metrics| Concision | Human | [He et al., 2024a](#) |
| **Opinion Dynamics** | External alignment metrics| Human likeness index | Automatic | [Chuang et al., 2023b](#) |
| **Opinion Dynamics** | External alignment metrics| Alignment between model and human (Kappa correlation coefficient, MAE), Authenticity (alignment of ratings between the agent and human annotators) | Human | [Chan et al., 2023](#) |
| **Opinion Dynamics** | External alignment metrics| Alignment between model and human (Kappa correlation coefficient, MAE), Authenticity (alignment of ratings between the agent and human annotators) | Human | [Triem and Ding, 2024](#) |
| **Opinion Dynamics** | External alignment metrics| Alignment between model and human (Kappa correlation coefficient, MAE), Authenticity (alignment of ratings between the agent and human annotators) | Human | [Lv et al., 2024](#) |
| **Opinion Dynamics** | Content and textual metrics| Turn-level Kendall-Tau correlation (naturalness, coherence, engagingness, and groundedness) | Automatic | [Chan et al., 2023](#) |
| **Opinion Dynamics**       | Content and textual metrics| Turn-level Spearman correlation (naturalness, coherence, engagingness, and groundedness) | Automatic | [Chan et al., 2023](#) |
| **Opinion Dynamics**       | Bias, fairness, and ethics metrics| Partisan bias | Automatic | [Chuang et al., 2023b](#) |
| **Opinion Dynamics**       | Bias, fairness, and ethics metrics| Bias (cultural, linguistic, economic, demographic, ideological) | Automatic | [Qu and Wang, 2024](#) |
| **Opinion Dynamics**       | Bias, fairness, and ethics metrics| Bias (mean) | Automatic | [Chuang et al., 2023a](#) |
| **Opinion Dynamics**       | Bias, fairness, and ethics metrics| Extreme values | Automatic | [Chuang et al., 2023b](#) |
| **Opinion Dynamics**       | Bias, fairness, and ethics metrics| Wisdom of Partisan Crowds effect | Automatic | [Chuang et al., 2023b](#) |
| **Opinion Dynamics**       | Bias, fairness, and ethics metrics| Opinion diversity | Automatic | [Chuang et al., 2023a](#) |
| **Psychological Experiment** | Social and economic metrics| Money allocation | Automatic | [Lei et al., 2024](#) |
| **Psychological Experiment** | Psychological metrics| Attitude change | Automatic | [Wang et al., 2025a](#) |
| **Psychological Experiment** | Psychological metrics| Average happiness value per time step | Automatic | [He and Zhang, 2024](#) |
| **Psychological Experiment** | Psychological metrics| Belief value | Automatic | [Lei et al., 2024](#) |
| **Psychological Experiment** | Psychological metrics| Personality (Big Five Inventory, MBTI score, SD3 score, Linguistic Inquiry and Word Count framework, HEXACO) | Automatic | [He and Zhang, 2024](#) |
| **Psychological Experiment** | Psychological metrics| Personality (Big Five Inventory, MBTI score, SD3 score, Linguistic Inquiry and Word Count framework, HEXACO) | Automatic | [de Winter et al., 2024](#) |
| **Psychological Experiment** | Psychological metrics| Personality (Big Five Inventory, MBTI score, SD3 score, Linguistic Inquiry and Word Count framework, HEXACO) | Automatic | [Bose et al., 2024](#) |
| **Psychological Experiment** | Psychological metrics| Personality (Big Five Inventory, MBTI score, SD3 score, Linguistic Inquiry and Word Count framework, HEXACO) | Automatic | [Jiang et al., 2023b](#) |
| **Psychological Experiment** | Psychological metrics| Longitudinal trajectories of emotions | Automatic | [De Duro et al., 2025](#) |
| **Psychological Experiment** | Psychological metrics| Valence entropy | Automatic | [Lei et al., 2024](#) |
| **Psychological Experiment** | Psychological metrics| Arousal entropy | Automatic | [Lei et al., 2024](#) |
| **Psychological Experiment** | Performance metrics| Precision of item recommendation | Automatic | [Wang et al., 2025a](#) |
| **Psychological Experiment** | Performance metrics| Missing rate | Automatic | [Lei et al., 2024](#) |
| **Psychological Experiment** | Performance metrics| Rejection rate | Automatic | [Lei et al., 2024](#) |
| **Psychological Experiment** | Internal consistency metrics| Correlation between social dilemma game outcome and agent personality | Automatic | [Bose et al., 2024](#) |
| **Psychological Experiment** | Internal consistency metrics| Behavioral similarity | Automatic | [Li et al., 2024b](#) |
| **Psychological Experiment** | Internal consistency metrics| Perception consistency (agent perceived safety, agent perceived liveliness) | LLM | [Verma et al., 2023](#) |
| **Psychological Experiment** | External alignment metrics| Rationality of the agent memory | Automatic | [Wang et al., 2025a](#) |
| **Psychological Experiment** | External alignment metrics| Believability of behavior | Automatic | [Wang et al., 2025a](#) |
| **Psychological Experiment** | Content and textual metrics| Salience of individual words | Automatic | [De Duro et al., 2025](#) |
| **Psychological Experiment** | Content and textual metrics| Absolutist words | Automatic | [De Duro et al., 2025](#) |
| **Psychological Experiment** | Content and textual metrics| Personal pronouns or emotions | Automatic | [De Duro et al., 2025](#) |
| **Psychological Experiment** | Content and textual metrics| Information entropy | Automatic | [Wang et al., 2025a](#) |
| **Psychological Experiment** | Content and textual metrics| Story (readability, personalness, redundancy, cohesiveness, likeability, believability) | Human | [Jiang et al., 2023b](#) |
| **Psychological Experiment** | Content and textual metrics| Story (readability, personalness, redundancy, cohesiveness, likeability, believability) | LLM | [Jiang et al., 2023b](#) |
| **Simulated Individual** | Social and economic metrics| Numbers of generated peer support strategies | Automatic | [Liu et al., 2024b](#) |
| **Simulated Individual** | Social and economic metrics| Perceived social support questionnaire | Human | [Liu et al., 2024b](#) |
| **Simulated Individual** | Psychological metrics| Emotions | Human | [Pataranutaporn et al., 2024](#) |
| **Simulated Individual** | Psychological metrics| Agency | Human | [Pataranutaporn et al., 2024](#) |
| **Simulated Individual** | Psychological metrics| Future consideration | Human | [Pataranutaporn et al., 2024](#) |
| **Simulated Individual** | Psychological metrics| Self-reflection | Human | [Pataranutaporn et al., 2024](#) |
| **Simulated Individual** | Psychological metrics| Insight | Human | [Pataranutaporn et al., 2024](#) |
| **Simulated Individual** | Psychological metrics| Persona Perception Scale | Human | [Salminen et al., 2024](#) |
| **Simulated Individual** | Psychological metrics| Persona Perception Scale | Human | [Shin et al., 2024](#) |
| **Simulated Individual** | Psychological metrics| Persona Perception Scale | Human | [Ha et al., 2024](#) |
| **Simulated Individual** | Psychological metrics| Persona Perception Scale | Human | [Chen et al., 2024b](#) |
| **Simulated Individual** | Psychological metrics| Engagement | Human | [Zhang et al., 2024a](#) |
| **Simulated Individual** | Psychological metrics| Safety | Human | [Zhang et al., 2024a](#) |
| **Simulated Individual** | Psychological metrics| Sensitivity to personalization | Automatic | [Giorgi et al., 2024](#) |
| **Simulated Individual** | Psychological metrics| Agent self-awareness | LLM | [Xie et al., 2024b](#) |
| **Simulated Individual** | Psychological metrics| Personality (Big Five Inventory rated by LLM) | LLM | [Jiang et al., 2023a](#) |
| **Simulated Individual** | Psychological metrics| Positively mention rate | Automatic | [Kamruzzaman and Kim, 2024](#) |
| **Simulated Individual** | Psychological metrics| Optimism | Human | [Pataranutaporn et al., 2024](#) |
| **Simulated Individual** | Psychological metrics| Self-esteem | Human | [Pataranutaporn et al., 2024](#) |
| **Simulated Individual** | Psychological metrics| Pressure perceived scale | Human | [Liu et al., 2024b](#) |
| **Simulated Individual** | Performance metrics| Error rates (error of average, error of dispersion) | Automatic | [Lin et al., 2024](#) |
| **Simulated Individual** | Performance metrics| Model fit indices (Chi-square to degrees of freedom ratio, Comparative Fit Index, Tucker-Lewis Index, Root Mean Square Error of Approximation) | Automatic | [Ke and Ng, 2024](#) |
| **Simulated Individual** | Performance metrics| Knowledge accuracy (WikiRoleEval with human evaluators) | Human | [Tang et al., 2024](#) |
| **Simulated Individual** | Performance metrics| Knowledge accuracy (WikiRoleEval) | LLM | [Tang et al., 2024](#) |
| **Simulated Individual** | Performance metrics| Win rates | Automatic | [Chi et al., 2024](#) |
| **Simulated Individual** | Performance metrics| Comprehension | Automatic | [Shin et al., 2024](#) |
| **Simulated Individual** | Performance metrics| Completeness | Automatic | [Shin et al., 2024](#) |
| **Simulated Individual** | Performance metrics| Validity (average variance extracted, inter-construct correlations) | Automatic | [Ke and Ng, 2024](#) |
| **Simulated Individual** | Performance metrics| Composite reliability | Automatic | [Ke and Ng, 2024](#) |
| **Simulated Individual** | Performance metrics| Rated statement quality | Human | [Liu et al., 2023](#) |
| **Simulated Individual** | Performance metrics| Rated statement quality | LLM | [Liu et al., 2023](#) |
| **Simulated Individual** | Performance metrics| Conversational ability (CharacterEval) | LLM | [Tang et al., 2024](#) |
| **Simulated Individual** | Performance metrics| Roleplay subset of MT-Bench | LLM | [Tang et al., 2024](#) |
| **Simulated Individual** | Performance metrics| Professional scale (accuracy in replicating profession-specific knowledge) | LLM | [Sun et al., 2024](#) |
| **Simulated Individual** | Performance metrics| Language quality | LLM | [Zhang et al., 2024a](#) |
| **Simulated Individual** | Performance metrics| Prediction accuracy between real data and generated data (Replication success rate, Kullback-Leibler divergence) | Automatic | [Assaf and Lynar, 2024](#) |
| **Simulated Individual** | Performance metrics| Prediction accuracy between real data and generated data (Replication success rate, Kullback-Leibler divergence) | Automatic | [Tamaki and Littvay, 2024](#) |
| **Simulated Individual** | Performance metrics| Prediction accuracy between real data and generated data (Replication success rate, Kullback-Leibler divergence) | Automatic | [Park et al., 2024](#) |
| **Simulated Individual** | Performance metrics| Prediction accuracy between real data and generated data (Replication success rate, Kullback-Leibler divergence) | Automatic | [Yeykelis et al., 2024](#) |
| **Simulated Individual** | Performance metrics| Accuracy of distinguishing between AI-generated and human-built solutions | Automatic | [Schuller et al., 2024](#) |
| **Simulated Individual** | Internal consistency metrics| Accuracy of reaction based on social relationship | Automatic | [Liu et al., 2024a](#) |
| **Simulated Individual** | Internal consistency metrics| Perceived connection between personas and system outcomes | Human | [Chen et al., 2024b](#) |
| **Simulated Individual** | Internal consistency metrics| Representativeness (Wasserstein distance, respond with similar answers to individual survey questions), Consistency (Frobenius norm, the correlation across responses to a set of questions in each survey) | Automatic | [Moon et al., 2024](#) |
| **Simulated Individual** | Internal consistency metrics| Role consistency (WikiRoleEval with human evaluators) | Human | [Tang et al., 2024](#) |
| **Simulated Individual** | Internal consistency metrics| Role consistency/attractiveness (WikiRoleEval, CharacterEval) | LLM | [Tang et al., 2024](#) |
| **Simulated Individual** | Internal consistency metrics| Consistency | Human | [Zhang et al., 2024a](#) |
| **Simulated Individual** | Internal consistency metrics| Consistency | Human | [Mishra et al., 2023](#) |
| **Simulated Individual** | Internal consistency metrics| Future self-continuity | Human | [Pataranutaporn et al., 2024](#) |
| **Simulated Individual** | Internal consistency metrics| Agreement between a synthetic annotator both with and without a leave-one-out attribute (Cohen’s Kappa) | Automatic | [Castricato et al., 2024](#) |
| **Simulated Individual** | Internal consistency metrics| Consistency with the scenario and characters | Automatic | [Zhang et al., 2024a](#) |
| **Simulated Individual** | Internal consistency metrics| Quality and logical coherence of the script content | Automatic | [Zhang et al., 2024a](#) |
| **Simulated Individual** | Internal consistency metrics| Nation-related response percentage | Automatic | [Kamruzzaman and Kim, 2024](#) |
| **Simulated Individual** | External alignment metrics| Unknown question rejection (WikiRoleEval with human evaluators) | Human | [Tang et al., 2024](#) |
| **Simulated Individual** | External alignment metrics| Unknown question rejection (WikiRoleEval) | LLM | [Tang et al., 2024](#) |
| **Simulated Individual** | External alignment metrics| Accuracy of self-knowledge | Automatic | [Liu et al., 2024a](#) |
| **Simulated Individual** | External alignment metrics| Correctness | Human | [Zhang et al., 2024a](#) |
| **Simulated Individual** | External alignment metrics| Correctness | Human | [Milička et al., 2024](#) |
| **Simulated Individual** | External alignment metrics| Agreement score between human raters and LLM | Automatic | [Liu et al., 2023](#) |
| **Simulated Individual** | External alignment metrics| Agreement score between human raters and LLM | Automatic | [Jiang et al., 2023a](#) |
| **Simulated Individual** | External alignment metrics| Agreement score between human raters and LLM | Automatic | [Liu et al., 2024a](#) |
| **Simulated Individual** | External alignment metrics| Human-likeness | Human | [Zhang et al., 2024a](#) |
| **Simulated Individual** | Content and textual metrics| Content similarity (ROUGE-L, BERTScore, GPT-based similarity, G-eval) | Automatic | [Shin et al., 2024](#) |
| **Simulated Individual** | Content and textual metrics| Entity density of summarization | Automatic | [Liu et al., 2024a](#) |
| **Simulated Individual** | Content and textual metrics| Entity recall of summarization | Automatic | [Liu et al., 2024a](#) |
| **Simulated Individual** | Content and textual metrics| Dialog diversity | Automatic | [Lin et al., 2024](#) |
| **Simulated Individual** | Bias, fairness, and ethics metrics| Hate speech detection accuracy | Automatic | [Giorgi et al., 2024](#) |
| **Simulated Individual** | Bias, fairness, and ethics metrics| Population heterogeneity | Automatic | [Murthy et al., 2024](#) |
| **Simulated Society** | Social and economic metrics| Social Conflict Count | Automatic | [Ren et al., 2024b](#) |
| **Simulated Society** | Social and economic metrics| Social Rules | Human | [Zhou et al., 2024b](#) |
| **Simulated Society** | Social and economic metrics| Social Rules | LLM | [Zhou et al., 2024b](#) |
| **Simulated Society** | Social and economic metrics| Financial and Material Benefits | Human | [Zhou et al., 2024b](#) |
| **Simulated Society** | Social and economic metrics| Financial and Material Benefits | LLM | [Zhou et al., 2024b](#) |
| **Simulated Society** | Social and economic metrics| Converged price | Automatic | [Toledo-Zucco et al., 2024](#) |
| **Simulated Society** | Social and economic metrics| Information diffusion | Automatic | [Park et al., 2023](#) |
| **Simulated Society** | Social and economic metrics| Relationship formation | Automatic | [Park et al., 2023](#) |
| **Simulated Society** | Social and economic metrics| Relationship | LLM | [Zhou et al., 2024b](#) |
| **Simulated Society** | Social and economic metrics| Coordination within other agents | Automatic | [Park et al., 2023](#) |
| **Simulated Society** | Social and economic metrics| Probability of social connection formation | Automatic | [Leng and Yuan, 2024](#) |
| **Simulated Society** | Social and economic metrics| Percent of social welfare maximization choices | Automatic | [Leng and Yuan, 2024](#) |
| **Simulated Society** | Social and economic metrics| Persuasion (distribution of persuasion outcomes, odds ratios) | Automatic | [Campedelli et al., 2024](#) |
| **Simulated Society** | Social and economic metrics| Anti-social behavior (effect on toxic messages) | Automatic | [Campedelli et al., 2024](#) |
| **Simulated Society** | Social and economic metrics| Norm Internalization Rate | Automatic | [Ren et al., 2024b](#) |
| **Simulated Society** | Social and economic metrics| Norm Compliance Rate | Automatic | [Ren et al., 2024b](#) |
| **Simulated Society** | Psychological metrics| NASA-TLX Scores | Human | [Zhang et al., 2024c](#) |
| **Simulated Society** | Psychological metrics| Helpfulness rating | Human | [Zhang et al., 2024c](#) |
| **Simulated Society** | Psychological metrics| Personality (Big Five Inventory, MBTI score, SD3 score, Linguistic Inquiry and Word Count framework, HEXACO) | Automatic | [Frisch and Giulianelli, 2024](#) |
| **Simulated Society** | Psychological metrics| Personality (Big Five Inventory, MBTI score, SD3 score, Linguistic Inquiry and Word Count framework, HEXACO) | Automatic | [Li et al., 2024b](#) |
| **Simulated Society** | Psychological metrics| Degree of reciprocity | Automatic | [Leng and Yuan, 2024](#) |
| **Simulated Society** | Psychological metrics| Pleasure rating | Human | [Zhang et al., 2024c](#) |
| **Simulated Society** | Psychological metrics| Trend of Favorability Decline | Automatic | [Gu et al., 2024](#) |
| **Simulated Society** | Psychological metrics| Negative Favorability Achievement | Automatic | [Gu et al., 2024](#) |
| **Simulated Society** | Psychological metrics| Trend of Favorability Decline | Automatic | [Gu et al., 2024](#) |
| **Simulated Society** | Psychological metrics| Negative Favorability Achievement | Automatic | [Gu et al., 2024](#) |
| **Simulated Society** | Performance metrics| Abstention accuracy | Automatic | [Ashkinaze et al., 2024](#) |
| **Simulated Society** | Performance metrics| Accuracy of information gathering | Automatic | [Kaiya et al., 2023](#) |
| **Simulated Society** | Performance metrics| Implicit reasoning accuracy | Automatic | [Mou et al., 2024b](#) |
| **Simulated Society** | Performance metrics| Prediction accuracy (F1 score, AUC, MSE, MAE, depression risk prediction accuracy, suicide risk prediction accuracy) | Automatic | [Lan et al., 2024](#) |
| **Simulated Society** | Performance metrics| Guess accuracy | Automatic | [Leng and Yuan, 2024](#) |
| **Simulated Society** | Performance metrics| Classification accuracy | Automatic | [Li et al., 2024a](#) |
| **Simulated Society** | Performance metrics| Success rate | Automatic | [Kaiya et al., 2023](#) |
| **Simulated Society** | Performance metrics| Success rate | Automatic | [Li et al., 2023b](#) |
| **Simulated Society** | Performance metrics| Success rate | Automatic | [Li et al., 2023b](#) |
| **Simulated Society** | Performance metrics| Success rate for coordination (identification accuracy, workflow correctness, alignment between job and agent’s skill) | Automatic | [Li et al., 2023a](#) |
| **Simulated Society** | Performance metrics| Success rate for coordination (identification accuracy, workflow correctness, alignment between job and agent’s skill) | Automatic | [Li et al., 2023a](#) |
| **Simulated Society** | Performance metrics| Task Accuracy | Automatic | [Zhang et al., 2023a](#) |
| **Simulated Society** | Performance metrics| Task Accuracy | Automatic | [Lan et al., 2024](#) |
| **Simulated Society** | Performance metrics| Errors in the prompting sequence | Human | [Antunes et al., 2023](#) |
| **Simulated Society** | Performance metrics| Error-free execution | Automatic | [Wang et al., 2024a](#) |
| **Simulated Society** | Performance metrics| Goal completion | Human | [Mou et al., 2024b](#) |
| **Simulated Society** | Performance metrics| Goal completion | LLM | [Zhou et al., 2024a](#) |
| **Simulated Society** | Performance metrics| Goal completion | LLM | [Mou et al., 2024b](#) |
| **Simulated Society** | Performance metrics| Goal completion | LLM | [Zhou et al., 2024b](#) |
| **Simulated Society** | Performance metrics| Efficacy | Human | [Ashkinaze et al., 2024](#) |
| **Simulated Society** | Performance metrics| Knowledge | Human | [Zhou et al., 2024b](#) |
| **Simulated Society** | Performance metrics| Knowledge | LLM | [Zhou et al., 2024b](#) |
| **Simulated Society** | Performance metrics| Reasoning abilities | Automatic | [Chen et al., 2023](#) |
| **Simulated Society** | Performance metrics| Reasoning abilities | Human | [Chen et al., 2023](#) |
| **Simulated Society** | Performance metrics| Efficiency | Automatic | [Piatti et al., 2024](#) |
| **Simulated Society** | Performance metrics| Text understanding and creative writing abilities (Dialogue response dataset, Commongen Challenge) | LLM | [Chen et al., 2023](#) |
| **Simulated Society** | Performance metrics| Probabilities of receiving, storing, and retrieving the key information across the population | Automatic | [Kaiya et al., 2023](#) |
| **Simulated Society** | Performance metrics| Correlation between predicted and real results | Automatic | [Mitsopoulos et al., 2024](#) |
| **Simulated Society** | Internal consistency metrics| Behavioral similarity | Automatic | [Li et al., 2024b](#) |
| **Simulated Society** | Internal consistency metrics| Semantic consistency (cosine similarity) | Automatic | [Qiu and Lan, 2024](#) |
| **Simulated Society** | External alignment metrics| Alignment (Environmental understanding and response accuracy, adherence to predefined settings) | Automatic | [Gu et al., 2024](#) |
| **Simulated Society** | External alignment metrics| Strategy accuracy (strategies provided by the models vs. by human experts and evaluate the accuracy) | Automatic | [Zhang et al., 2024b](#) |
| **Simulated Society** | External alignment metrics| Believability of behavior | Human | [Zhou et al., 2024b](#) |
| **Simulated Society** | External alignment metrics| Believability of behavior | Human | [Park et al., 2023](#) |
| **Simulated Society** | Content and textual metrics| Content similarity (ROUGE-L, BERTScore, GPT-based similarity, G-eval, BLEU-4) | Automatic | [Li et al., 2024a](#) |
| **Simulated Society** | Content and textual metrics| Content similarity (ROUGE-L, BERTScore, GPT-based similarity, G-eval) | Automatic | [Chen et al., 2024f](#) |
| **Simulated Society** | Content and textual metrics| Content similarity (ROUGE-L, BERTScore, GPT-based similarity, G-eval) | Automatic | [Mishra et al., 2023](#) |
| **Simulated Society** | Content and textual metrics| Semantic understanding | Automatic | [Gu et al., 2024](#) |
| **Simulated Society** | Content and textual metrics| Complexity of generated content | Automatic | [Antunes et al., 2023](#) |
| **Simulated Society** | Content and textual metrics| Dialogue generation quality | Automatic | [Antunes et al., 2023](#) |
| **Simulated Society** | Content and textual metrics| Number of conversation rounds | Automatic | [Zhang et al., 2024c](#) |
| **Simulated Society** | Bias, fairness, and ethics metrics| Bias rate (herd effect, authority effect, Ben Franklin effect, rumor chain effect, gambler’s fallacy, confirmation bias, halo effect) | Human | [Liu et al., 2025](#) |
| **Simulated Society** | Bias, fairness, and ethics metrics| Bias rate (herd effect, authority effect, Ben Franklin effect, rumor chain effect, gambler’s fallacy, confirmation bias, halo effect) | LLM | [Liu et al., 2025](#) |
| **Simulated Society** | Bias, fairness, and ethics metrics| Bias rate (herd effect, authority effect, Ben Franklin effect, rumor chain effect, gambler’s fallacy, confirmation bias, halo effect) | Automatic | [Liu et al., 2025](#) |
| **Simulated Society** | Bias, fairness, and ethics metrics| Equality | Automatic | [Piatti et al., 2024](#) |
| **Writing**  | Psychological metrics| Qualitative feedback (expertise, social relation, valence, level of involvement) | Human | [Benharrak et al., 2024](#) |
| **Writing**  | Performance metrics| Prediction accuracy (F1 score, AUC, MSE, MAE, depression risk prediction accuracy, suicide risk prediction accuracy) | Automatic | [Wang et al., 2024f](#) |
| **Writing**  | Performance metrics| Success rate | Automatic | [Wang et al., 2024d](#) |
| **Writing**  | Performance metrics| Behavioral patterns | Human | [Zhang et al., 2024c](#) |
| **Writing**  | Internal consistency metrics| Consistency (user profile, psychotherapeutic approach) | Automatic | [Mishra et al., 2023](#) |
| **Writing**  | Internal consistency metrics| Motivational consistency | LLM | [Wang et al., 2024d](#) |
| **Writing**  | Internal consistency metrics| Audience similarity | Human | [Choi et al., 2024](#) |
| **Writing**  | Internal consistency metrics| Quality of generated dimension & values (relevance, mutual exclusiveness) | Human | [Choi et al., 2024](#) |
| **Writing**  | External alignment metrics| Factual error rate | Automatic | [Wang et al., 2024f](#) |
| **Writing**  | External alignment metrics| Correctness (politeness, interpersonal behavior) | Automatic | [Mishra et al., 2023](#) |
| **Writing**  | External alignment metrics| Hallucination (groundedness of the chat responses) | Human | [Choi et al., 2024](#) |
| **Writing**  | Content and textual metrics| Linguistic similarity | Human | [Choi et al., 2024](#) |
| **Writing**  | Content and textual metrics| Fluency | Human | [Mishra et al., 2023](#) |
| **Writing**  | Content and textual metrics| Perplexity | Automatic | [Mishra et al., 2023](#) |
| **Writing**  | Content and textual metrics| Non-Repetitiveness | Human | [Mishra et al., 2023](#) |
| **Writing**  | Content and textual metrics| Response generation quality | Automatic | [Li et al., 2024a](#) |
| **Writing**  | Content and textual metrics| Coherency | LLM | [Wang et al., 2024d](#) |

## Relationships Between Agent Attributes and Downstream Tasks

![Relationships between agent attributes and downstream tasks. The numbers in the heatmap represent the paper counts](assets/heatmap.png)

Relationships between agent attributes and downstream tasks. The numbers in the heatmap represent the paper counts.

