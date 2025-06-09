# 🧠 AI Signal – Hallucination from Malformed Input

Broken or incomplete signals entering LLMs or AI models can result in hallucinated outputs — responses that appear fluent but are factually incorrect, misleading, or unsafe.

---

## 📍 Early Indicators

- Event payloads missing metadata or context  
- Ingested user actions without valid consent path  
- Prompts or structured inputs overwritten by noisy triggers  
- Model outputs contradict ground truth or embed user-specific hallucinations  

---

## 🔍 Example Scenarios

- LLM recommends a feature that was deprecated  
- AI chatbot creates fictional user paths based on partial logs  
- Customer service model generates non-existent resolution steps  

---

## ⏳ RCA Escalation Path

Will be promoted to `/use-cases/ai-product/hallucination-due-to-signal-drift/` if reproducibility and system-wide impact are confirmed.

> “When the signal breaks, the story the model tells becomes fiction.”
