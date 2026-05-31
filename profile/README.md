# neurobloom.ai

Open protocols and emotionally intelligent infrastructure for AI agents.
Home of **PACT** — the Protocol for Agent Collaboration & Transfer.

---

## Install

```bash
pip install pact-protocol      # core intent protocol
pip install pact-langchain     # LangChain integration
pip install pact-ax-client     # multi-agent collaboration SDK
```

---

## 30-second quickstart

```python
from pact_ax_client import Agent

agent = Agent("my-agent", base_url="http://localhost:8000")
agent.register_capability("contract_review", description="Reviews NDAs")

decision = agent.route("contract_review")
if decision.routed:
    result = agent.handoff(decision.best_agent, state_data={"doc": "..."})
    agent.remember("contract_review", partner_id=decision.best_agent, outcome="positive")
```

---

## The PACT layer map

| Repo | Layer | What it handles |
|---|---|---|
| [`pact`](https://github.com/neurobloomai/pact) | Core | The protocol itself — how agents speak a shared language |
| [`pact-ax`](https://github.com/neurobloomai/pact-ax) | **A**gent e**x**perience | Agent-to-agent collaboration primitives (server) |
| [`pact-ax-client`](https://github.com/neurobloomai/pact-ax-client) | SDK | Python SDK for pact-ax — `pip install pact-ax-client` |
| [`pact-hx`](https://github.com/neurobloomai/pact-hx) | **H**uman e**x**perience | How agents show up for a single human |
| [`pact-hh`](https://github.com/neurobloomai/pact-hh) | **H**uman-**H**uman | Humans collaborating through agents |
| [`pact-gx`](https://github.com/neurobloomai/pact-gx) | **G**overnance | Relational authority and structural dissent |
| [`pact-sx`](https://github.com/neurobloomai/pact-sx) | **S**ystemic | Relationships between entities and systems |
| [`pact-bridge`](https://github.com/neurobloomai/pact-bridge) | Spine | Connective tissue across the layers |
| [`pact-demos`](https://github.com/neurobloomai/pact-demos) | Examples | Reference implementations and walkthroughs |
| [`pact-contract-testing`](https://github.com/neurobloomai/pact-contract-testing) | Conformance | Contract tests for PACT-compliant agents |
| [`rlp-0`](https://github.com/neurobloomai/rlp-0) | Sibling | Relational Ledger Protocol — computational relationships |

---

## What pact-ax-client gives you

| Primitive | What it does |
|-----------|-------------|
| **Agent** | High-level façade — route, handoff, remember, vote in one object |
| **Capabilities** | Register and discover agent skills |
| **Trust** | Persistent, weighted trust scores between agents |
| **Router** | Route tasks to the best trusted + capable agent |
| **Episodic Memory** | Record and recall past interactions |
| **Handoff / Transfer** | Prepare → send → receive state packets |
| **Dead Letter Queue** | Park failed deliveries for retry |
| **Consensus** | Weighted-vote consensus across agents |

---

## Start here

New to PACT? Read [`pact`](https://github.com/neurobloomai/pact) first.  
Building with agents? `pip install pact-ax-client` and follow the quickstart above.  
Running the server? See [`pact-ax`](https://github.com/neurobloomai/pact-ax).

---

## Utility tools

| Repo | What it does |
|---|---|
| [`market-tools`](https://github.com/neurobloomai/market-tools) | Market dashboards and stock screeners for US and India (Yahoo Finance) |

---

*MIT-licensed. Issues and PRs welcome across every layer.*
