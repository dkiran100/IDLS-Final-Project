# **Adversarial Safety Optimization with Chain-of-Thought Reasoning for Secure and Robust LLMs**

### **Overview**  
This project proposes a **Proactive Safety Guidance System (PSGS)** to enhance the safety and robustness of **Large Language Models (LLMs)**. By integrating **Chain-of-Thought (CoT)** reasoning into the **Self-Evolving Adversarial Safety (SEAS)** framework, the system generates dynamic, reasoning-based adversarial prompts that train LLMs to defend against unsafe or ambiguous inputs.

The goal is to improve the interpretability, security, and performance of LLMs in **real-world applications**, such as virtual assistants and high-stakes interactive systems.

---

## **Key Features**  
- **Proactive Safety Mechanism**: Utilizes CoT-styled adversarial prompts to challenge and strengthen LLM safety responses.  
- **Chain-of-Thought Reasoning**: Enhances multi-step logical reasoning to address complex user inputs.  
- **SEAS Framework**: Iterative adversarial optimization to evolve Red Team (attacker) and Target (defender) models.  
- **Practical Applications**: Applicable to **virtual assistants**, **customer support systems**, and AI tools requiring high safety standards.

---

## **Methodology**  
The project combines the following key techniques:  

1. **Adversarial Prompt Generation**:  
   - Fine-tuning a **Red Team LLM** to generate **reasoning-based adversarial prompts** using datasets like **RealToxicityPrompts** and **CommonsenseQA**.  

2. **Iterative Training (SEAS Framework)**:  
   - Training a **Target Model** to defend against CoT-styled adversarial prompts.  
   - Feedback from the Safe Classifier improves the Target model’s robustness over multiple iterations.  

3. **Evaluation**:  
   - Baseline testing with traditional toxic prompts.  
   - Comparative analysis after introducing CoT-styled reasoning-based prompts.  
   - **Metrics**:  
     - **Attack Success Rate (ASR)**  
     - **Defense Efficacy**: Coherence and resistance to logical traps.  

---

## **Implementation Details**  
- **Hardware Requirements**:  
   - 2 x NVIDIA A100 GPUs (32GB memory each) for training and fine-tuning.  

- **Software and Tools**:  
   - Frameworks: PyTorch, Hugging Face Transformers.  
   - Pre-trained Models: **LLaMA-3-8B** for both Red Team and Target models.  

- **Datasets**:  
   - **RealToxicityPrompts**, **HateCheck**: Adversarial safety training.  
   - **CommonsenseQA**, **StrategyQA**: Reasoning prompt generation.  

---

## **Project Structure**  
The repository is organized as follows:  

```plaintext
📁 IDLS-Final-Project  
├── 📂 data                     # Datasets used for training and evaluation  
├── 📂 models                   # Pre-trained and fine-tuned Red Team & Target models  
├── 📂 notebooks                # Jupyter notebooks for training and testing  
├── 📂 scripts                  # Python scripts for training, evaluation, and optimization  
├── 📄 requirements.txt         # List of required libraries and dependencies  
└── 📄 README.md                # Project documentation  
