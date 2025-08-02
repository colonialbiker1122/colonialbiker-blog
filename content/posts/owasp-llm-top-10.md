+++
date = '2025-08-02T12:44:04+05:30'
draft = false
title = 'OWASP LLM Top 10'
+++
## 1. Prompt Injection
- Direct / Jailbreak
- Indirect : Summarise webpage, upload resume
- Previlige control, trust boundaries

## 2. Insecure output handling
- Apps with LLM privileges beyond user requirement
- Example: LLM output interpreted by browser resulting in XSS

## 3. Training data poisoning
- Supply chain of training data, ML-BOM, sandboxing, MLSecOps, biased opinions (leading to Hate crimes etc.)

## 4. Model Denial of Service
- Continuous input overflow, repetitive long input, recursive context expansion, variable length input flooding, DoS etc.

## 5. Supply chain vulnerabilities
- Poisoned crowd-sourced data, outdated models, model and code signing, PyPi package registry, AI-BOM

## 6. Sensitive Information Discourse
- Memorisation of training data (sensitive data), unintended disclosure of confidential information due to LLM misinterpretation

## 7. Insecure plugin design

## 8. Excessive agency
- Eliminate excessive functionality/ permissions/ autonomy.

## 9. Overreliance
- Hallucination, confabulation, plagiarism, disinformation, Parameters Efficient Tuning (PET), chain of thought prompting

## 10. Model theft
- Shadow model, ML model registry, side channel attacks, self-instruct (generate synthetic training data)

