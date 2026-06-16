# Agentic AI for Defensive Security Automation

This repository contains two complementary Jupyter notebooks demonstrating practical use of **agentic AI** in cybersecurity:

1. **Red Team Engagement Simulator** (`orchestrator_worker_human_in_loop.ipynb`)
2. **Defensive C2 Anomaly Detection Agent** (`defensive_c2_anomaly_agent.ipynb`)

Both examples use the **Orchestrator + Worker** pattern with **Human-in-the-Loop (HITL)** oversight and integrate with the **MITRE ATT&CK** framework.

---

## 1. Red Team Engagement Simulator (Human-in-the-Loop)

**File:** `orchestrator_worker_human_in_loop.ipynb`

This notebook simulates a controlled red team engagement using a multi-agent system. It demonstrates how agentic workflows can structure and document offensive security activities in a repeatable, auditable way.

**Key Features:**
- Orchestrator + Worker architecture
- Human approval gates between phases (Recon → Exploitation → Post-Exploitation → Reporting)
- MITRE ATT&CK technique mapping with hyperlinks
- Built with LangChain + OpenAI

**Relevance:** Shows practical understanding of building AI tooling to support red team operations, adversarial emulation, and security automation.

---

## 2. Defensive C2 Anomaly Detection Agent

**File:** `defensive_c2_anomaly_agent.ipynb`

This notebook demonstrates a lightweight defensive agent that enriches security alerts and requires human approval before taking action (e.g., notifying the SOC team). It is designed as a complement to traditional ML-based detection (such as K-Means clustering for C2 beaconing).

**Key Features:**
- Two specialized agents (enrichment + notification)
- Human-in-the-Loop approval before sending notifications
- MITRE ATT&CK mapping (T1071.001)
- Simple and extensible design

**Relevance:** Illustrates how agentic AI can be applied to defensive security operations, alert triage, and automated notification workflows with human oversight.

---

## How the Two Notebooks Work Together

| Aspect                    | Red Team Notebook                          | Defensive Notebook                          |
|---------------------------|--------------------------------------------|---------------------------------------------|
| **Focus**                 | Offensive / Adversarial emulation          | Defensive / Alert response                  |
| **Pattern**               | Orchestrator + multiple specialized workers| Two specialized agents                      |
| **Human Oversight**       | Approval between major phases              | Approval before sending notifications       |
| **MITRE ATT&CK**          | Multiple techniques across phases          | Single technique (T1071.001)                |
| **Use Case**              | Red team tooling & simulation              | Security automation & SOC support           |

Together they show a balanced view of how agentic AI can be applied across both offensive and defensive cybersecurity workflows.

---

## Running the Notebooks

### Requirements
```bash
pip install langgraph langchain-openai langchain
```

### API Key
Both notebooks expect an OPENAI_API_KEY environment variable (or Colab secret).
#### Execution

* Run cells sequentially.
* Human input is required at approval gates.

## Future Improvements / Known Limitations

* Phase 2 technique selection in the red team notebook can be further refined for accuracy and consistency.
* Both examples currently use simulated actions. Future versions could integrate real tools or APIs in a safe, controlled environment.
* The defensive notebook is intentionally lightweight and can be extended to work alongside existing ML detection pipelines (e.g., K-Means C2 beaconing).


## Repository Structure

* orchestrator_worker_human_in_loop.ipynb – Red team engagement simulator
* defensive_c2_anomaly_agent.ipynb – Defensive C2 anomaly agent (OpenAI version)
* README.md – This file
