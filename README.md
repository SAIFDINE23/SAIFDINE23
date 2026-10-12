<div align="center">

# Saif-Eddine El Khantache

**AI Engineer** — LLM systems, multi-agent orchestration, large-scale machine learning

Final-year engineering student · EILCO (France) & ENSIAS (Morocco) · B.Sc. Applied Mathematics

**Looking for a 6-month end-of-studies internship (PFE) — from February 2027, anywhere in France**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/saif-eddine-el-khantache)
[![Email](https://img.shields.io/badge/Email-333333?style=flat-square&logo=gmail&logoColor=white)](mailto:saifdineelkhantache@gmail.com)

</div>

---

I build AI systems that make it to production, and I measure them before I claim anything.

Every project below states the metric, the baseline it was compared against, and what it does **not**
solve yet. If a number is missing, it is because I have not measured it.

---

## Featured work

### Real-time e-commerce recommender system

`PySpark` `Kafka` `Spark Streaming` `Redis` `Airflow` `MLflow` `Docker`

Batch and streaming architecture over **110 million** browsing events: Spark data lake, Kafka /
Spark Streaming ingestion, session profiles served from Redis in ~2.5 s, recommendations computed
in ~5 ms.

ALS collaborative filtering, evaluated against a popularity baseline defined *before* training:
**+58% Recall@10** and **+87% NDCG@10**.

Nightly Airflow pipeline with a blocking data-quality gate, champion/challenger retraining and
promotion through the MLflow model registry.

*Next: LightGBM re-ranking and a serving API — not built yet, so not claimed.*

---

### Multi-agent fact-checker

`LangGraph` `LangSmith` `tool calling`

A language model alone cannot check facts: it only has its training memory, and it hallucinates
confidently. This system grounds every verdict in external evidence.

Four orchestrated agents — evidence retrieval through web search, a structured verdict carrying a
confidence score, a critic agent that audits the reasoning and can trigger a correction loop, and a
human-in-the-loop node that interrupts the graph when confidence is too low.

**93% accuracy on 15 labelled claims.** Every run traced in LangSmith.

LangGraph was chosen for cyclic graphs and native checkpointing, which make pausing and resuming
execution possible — a simple chain cannot do that.

---

### Enterprise RAG assistant

`LangChain` `ChromaDB` `Gemini embeddings` `Llama-3 / Groq` `FastAPI` `RAGAS`

Upload a long PDF, ask questions in natural language, get answers generated **only** from the
document, with their source cited.

1,000-character chunks with 200 overlap, ChromaDB vector store, top-4 passage retrieval,
Llama-3 served through Groq for low latency, FastAPI backend with a web interface.

**83% faithfulness** measured with RAGAS before the assistant was made available.

Deployed end to end: Docker, AWS provisioned with Terraform and Ansible, orchestrated on a
hardened K3s Kubernetes cluster.

---

### Fake news detection — content and source

`BERT` `Neo4j` `scikit-learn` `TF-IDF` `Word2Vec` `LSTM`

Disinformation spreads faster than manual verification can follow. This project attacks it from two
angles: what the article says, and who publishes it.

**Content** — comparative study on **72,000 labelled articles**: SVM and Random Forest (TF-IDF,
Word2Vec), then an LSTM, then a fine-tuned BERT. **97% accuracy against 94%** for the classical
models, with an equivalent F1 score.

**Source** — articles, authors and sites modelled as a Neo4j graph. The Louvain algorithm surfaced
networks of sites sharing the same authors.

What I actually learned: a score that high made us question the dataset, and we found a **source
bias** — part of the genuine articles came from a single news agency the model could recognise by
style alone. Robustness still has to be validated on external data.

---

## Professional experience

**AI & Back-End Engineer** — DATALIA, Paris · May – July 2026
Generative-AI SaaS editor, agile feature team of five. Two-stage prompt engineering pipeline
(criteria selection, then generation) for image and code generation, with output control and
test-validated variable selection. Six back-end features taking the platform from individual to
collaborative, administrable and monetised use.

**AI Engineer, 3D Vision** — 3D Smart Factory · July – September 2024
Dental segmentation on 3D meshes with MeshSegNet (PyTorch), **Dice above 95%**. Containerised
preprocessing pipeline over **20 GB** of raw medical data, reproducible and documented — the team
took it over without my help.

---

## Toolbox

**Generative AI & agents** — LLMs, RAG, multi-agent systems (LangGraph, LangChain), tool calling,
human-in-the-loop, prompt engineering, NLP, BERT

**Machine learning** — Python, PyTorch, scikit-learn, Pandas, NumPy, LSTM, CNN, SVM, Random Forest,
TF-IDF, Word2Vec, clustering, recommender systems

**Data & cloud** — SQL, PostgreSQL, PySpark, Kafka, Airflow, MLflow, Neo4j, ChromaDB, Redis, AWS,
Terraform, Ansible, Docker, Kubernetes, CI/CD, Git, FastAPI, Linux

**Evaluation** — RAGAS, labelled test sets, baselines defined before training, data-bias detection,
Matplotlib, Seaborn

---

## Education & certifications

| | |
|---|---|
| 2025 – 2027 | **Engineering degree, Artificial Intelligence** — EILCO, Calais, France |
| 2023 – 2025 | **Engineering degree, Data Science & IoT** — ENSIAS, Rabat, Morocco |
| 2022 – 2023 | **B.Sc. Applied Mathematics** — Ibn Tofail University, Kénitra, Morocco |

**Master DevOps: CI/CD, Automation & Monitoring** — Coursera / Edureka, 2025
**Cloud AWS Foundations** — IBM · **GANs Specialization** — DeepLearning.AI

---

<div align="center">

Arabic (native) · French (C1) · English (B2)

**Open to AI and data internships from February 2027.**
[Get in touch](mailto:saifdineelkhantache@gmail.com)

</div>
