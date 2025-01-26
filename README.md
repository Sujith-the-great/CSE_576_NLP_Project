# HallucinationGuard-Llama

## Objective
The primary objective of this project is to explore and evaluate methods for detecting and minimizing hallucinations in Large Language Models (LLMs) during complex legal reasoning tasks. The project focuses on generating optimal questions to identify hallucinations and applying advanced reasoning and verification approaches to improve factual accuracy and reduce errors in LLM-generated text.

## Key Elements
1. **Problem Statement**: Hallucination in LLMs remains a critical challenge, especially in legal reasoning tasks. This project aims to address this by evaluating five reasoning and verification approaches across multiple LLMs.
2. **Approaches**:
   - **TREACC (Topic, Rule, Explanation, Analysis, Counter Arguments, Conclusion)**: A structured reasoning approach for legal tasks.
   - **Self-Verification**: A two-step process involving legal reasoning and verification question generation.
   - **Attention-based Verification**: A multi-stage approach focusing on critical legal terms and iterative refinement.
   - **Location-Based Error Correction**: Identifies and corrects reasoning errors by pinpointing their location in the reasoning chain.
   - **Deductive Verification of CoT Reasoning**: Uses structured natural language-based deductive reasoning to verify multi-step reasoning chains.
3. **Models Evaluated**:
   - Llama-3.1-8B-Instruct
   - Llama-3.2-3B-Instruct
   - Gemini-1.5-Flash
4. **Dataset**: 175 legal reasoning questions, options, and ground truth.

## Procedure
1. **Implementation of Approaches**: Each reasoning approach (TREACC, Self-Verification, Attention-based Verification, Location-Based Error Correction, Deductive Verification) was implemented and tested on the three LLMs.
2. **Evaluation**: The dataset was run on each approach, and the results were compared to assess the effectiveness of each method in minimizing hallucinations and improving factual accuracy.
3. **Analysis**: The performance of each approach was analyzed across the models, and the results were compared to a baseline Zero-shot Chain-of-Thought (COT) approach.

## Concepts
- **Hallucination in LLMs**: The generation of incorrect or nonsensical information by LLMs, particularly in complex reasoning tasks.
- **Legal Reasoning**: The application of legal principles and logical frameworks to solve legal problems.
- **Self-Verification**: A process where the model evaluates its own reasoning steps to identify and correct errors.
- **Attention-based Verification**: A method that focuses on critical terms and iteratively refines reasoning steps to ensure accuracy.
- **Deductive Reasoning**: A logical process where conclusions are drawn from a set of premises or facts.

## Results
The results from the evaluation are summarized below:

| Approach                | Llama-3.1-8B-Instruct | Llama-3.2-3B-Instruct | Gemini-1.5-Flash |
|-------------------------|-----------------------|-----------------------|------------------|
| Self-Verification       | 85.71%               | 60%                  | 100%             |
| Attention-based Verification | 85.14%           | 80.57%               | 96.57%           |
| TREACC                  | 54.86%               | 66.86%               | 84%              |
| Deductive Reasoning     | 42.2%                | 33.7%                | 63.42%           |
| Location-Based Error Correction | 41.17%       | 34.21%               | 60.2%            |
| Baseline Zero-shot COT  | 57.14%               | 37.14%               | 61.4%            |

### Key Findings:
- **Self-Verification** performed exceptionally well on Gemini-1.5-Flash (100%) but had moderate performance on Llama-3.2-3B (60%).
- **Attention-based Verification** showed consistent performance across all models, with the highest accuracy on Gemini-1.5-Flash (96.57%).
- **TREACC** had variable performance, peaking at 84% on Gemini-1.5-Flash but only achieving 54.86% on Llama-3.1-8B.
- **Deductive Verification** and **Location-Based Error Correction** were the weakest performers, highlighting challenges in decomposing legal reasoning tasks.

## Individual Contributions
- **Chao-Shiang, Chen**: Implemented the TREACC Approach (20%).
- **Ankitha Dongerkerry Pai**: Implemented the Self-Verification Approach (20%).
- **Rakshita Madhavan**: Implemented the Attention-based Verification Approach (20%).
- **Suraj Kumar Manylal**: Implemented the Location-Based Error Correction Approach (20%).
- **Bala Sujith Potineni**: Implemented the Deductive Verification Approach (20%).

## References
1. Yu, Fangyi, et al. "Exploring the Effectiveness of Prompt Engineering for Legal Reasoning Tasks." _Annual Meeting of the Association for Computational Linguistics_, 2023.
2. Hong, Ruixin, et al. "A Closer Look at the Self-Verification Abilities of Large Language Models in Logical Reasoning." _ArXiv (Cornell University)_, 2023.
3. Zhan, Ling, et al. "Deductive Verification of Chain-of-Thought Reasoning." _ArXiv (Cornell University)_, 2023.
4. Tyen, et al. "LLMs Cannot Find Reasoning Errors but Can Correct Them Given the Error Location." _ACL Anthology_, 2024.
5. Zhang, Tianhang, et al. "Enhancing Uncertainty-based Hallucination Detection with Stronger Focus." _arXiv preprint arXiv:2311.13230_, 2023.

## Repository Structure
- `Final Report-1.pdf`: The detailed project report.
- `README.md`: This file, providing an overview of the project.
- `code/`: Directory containing the implementation code for each approach.
- `data/`: Directory containing the dataset used for evaluation.

## How to Use
1. Clone the repository:
   ```
   git clone https://github.com/your-username/HallucinationGuard-Llama.git
   ```
2. Navigate to the code/ directory to explore the implementation of each reasoning approach.

3. Refer to the Final Report-1.pdf for detailed insights into the project's methodology and results.
