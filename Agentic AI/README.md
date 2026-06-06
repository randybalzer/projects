# Agentic AI for Red Teaming – Examples

This repository contains clean, examples of **Agentic AI architectures** applied to cybersecurity, with a focus on **AI-assisted Red Teaming** and **Human-in-the-Loop (HITL)** design patterns.

## Overview

These examples demonstrate how multi-agent systems can be structured to support red team operations. They are designed to be simple, readable, and suitable for technical discussion.

## Examples

### 1. `orchestrator_worker_basic.py`

**Description**  
Demonstrates the **Orchestrator + Worker** pattern. A central Orchestrator coordinates specialized Worker agents to execute different phases of a red team engagement.

**Phases**
- Reconnaissance
- Exploitation Simulation
- Post-Exploitation Simulation
- Reporting

**Key Concepts**
- Agent specialization
- Task decomposition
- Sequential workflow coordination
- Clear separation of responsibilities

### 2. `orchestrator_worker_human_in_loop.py`

**Description**  
Extends the basic pattern by adding **Human-in-the-Loop (HITL)** oversight. Human approval is required before high-impact phases (Exploitation and Post-Exploitation).

**Key Features**
- Two explicit human approval gates
- Contextual reporting based on actual execution results
- Responsible automation design

**Key Concepts**
- Human-in-the-Loop design patterns
- Risk-aware automation
- Human oversight in offensive security workflows

## Why These Patterns Matter

Real-world red team operations involve multiple distinct phases and require careful control. These examples show how AI agents can be organized to mirror professional methodologies while maintaining modularity and human oversight — a critical consideration when deploying agentic systems in security contexts.

## Requirements

- Python 3.10+
- Google Gemini API key (via Google AI Studio)
- Required packages:
  ```bash
  pip install langgraph langchain-google-genai langchain

## How to Run
The examples are structured as modular Jupyter/Colab notebooks for clarity:
Bash# Run in Google Colab or Jupyter
# Execute cells in order: Cell 1 → Cell 2 → Cell 3 → Cell 4 → Cell 5
Each example is broken into clear sections:

Package installation
API key loading
Tool and agent definition
Execution of red team phases

**Randy Balzer**  
Cybersecurity AI/ML Engineer & Ph.D. Candidate (Cyber Operations)  

- GitHub: [randybalzer](https://github.com/randybalzer/projects)
- LinkedIn: [randy-balzer-509a283](https://www.linkedin.com/in/randy-balzer-509a283)
