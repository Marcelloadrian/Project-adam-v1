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
