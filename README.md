# LLM 심화 — Transformer 와 LLMs

<p class="gh-only">📖 <b>웹 교재로 보기:</b> <a href="https://ai-boostcamp.github.io/AgenticAI/">https://ai-boostcamp.github.io/AgenticAI/</a></p>

사전학습 LLM 을 **내 문제에 맞게 조정하고(Fine-tuning)**, **행동하는 시스템(AI
Agent)으로 확장**하는 방법을 다루는 교재다. 강의 "Transformer 와 LLMs"(홍근선,
㈜한국AI연구소)의 슬라이드를 읽는 글로 다시 쓴 것으로, 모든 실습은 Google Colab
노트북과 함께 제공된다.

1장에서는 Hugging Face 에서 모델을 구해 실행하는 것에서 시작해 Trainer 기반
Fine-tuning 과 LoRA · Unsloth · GGUF 까지, 2장에서는 Agent 의 개념에서 시작해
LangChain(RAG) · LangGraph · Tracing 까지 나아간다. 부록에서는 Agentic AI 를
Ontology · Knowledge Graph 와 결합하는 그림을 정리한다.

## 목차

**[교재 개요와 전체 목차](00_교재개요.md)** — 강의 전체에서 이 교재가 다루는 범위와
장 번호 대응

**1장 LLM Fine-tuning** — [장 개요](ch01_LLM파인튜닝/00_1장개요_장개요.md)

- [1.1 Hugging Face 와 LLM](ch01_LLM파인튜닝/1.1_HuggingFace와LLM.md) — 계정과
  Access Token, Transformers 라이브러리, Pipeline 실습, 동적 양자화, ChatBot,
  Multi-modal 모델
- [1.2 LLM Fine-tuning](ch01_LLM파인튜닝/1.2_FineTuning.md) — Trainer 기반 표준
  절차, IMDB · 한국어 영화 리뷰 감성 분류 실습
- [1.3 LoRA 를 이용한 Fine-tuning](ch01_LLM파인튜닝/1.3_LoRA.md) — PEFT 와 LoRA 의
  원리, 한국어 감성 분석 · Qwen3-14B Reasoning 실습, GGUF 저장과 llama.cpp 실행

**2장 AI Agent** — [장 개요](ch02_AIAgent/00_2장개요_장개요.md)

- [2.1 AI Agent 개요](ch02_AIAgent/2.1_AIAgent개요.md) — Planning · Memory · Tool
  use, 대표 연구(CoT/ToT/ReAct/Reflexion)와 Agent framework 비교
- [2.2 LangChain 과 RAG](ch02_AIAgent/2.2_LangChain과RAG.md) — Agent 구조 직접
  만들기, LangChain ReAct/Custom Agent, RAG 파이프라인과 Query Augment · Chunking
  설계
- [2.3 LangGraph 활용](ch02_AIAgent/2.3_LangGraph.md) — State · Node · Edge, 병렬 ·
  조건부 분기 · 재시도 루프, Multi-Agent 협업, MCP, AI-Ready Data
- [2.4 LangGraph Tracing](ch02_AIAgent/2.4_Tracing.md) — LangSmith · LangFuse 관측,
  Prompt 버전 관리와 A/B 실험 · 평가

**부록**

- [부록 A. Agentic AI 와 Ontology](부록A_AgenticAI/부록A_AgenticAI.md) — LLM ·
  Ontology · Knowledge Graph · GNN 파이프라인과 Palantir 의 접근 방식

## 실습 안내

각 실습 제목 아래의 **"Open in Colab" 배지**를 누르면 노트북이 Colab 에서 바로
열린다. 노트북 파일은 이 저장소의 [`code/`](https://github.com/AI-BoostCamp/AgenticAI/tree/main/code)
폴더에 교재의 실습 번호와 같은 이름으로 들어 있다.

실행 전 준비:

- **GPU 런타임** — 대부분의 실습은 Colab 의 GPU(T4/L4 급 이상)를 사용한다.
- **Hugging Face 토큰** — 계정을 만들고 Access Token 을 발급받아 Colab 보안
  비밀(secrets)에 `HF_TOKEN` 이름으로 저장한다. 절차는
  [1.1 절](ch01_LLM파인튜닝/1.1_HuggingFace와LLM.md)에서 다룬다. 토큰을 노트북
  파일에 직접 적지 않는 것이 원칙이다.
- **2장 실습의 추가 키** — 2.2~2.4 의 일부 실습은 `OPENAI_API_KEY` 를, 2.4 의
  tracing 실습은 `LANGSMITH_API_KEY` · `LANGFUSE_PUBLIC_KEY` ·
  `LANGFUSE_SECRET_KEY` 를 같은 방식으로 Colab 보안 비밀에 등록해 사용한다.

## 저자

**홍근선** — ㈜한국AI연구소 대표이사 · 삼성 DS사업부 딥러닝 전문 강사 ·
성균관대학교 데이터사이언스융합학과 겸임교수 (gshong@ai-camp.kr)
