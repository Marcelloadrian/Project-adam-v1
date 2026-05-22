# Project Adam (Phase 1: Synthetic Data Ingestion & Baseline Study)

Project Adam is an experimental framework designed to build an Autonomous Multi-Agent Social Ecosystem. The ultimate goal is to generate domain-specific synthetic social interactions, compress them into structural "Soul Documents," and train a Small Language Model (SLM) from scratch using sequential neural networks (LSTM) to mimic human behavioral biases, localized slang, and casual communication patterns.

This repository contains **Phase 1 (V1)**, which focuses on engineering the automated synthetic data pipeline and establishing the initial raw baseline dataset.

---

## 📊 V1 Dataset Architecture

The baseline dataset consists of **2,000 synthetic chat logs** representing conversational interactions between two core personas (Marcel and Jessica). The pipeline successfully automated the data collection and structured the output into a unified, lightweight JSON format.

### Data Preview (`data_simulasi_tahun_1.json`)
```json
[
  {
    "index": 1,
    "year": "Tahun 1",
    "sender": "Jessica",
    "text": "ekhem udah lupa ada gw?"
  },
  {
    "index": 2,
    "year": "Tahun 1",
    "sender": "Marcel",
    "text": "hahahaha gw juga lupa sih, tapi gw ingat gw ada gw, so yeah, gw ada"
  }
]

```

---

## 🔍 Critical Evaluation & Engineering Insights (The V1 Imperfection)

As a robust Data Engineering and Machine Learning project, Phase 1 was strictly evaluated to analyze the behavioral limits of the local generative LLM framework.

### Key Findings:

1. **Context Looping & Mode Collapse:** The extracted raw data exhibits a heavy pattern of repetition (e.g., hyper-fixation on localized loops like *"capek bgt"*, *"kesepian"*, and *"shift sales"*).
2. **Determinism vs. Entropy:** Due to a low default temperature setting and lack of external state intervention during the simulation, the two agents fell into a conversational feedback loop, reducing the semantic variance of the dataset.
3. **Implication for SLM Training:** If this raw dataset is directly injected into the V3 LSTM architecture, the resulting Small Language Model will inherit this communication defect, producing highly predictable and repetitive responses.

---

## 🚀 The Blueprint Evolution (Next Steps)

The flaws discovered in this V1 baseline study directly inform the architectural design of **Phase 2 (V2 Syn Theater)** and **Phase 3 (Mimicry)**.

```
[V1: Raw Ingestion (Current)] ──► [V2: Multi-Agent Syn Theater] ──► [V3: Custom SLM via LSTM]

```

### 🧠 Phase 2: Autonomous Theater Architecture

To eliminate context looping and introduce semantic entropy, Phase 2 will introduce:

* **The Groq Director Layer:** An external orchestration layer that dynamically injects real-time events and forces topic transitions every 10-15 tokens.
* **Hyperparameter Tuning:** Introducing `frequency_penalty` and scaling the `temperature` (0.85 - 1.0) to penalize repetitive phrasing and unlock creative vocabularies.
* **The Infant Agent (Tabula Rasa):** Injecting an unconditioned agent into the backchannels to absorb social jargon and behavioral biases through In-Context Social Learning.

### 🧪 Phase 3: Custom SLM Training (From Scratch)

* Extracting the refined chat logs of the Infant Agent to build a specialized localized Vocabulary Map (slang, typographies, emotional triggers).
* Building and training a custom **Sequence-to-Sequence LSTM with Attention Gating** from scratch in PyTorch to lock the sirkel's "soul" into an independent chatbot without relying on external LLM weights.

---

## 🛠️ How to Inspect the Data

To run a quick diagnostics check on the harvested dataset, execute the following script:

```python
import json

file_path = 'data_simulasi_tahun_1.json' # Adjust path if stored inside a subdirectory
with open(file_path, 'r', encoding='utf-8') as f:
    data = json.load(f)

print(f"Total Harvested Logs: {len(data)} entries.")
print(json.dumps(data[:5], indent=2, ensure_ascii=False))

```

---

**Author:** Tsem Li An

**Specialization:** Computer Science / Machine Learning Infrastructure

*Copyright © 2026 Adrian Marcello Budiman. All rights reserved under the MIT License.*

```

```
