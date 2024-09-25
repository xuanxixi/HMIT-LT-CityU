# TAP MAS: A Multi-Agent System for Translating and Proofreading Hong Kong Legal Judgments

<p align="center">
  <img src="./Figure1.png" alt="Figure 1" style="display: block; margin: 0 auto;" />
  <br />
  <em>Figure 1: TAP MAS: A Multi-Agent System for Translating and Proofreading Hong Kong Legal Judgments</em>
</p>

## 1. Abstract

We have developed a virtual professional studio using a Multi-Agent System (MAS) as the underlying machine translation (MT) engine to support the HMIT platform for Hong Kong legal judgment translation and proofreading. The overall architecture is illustrated in Figure 1. This system consists of three agents: Translator, Annotator, and Proofreader. Following these traditional translation roles, we refer to the system as TAP MAS, or simply TAP. Each agent in TAP MAS cooperates throughout the entire translation process of a judgment (or any text), ensuring quality and consistency in the final product.

The system is scheduled for launch and will be available at [https://hmit.LT.cityu.edu.hk](https://hmit.LT.cityu.edu.hk).

## 2. Dataset

The dataset used is the **CFA Judgement Corpus 97-22**, which is proposed for the first time in this paper. You can find the dataset at [CFA_Judgement_Corpus_97-22](https://huggingface.co/datasets/xxuan-nlp/CFA_Judgement_Corpus_97-22).

<p align="center">
  <img src="./Figure2.png" alt="Figure 2" style="display: block; margin: 0 auto; width: 50%;" />
  <br />
  <em>Figure 2: Overview of the CFA Judgement Corpus</em>
</p>

## 3. Prompt Engineering

The TAP MAS system utilizes few-shot prompting techniques to guide the three agents. Below is Figure 3, which illustrates the few-shot prompts used in TAP MAS. The green, blue, and red highlights represent the outputs from the Translator (T), Annotator (A), and Proofreader (P) agents, respectively.

<p align="center">
  <img src="./Figure3.png" alt="Figure 3" style="display: block; margin: 0 auto;" />
  <br />
  <em>Figure 3: Illustration of few-shot prompts used in TAP MAS</em>
</p>

## 4. LLM Response Parameter Settings

TAP MAS consists of three agents, and their LLM response parameters are configured as follows:

- Temperature: 0
- Max Tokens: 4,096
- Frequency Penalty: 0
- Presence Penalty: 0

Please refer to my paper for details.

## 5. Experimental Results

### 5.1 Automatic Evaluation

The performance of TAP MAS was evaluated across various configurations of the three agents. Below is the performance summary in Table 1:

<p align="center">
  <img src="./Figure4.png" alt="Figure 4" style="display: block; margin: 0 auto;" />
  <br />
</p>

### 5.2 Human Evaluation

To ensure a comprehensive, adequate, and reliable evaluation of the translation quality of Hong Kong legal judgments, this paper proposes the **ACS metric**. This metric evaluates the translation quality across three key dimensions:

- **A** (Accuracy of legal meaning)
- **C** (Coherence and cohesion in structure)
- **S** (Appropriateness in style)

The results of human evaluation for three representative MT systems are summarized in Table 2:

<p align="center">
  <img src="./Figure5.png" alt="Figure 5" style="display: block; margin: 0 auto;" />
  <br />
</p>

## 6. Publication

This paper is a result of project research, funded by the Hong Kong Research Grants Council. It was oral presented at the [Hong Kong Bilingual Legal System: Retrospect and Prospect Conference](https://www.law.hku.hk/events/conference-on-hong-kong-bilingual-legal-system-retrospect-and-prospect-day-1/) of the Faculty of Law, University of Hong Kong, in August 2023.

The paper will be published in the **Conference Proceeding of 'Hong Kong Bilingual Legal System: Retrospect and Prospect'** (Best Paper Award), at the University of Hong Kong in 2025.

(Authors: Prof. King Kui SIN, Xi Xuan, Prof. Chunyu Kit, Prof. Clara Ho-yan Chan, Prof. Honic Ho-kin Ip)
