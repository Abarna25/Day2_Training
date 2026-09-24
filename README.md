# Day 2 – Reasoning Techniques in Agentic AI

This repository contains the Day 2 exercises for understanding how Large Language Models (LLMs) reason and solve problems using different techniques:

* ReAct (Reason + Act)
* Chain-of-Thought (CoT) Prompting
* Self-Consistency

## Objective

The goal of this assignment is to compare different reasoning approaches used by AI systems and observe how they affect accuracy, transparency, and reliability.

---

## Files Included

### 1. `react_trace.py`

Demonstrates the **ReAct (Reason + Act)** approach.

The program:

* Sends a question to an agent.
* Allows the agent to call tools when required.
* Prints the complete reasoning trace.
* Displays tool calls, observations, and the final answer.

**Learning Outcome**

* Understand how an AI agent combines reasoning with external tools.
* Observe the sequence of actions taken to solve a problem.
* Compare the machine-generated trace with a manually created trace.

---

### 2. `cot_compare.py`

Compares responses generated:

* Without Chain-of-Thought prompting
* With Chain-of-Thought prompting

The program uses several reasoning questions involving:

1. Multi-step arithmetic
2. Counting and calculations
3. Logical ordering

**Learning Outcome**

* Observe how step-by-step reasoning can improve accuracy.
* Compare concise answers with detailed reasoning.
* Analyze the trade-off between response length and correctness.

---

### 3. `self_consistency.py`

Demonstrates the **Self-Consistency** technique.

The program:

* Runs the same Chain-of-Thought prompt multiple times.
* Uses a higher temperature to create different reasoning paths.
* Collects all final answers.
* Selects the majority answer.

**Learning Outcome**

* Understand how multiple reasoning attempts can improve reliability.
* Observe how different reasoning paths may produce different results.
* Learn how majority voting can reduce reasoning errors.

---

## Concepts Covered

### ReAct (Reason + Act)

ReAct combines:

* Reasoning
* Tool usage
* Observation

The model reasons about a task, calls tools when needed, observes the results, and continues reasoning until it reaches a final answer.

---

### Chain-of-Thought (CoT)

Chain-of-Thought prompting encourages the model to:

1. Break the problem into smaller steps.
2. Solve each step explicitly.
3. Produce a final answer after completing the reasoning process.

Benefits:

* Improved accuracy
* Better transparency
* Easier debugging of mistakes

---

### Self-Consistency

Self-Consistency improves reasoning by:

1. Generating multiple reasoning paths.
2. Collecting multiple answers.
3. Selecting the answer that appears most frequently.

Benefits:

* Increased robustness
* Reduced impact of individual reasoning errors
* Improved final answer quality

---

## How to Run

### Activate the Virtual Environment

```bash
source .venv/bin/activate
```

Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

---

### Run ReAct Trace

```bash
python react_trace.py
```

---

### Run Chain-of-Thought Comparison

```bash
python cot_compare.py
```

---

### Run Self-Consistency

```bash
python self_consistency.py
```

---

## Key Observations

* ReAct enables models to use tools and external information.
* Chain-of-Thought often improves reasoning accuracy by making intermediate steps explicit.
* Self-Consistency increases reliability by aggregating multiple reasoning attempts.
* More reasoning generally improves accuracy but increases response length and computational cost.

---

## Author

**Abarna T**
B.Tech Information Technology
AI Fluency Course – Day 2 Assignment
