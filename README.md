# 🌊 AQUA SENTINEL

### Real-Time AI Agents for Water Crisis Prevention

<div align="center">
  
  ![Project Cover](Images/hero_image_clean.png)
  
  *AQUA SENTINEL - Kaggle AI Agents Capstone 2025 | Track: Agents for Good*
  
  [![Kaggle](https://img.shields.io/badge/Kaggle-Competition-blue)](https://www.kaggle.com)
  [![Python](https://img.shields.io/badge/Python-3.11+-green)](https://www.python.org)
  [![Google ADK](https://img.shields.io/badge/Google-ADK-orange)](https://google.github.io/adk-docs/)
  
</div>

---

## 🎯 The Problem

> **The problem isn't data—it's coordination.**

In 2023, the Horn of Africa faced its worst drought in 40 years. **20 million people** experienced acute hunger. Yet, we saw it coming months in advance—satellite data, weather models, and sensors all signaled the crisis. By the time the information was synthesized and coordinated, it was too late.

**AQUA SENTINEL** solves this coordination gap by using AI agents to monitor, analyze, and alert on water crises in real-time.

<div align="center">
  
  ![Problem Solution](Images/problem_solution_comparison.png)
  
  *The Problem vs. AQUA SENTINEL Solution*
  
</div>

---

## ⚡ Key Features

### 🚀 Real-Time Data Integration
- **NASA EONET**: Global natural disaster events (floods, droughts, severe storms) - daily updates
- **USGS Water Services**: Real-time water level sensors for US rivers (gage height, discharge rates)
- **Open-Meteo API**: Weather forecasts and current conditions (updated every 15 minutes)
- **REST Countries**: Geographic and demographic data for alert targeting

### 🤖 Multi-Agent Architecture
- **Hydro Orchestrator**: Intelligent query routing and synthesis
- **Sentinel Agent**: Parallel monitoring of multiple data sources
- **Guardian Agent**: Predictive analytics pipeline
- **Responder Agent**: Alert delivery with retry mechanisms

<div align="center">
  
  ![Architecture](Images/architecture_infographic.png)
  
  *System Architecture: Hydro Orchestrator with Parallel, Sequential, and Loop agent patterns*
  
</div>

---

## 📊 Impact & Performance

| Metric | Traditional | AQUA SENTINEL | Improvement |
|--------|------------|---------------|-------------|
| **Data Synthesis** | 4-6 hours | ~15 seconds | **99% faster** |
| **Sources Monitored** | 1-2 | 3+ (parallel) | **3x coverage** |
| **Alert Generation** | Manual, reactive | Automatic, 24/7 | **Proactive** |
| **Response Time** | Days to weeks | Minutes to hours | **Days saved** |

<div align="center">
  
  ![Impact Metrics](Images/impact_metrics_comparison.png)
  
</div>

---

## 🏗️ Agent Patterns

### ParallelAgent: Sentinel
Monitors multiple data sources **simultaneously**—weather (Open-Meteo), water levels (USGS), and disasters (NASA EONET)—enabling comprehensive real-time assessment.

<div align="center">
  
![Parallel Pattern](Images/parallel_agent_pattern.png)
  
*ParallelAgent: Concurrent Data Collection - Multiple sources fetched simultaneously*

</div>

### SequentialAgent: Guardian
Processes data in a structured **pipeline**: forecast → analyze → recommend, ensuring logical flow and dependency handling.

<div align="center">
  
![Sequential Pattern](Images/sequential_agent_pattern.png)
  
*SequentialAgent: Ordered processing pipeline (Forecast → Analyze → Recommend)*

</div>

### LoopAgent: Responder
Implements **retry logic** for critical alerts, ensuring delivery confirmation before completion (max 3 iterations).

<div align="center">
  
![Loop Pattern](Images/loop_agent_pattern.png)
  
*LoopAgent: Alert delivery with retry mechanism (max 3 iterations)*

</div>

---

## 🛠️ Technical Stack

- **Framework**: Google Agent Development Kit (ADK)
- **Model**: Gemini 2.0 Flash
- **APIs**: NASA EONET, USGS Water Services, Open-Meteo, REST Countries
- **Session Management**: InMemorySessionService
- **Evaluation**: Multi-dimensional scoring framework

<div align="center">
  
  ![Data Sources](Images/data_sources_visual.png)
  
  *Real-time data integration: Weather, Water Levels, Disasters, and Country Data with Aqua Sentinel at the center*
  
</div>

---

## 📈 Evaluation Results

AQUA SENTINEL achieves **96% average score** across 4 evaluation dimensions:

- ✅ **Validity (25%)**: Error-free responses
- ✅ **Relevance (35%)**: Domain-appropriate content
- ✅ **Freshness (20%)**: Real-time data indicators
- ✅ **Quality (20%)**: Response completeness

**Status**: 4/4 tests passed | Evaluation Successful ✅

<div align="center">
  
![Evaluation](Images/evaluation_framework.png)

*Evaluation Dimensions: Multi-dimensional Scoring Framework*

</div>

<div align="center">
  
![Agent Patterns Comparison](Images/agent_patterns_comparison.png)

*Agent Patterns: Parallel vs Sequential vs Loop workflows*

</div>

---

## 🚀 Quick Start

### Prerequisites
- Python 3.11+
- Google API Key (set in Kaggle Secrets)

### Installation
```bash
pip install google-genai google-adk requests
```

### Usage
Open the notebook and run the cells. Example queries:

```python
# Regional water situation
response = await query_aqua_sentinel(
    "What is the current water situation in California? Get real-time data from all sources."
)

# Global disaster monitoring
response = await query_aqua_sentinel(
    "What natural disasters are currently happening globally? Focus on water-related events."
)

# Emergency alerts
response = await query_aqua_sentinel(
    "Send an emergency drought alert to Kenya. Groundwater levels are critically low."
```

---

## 🎓 ADK Concepts Demonstrated

| Concept | Implementation | Status |
|---------|---------------|--------|
| Multi-Agent System | 4 agent patterns | ✅ |
| Custom Tools | 5 real-time API integrations | ✅ |
| Sessions & Memory | InMemorySessionService | ✅ |
| Agent Evaluation | Multi-dimensional framework | ✅ |
| Gemini Models | Gemini 2.0 Flash | ✅ |
| Real-Time Data | Live API connections | ✅ |

**Total**: 6+ key concepts (exceeds minimum requirement of 3)

---

## 🎯 Why Agents?

Traditional dashboards **display** data. AQUA SENTINEL agents **interpret**, **correlate**, and **act**:

- 🌍 **Monitors autonomously** across multiple data sources 24/7
- 🔍 **Correlates** weather, water levels, and disasters for holistic insights
- ⚡ **Proactively alerts** before crises escalate
- 🤝 **Coordinates** information that previously existed in silos

<div align="center">
  
  ![Agent Coordination](Images/agent_coordination.png)
  
  *Intelligent coordination: Hydro Orchestrator delegates queries to specialized agents based on context*
  
</div>

---

## 📖 Project Journey

This project evolved from an initial serverless architecture vision to a focused, notebook-based implementation using ADK patterns. Key challenges overcome:

- **Agent Parent Conflicts**: Solved by creating separate agent instances
- **Rate Limiting**: Mitigated through model selection and delays
- **Evaluation Consistency**: Addressed with multi-dimensional scoring

<div align="center">
  
![Project Timeline](Images/project_journey_timeline.png)

*Project Evolution: Development timeline and milestones*

</div>

<div align="center">
  
![Hydro Orchestrator](Images/hydro_orchestrator_diagram.png)

*Hydro Orchestrator Architecture*

</div>

---

## 💡 The Story

Inspired by the [#TeamWater campaign](https://teamwater.org), AQUA SENTINEL represents my attempt to contribute to water crisis prevention through technology. As a 22-year-old international student studying Computer Science, I wanted to build something that could make a tangible impact—beyond just financial donations.

The 2023 Horn of Africa drought showed that the problem wasn't lack of information, but lack of coordination. **This is exactly what AI agents are built for.**

---

## 📚 Resources

- [Google ADK Documentation](https://google.github.io/adk-docs/)
- [Project Notebook](./project-final%20(1).ipynb)
- [#TeamWater Campaign](https://teamwater.org)
- [Kaggle Competition](https://www.kaggle.com)

---

## 🏆 Credits

**Author**: [Jai Adithya Ram Nayani](https://www.linkedin.com/in/jai-adithya-ram-nayaniyani-20363b1a0/)

**Acknowledgments**:
- Google & Kaggle for the Agents Intensive Course
- MrBeast & Mark Rober for #TeamWater inspiration
- NASA, USGS, and Open-Meteo for free, accessible APIs

---

<div align="center">
  
  **Built with 💧 for the Kaggle AI Agents Intensive Capstone**
  
  *Empowering communities with AI-driven water crisis prevention*
  
</div>

