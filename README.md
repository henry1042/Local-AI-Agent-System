# 🧠 Local AI Agent System

A production-grade **local-first AI engineering system** combining Retrieval-Augmented Generation (RAG), autonomous agent reasoning (ReAct), secure tool execution, local LLM infrastructure (Ollama), and multi-layer AI safety architecture.

> Built to demonstrate real AI system engineering, not just prompt engineering.

---

## 🚀 Overview

This project is a full-stack AI system architecture designed for real-world enterprise AI workflows.

It demonstrates end-to-end AI system engineering including:

- RAG-based knowledge retrieval system
- Autonomous agent reasoning (ReAct loop)
- Local LLM deployment without cloud dependency
- Tool orchestration and execution safety
- Production-grade backend architecture design

---

## ⚡ Key Features

### 📚 RAG Knowledge System
Three-stage retrieval pipeline:
- Local Knowledge Base (primary source)
- LLM general knowledge fallback
- Wikipedia augmentation layer

Technical implementation:
- Embedding model: all-MiniLM-L6-v2 (384 dimensions)
- Vector database: ChromaDB
- Cosine similarity threshold: < 1.2
- Retrieval gating before LLM inference

---

### 🤖 Autonomous Agent (ReAct Engine)
Core reasoning loop:
Thought → Action → Observation → Final Answer

Capabilities:
- 19 integrated tools:
  - Web search
  - File analysis
  - Code execution
  - Web crawling
  - System utilities
  - Calculator engine
- Infinite loop detection system
- Context window control (10,000 characters)
- Tool execution isolation and safety constraints

---

### 🧠 Local-First LLM System
- Runtime: Ollama
- Model: gpt-oss:20b
- Fully offline inference (no external APIs)
- Centralized llm_service.py abstraction layer
- Hot-swappable model configuration

---

### 🛡️ Safety & Control Layer
Multi-layer AI safety system:
- Structured output validation (Pydantic schema enforcement)
- Role-based tool permission system
- Secure subprocess execution (shell=False)
- Duplicate tool call prevention
- Agent loop protection mechanisms

---

### 🔧 Data Quality Pipeline (5 Layers)
1. File validation and integrity checks
2. Document quality scoring system
3. Text normalization and cleaning
4. Chunk filtering and deduplication
5. Retrieval threshold gating before LLM execution

---

## 🏗️ System Architecture

User → UI Layer → RAG Engine → Local LLM (Ollama) → ReAct Agent Loop → Tool Execution Layer → Final Response

---

## 🧠 Advanced Architecture (Technical Deep Dive)

### 1. RAG Implementation
- Embedding: all-MiniLM-L6-v2 (384-dim)
- Vector DB: ChromaDB
- Cosine similarity threshold: < 1.2

### 2. Local LLM Layer
- Ollama runtime
- Centralized llm_service.py
- Model hot-swapping support

### 3. Agent Execution Engine
- ReAct reasoning loop implementation
- 19 tool integrations
- 10k character context limit
- Infinite loop detection system

### 4. Harness Engineering (AI Control Layer)
- Forced English output injection (_ENGLISH_OVERRIDE)
- Skill-based system prompts
- NEVER-rule enforcement system
- Duplicate tool call blocking

### 5. Hermes PRSOP (Structured Output System)
- Pydantic schema validation enforcement
- 5-layer safety pipeline:
  - Type validation
  - Regex constraints
  - Confidence gating
  - Whitelist filtering
  - Safe subprocess execution

---

## 🎯 Engineering Principles

- Local-first architecture (no cloud dependency)
- Deterministic tool execution
- Observable agent reasoning traces
- Safety-first AI system design
- Modular and extensible architecture

---

## 🧠 Purpose

This project demonstrates real-world AI engineering capability in:

- AI system architecture design
- RAG pipeline engineering
- Autonomous agent systems (ReAct)
- Tool orchestration frameworks
- Local LLM deployment
- Production backend system design

---

## 🧩 Why This Project Matters

Unlike typical AI demos, this system demonstrates:

- Real AI infrastructure design (not just prompting)
- Autonomous agent execution system
- Tool-based reasoning architecture
- Production safety controls
- Scalable modular system design
