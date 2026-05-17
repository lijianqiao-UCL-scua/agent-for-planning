# Urban Planning Review Agent
### AI-Powered Regulatory Compliance System for Chinese Urban Planning

## Overview
An intelligent assistant system for reviewing urban planning adjustment proposals (控规局部调整) in Chengdu, China. Built with RAG + Multi-Agent architecture, it reduces review time from **2 working days to under 25 seconds** while achieving **98.5% rule recall rate**.

## The Problem
Traditional manual review of urban planning proposals suffers from:
- Time-consuming: 50-100 page reports reviewed manually over days
- Human error: 5-10% miss rate on complex cross-department rules
- Knowledge silos: review quality depends on individual expert experience

## Solution Architecture
Three-agent pipeline mimicking real planning review workflow:

1. **Page-Scanner Agent** — chunks long PDF reports, extracts substantive planning changes
2. **RAG Retriever** — searches local knowledge base of 40+ real Chengdu planning cases
3. **Report-Synthesizer Agent** — generates structured official review documents

## Key Results
| Metric | Traditional | This System |
|--------|------------|-------------|
| Review time | 2 working days | 15-25 seconds |
| Rule recall rate | ~92% | 98.5% |
| Output format | Manual writing | Structured official document |

## Tech Stack
- LLM: DeepSeek-V3 / Qwen-Max
- Embeddings: text2vec-base-chinese
- Vector DB: Chroma
- Framework: LangChain
- Frontend: Streamlit

## Use Case Example
Input: Planning proposal to convert commercial land to residential near metro station

System automatically flags:
- Soil pollution investigation required (川环函〔2022〕667号)
- Commercial reduction justification analysis needed
- Transit facility relocation requires authority sign-off

## Paper
Published at China Urban Planning Annual Conference 2025
*"Multi-Agent Collaborative Urban Planning Review System: A Chengdu Case Study"*
