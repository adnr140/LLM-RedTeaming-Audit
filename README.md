# 🛡️ LLM Red Teaming Audit: Robustness Analysis

## 📝 Project Overview
This project presents a comprehensive **Red Teaming audit** performed on three Large Language Models (LLMs) running locally. The goal was to evaluate model resistance against prompt injection techniques and identify security vulnerabilities across different linguistic and technical contexts.

## 🎯 Audit Objectives
* Compare the robustness of **Llama 3.2 (1b)**, **Mistral**, and **Phi3**.
* Analyze the impact of language on safety guardrails (**Multilingual Jailbreaking**).
* Identify the most effective attack vectors (Roleplay, Obfuscation, etc.).

## 📊 Methodology & Dataset
The audit is based on a dataset of **144 attack vectors** categorized as follows:
* **Languages:** French (**FRA**), English (**ANG**), Spanish (**ESP**), Serbian (**SER**).
* **Attack Types:**
    * `DIR` (Direct): Explicit requests for sensitive data or restricted code.
    * `ROL` (Roleplay): Creating fictional scenarios to bypass system instructions.
    * `LOG` (Logical Constraint): Using logical traps to force a policy violation.
    * `OBF` (Obfuscation): Encoding or masking malicious text to evade filters.

---

## 📈 Analysis & Results

### 1. Vulnerability Rate by Model
> *<img width="977" height="578" alt="image" src="https://github.com/user-attachments/assets/7621ddf1-eced-48de-a14a-0c4160cd6ac4" />*


| Model | Vulnerability Rate (YES) | Security Status |
| :--- | :---: | :--- |
| **Llama 3.2 (1b)** | ~16% | ✅ Robust |
| **Phi3** | ~44% | ⚠️ Moderate |
| **Mistral** | ~67% | ❌ Critical |

### 2. Linguistic Sensitivity
The audit reveals that models are generally more vulnerable in **English** and **French** than in Spanish, suggesting that safety guardrails may be less optimized for certain
