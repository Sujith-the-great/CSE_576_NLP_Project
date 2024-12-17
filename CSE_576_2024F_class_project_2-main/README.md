# CSE 576 Fall 2024 Class Project: Generating Optimal Questions to detect Hallucinations in LLM Generated Text

Class Project for CSE 576, NLP, Fall 2024 semester. The goal of the project is to generate optimal questions to detect hallucinations in LLM generated text.

## PLEASE DO NOT SHARE THE DATASETS PROVIDED ANYWHERE ELSE!

## Week 1: (23rd October - 30th October)
1. Read the paper: CoVe (https://arxiv.org/pdf/2309.11495), We will look into other papers on a requirement basis.
2. Project group members should finish setup of their ASU Sol Accounts and configure running open-source LLMs on Sol (start with Llama-3.1-8B-Instruct) (https://huggingface.co/meta-llama/Llama-3.1-8B-Instruct)
3. The initial **dataset** (which contains a lot of mistakes in step-by-step reasoning inference done by LLMs) for exploration: [https://drive.google.com/drive/folders/1EmHAZ-cl-t611pQYwWjHpRaH2CRUVtg8](url)

About this Dataset: This dataset contains legal scenarios (MCQA format) in which the reasoner is provided with all necessary legal rules to solve the scenario. The reasoner has to correctly reason on how to apply the rules and arrive at the correct option as the solution to the scenario. LLMs have to generate step-by-step reasoning chains to solve these questions.

## Week 2: (30th October - 6th November)
1. Similar to CoVe, start with initial prompting techniques on the dataset to generate verification questions.
    1.1. Generate Questions for every error category mentioned in the data document
2. Use Llama-3.1-8B-Instruct for both generating the reasoning chains and questions.
3. Individual task: It is advised for everyone to indivdidually craft prompt for question-generation in the style of CoVe paper.

## Week 5: (20th November - 27th November)
1. Run the inferences on the entire dataset while comparing zero-shot vs. the methods implemented by the team members.
2. Provide a quantitative comparision study of whether implemented methods show improvement over zero-shot CoT reasoning chains.
3. Only focus on those samples in the dataset which are wrongly answered by the LLM in zero-shot CoT setting.
4. We will explore other datasets if required to check the generalizability of the methods, if time permits.
