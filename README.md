# 👋 안녕하세요, AI Engineer 김지운입니다.

**도메인 데이터를 LLM · RAG · Agent 기반 AI 솔루션으로 연결하는 주니어 AI 엔지니어**입니다.  
의료 AI 인턴십과 프로젝트를 통해 **PoC 기획, 데이터셋 구축, RAG 파이프라인, Multi-Agent 워크플로우, FastAPI 기반 AI 서버 연동**을 경험했습니다.

---

## 💡 About Me

- **LLM · RAG · Agent 기반 AI 솔루션 설계**  
  LLM을 단순 호출하는 챗봇이 아니라, 검색·추론·생성·검증 단계를 갖춘 AI Agent 구조로 설계합니다.

- **B2B GenAI PoC 경험**  
  의료 AI 인턴십에서 PACS 기반 `PACS Copilot`, `PPAI-RS 판독문 요약` PoC를 수행하며, 도메인 문서와 업무 데이터를 LLM/RAG 기반 솔루션으로 연결하는 경험을 쌓았습니다.

- **RAG / Vector Search 파이프라인 구현**  
  FAISS, ChromaDB, pgvector 기반 벡터 검색을 활용해 문서 검색 → 컨텍스트 구성 → LLM 응답 생성 흐름을 설계하고 구현했습니다.

- **Multi-Agent Workflow 설계**  
  LangGraph 기반으로 Detection, Retrieval, Action, Report 등 역할별 Agent를 분리하고, 복잡한 업무를 단계별로 자동화하는 구조를 설계했습니다.

- **Backend / AI Server 연동 경험**  
  FastAPI 기반 AI 서버와 Spring Boot 서비스 서버를 분리하고, REST API 기반 HTTP 통신으로 AI 요청·응답 흐름을 연동한 경험이 있습니다.

---

## 🛠️ Tech Stacks

| 분야 | 기술 스택 |
| :--- | :--- |
| **Language** | <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/> <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black"/> |
| **LLM / Agent** | <img src="https://img.shields.io/badge/LangGraph-000000?style=for-the-badge&logo=langchain&logoColor=white"/> <img src="https://img.shields.io/badge/Qwen-5A31F4?style=for-the-badge"/> <img src="https://img.shields.io/badge/LoRA_PEFT-FFCC4D?style=for-the-badge&logo=huggingface&logoColor=black"/> <img src="https://img.shields.io/badge/Prompt_Engineering-1F2937?style=for-the-badge"/> |
| **RAG / Vector DB** | <img src="https://img.shields.io/badge/RAG-47A248?style=for-the-badge"/> <img src="https://img.shields.io/badge/FAISS-00599C?style=for-the-badge"/> <img src="https://img.shields.io/badge/ChromaDB-47A248?style=for-the-badge"/> <img src="https://img.shields.io/badge/pgvector-316192?style=for-the-badge&logo=postgresql&logoColor=white"/> |
| **AI / ML** | <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white"/> <img src="https://img.shields.io/badge/BERT-FFB000?style=for-the-badge"/> <img src="https://img.shields.io/badge/YOLOv8-00ADD8?style=for-the-badge"/> <img src="https://img.shields.io/badge/DeepOD-1F2937?style=for-the-badge"/> |
| **Backend / API** | <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white"/> <img src="https://img.shields.io/badge/REST_API-2563EB?style=for-the-badge"/> |
| **Database / Infra** | <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white"/> <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/> |

---

## 🔗 Key Projects

### 1. 🏥 PACS Copilot PoC — CT 흉부 영상 판독 보조 도구

> CT 흉부 DICOM 영상을 기반으로 의료진의 판독 업무를 보조하는 PACS 연계형 AI PoC

- **목표:** DICOM 영상 기반 AI 판독 보조 흐름을 설계하고, LLM을 활용해 한국어 판독 보고서 초안을 생성
- **구조:** DICOM CT Image → Preprocessing → BiomedCLIP Image Embedding → Context / RAG → Solar Pro3 LLM → Korean Draft Report → Radiologist Review
- **핵심 설계:** LLM은 최종 진단자가 아니라, 의료진이 검토 가능한 판독문 초안 생성 보조 역할로 제한
- **기술:** BiomedCLIP, Solar Pro3, RAG, DICOM, PACS
- **의의:** 의료 VLM과 LLM을 PACS 워크플로우에 연결하는 B2B 의료 AI PoC 경험
- **GitHub:** [medical-ai-pacs](https://github.com/jiwoonkim00/medical-ai-pacs)

---

### 2. 📝 PPAI-RS — 판독문 번역·요약 PoC

> 의료진 중심 판독문을 환자가 이해하기 쉬운 언어로 번역·요약하는 환자 친화적 AI 요약 PoC

- **목표:** 의료 판독문을 쉬운 표현으로 재작성하고, 핵심 소견을 환자 친화적으로 요약
- **구조:** 현재 판독문 + 과거 판독문 → RAG 검색 → Qwen 기반 요약/재작성 → 이전 검사 대비 변화 요약
- **핵심 기능:** 과거 판독문이 있는 경우 RAG로 이전 기록을 검색해 현재 판독문과 비교 요약
- **기술:** Qwen, RAG, DICOM, PACS, Prompt Engineering
- **의의:** 단순 요약을 넘어 이전/현재 판독문을 비교하는 종적 비교 기능을 설계
- **GitHub:** [medical-translation](https://github.com/jiwoonkim00/medical-translation)

---

### 3. 🏭 AI 자율 운영 공정 시스템 — Press 이상 탐지 & 8D 리포트 자동 생성

> 프레스 설비 이상 탐지 후 LangGraph Multi-Agent로 원인 분석과 8D 리포트를 자동 생성하는 제조 AI Agent

- **목표:** 프레스 설비의 시계열 데이터를 기반으로 이상 탐지 → 원인 분석 → 조치 가이드 → 8D 리포트 생성을 자동화
- **Agent 구조:** Detection Agent → Retrieval Agent → Action Agent → PM Agent → Report Agent
- **주요 기여:**  
  - DeepOD 기반 TimesNet + AnomalyTransformer 앙상블 이상 탐지
  - 설비 매뉴얼, SOP, 8D 샘플 문서 기반 제조 특화 RAG 지식베이스 구축
  - Qwen2.5 + LoRA 기반 제조 이상/8D 리포트 생성 모델 구성
  - LangGraph 기반 Multi-Agent 워크플로우 설계
- **기술:** DeepOD, TimesNet, AnomalyTransformer, ChromaDB, bge-m3, Qwen2.5, LoRA, LangGraph
- **GitHub:** [AI Factory Repository](https://github.com/jiwoonkim00/ai_factory)

---

### 4. 🍳 CookDuck — AI 요리 추천 LLM Agent

> 식재료 인식 + RAG 레시피 검색 + LLM 조리 안내를 결합한 멀티모달 요리 도우미 서비스

- **목표:** 사용자가 가진 식재료를 기반으로 만들 수 있는 레시피를 추천하고, 조리 과정을 대화형으로 안내
- **구조:** 재료 사진 → YOLOv8 식재료 인식 → FAISS 레시피 검색 → RAG 컨텍스트 구성 → LLM 조리 안내 → STT/TTS 음성 도우미
- **주요 기여:**  
  - Sentence-BERT + FAISS 기반 RAG 파이프라인 설계
  - 요리 Q&A 10,000건 Instruction Dataset 생성
  - FastAPI AI 서버와 Spring Boot 서비스 서버 분리
  - REST API 기반 HTTP 통신으로 추천 요청·AI 응답 흐름 연동
  - Docker 기반 실행 환경 구성
- **기술:** YOLOv8, Sentence-BERT, FAISS, RAG, LLM, FastAPI, Spring Boot, Docker
- **GitHub:** [CookDuck Repository](https://github.com/jiwoonkim00/CookDuck_final)

---

### 5. 🧠 감정 기반 개인화 과제 추천 챗봇

> 사용자 일기·채팅 텍스트를 분석해 CBT 기반 행동 과제를 추천하는 AI 상담 보조 챗봇

- **목표:** 사용자의 감정 상태를 분석하고, CBT 이론과 WHO 가이드라인 기반 행동 과제를 개인화 추천
- **구조:** 사용자 텍스트 → 감정 멀티라벨 분류 → CBT 유형 추론 → RAG 기반 과제 검색 → LLM 추천 응답 생성
- **주요 기여:**  
  - KLUE/BERT 기반 43종 감정 멀티라벨 분류 모델 파인튜닝
  - 감정 확률 기반 CBT 유형 12종 추론 로직 설계
  - CBT·WHO 가이드라인 기반 RAG 추천 시스템 구현
  - pos_weight 기반 BCE Loss로 클래스 불균형 대응
- **기술:** KLUE/BERT, KOTE Dataset, RAG, pgvector/Chroma, LLM, FastAPI
- **GitHub:** [World Expansion Repository](https://github.com/jiwoonkim00/world-expansion)

---

## 🧩 Experience Highlights

### 🏥 Medical Standard — AI Engineer Intern

- PACS 기반 LLM/RAG PoC 2건 수행: `PACS Copilot`, `PPAI-RS`
- 공공 의료 AI 사업 제안서의 기술 아키텍처, 데이터 흐름, AI 기능 정의 작성
- PPAI-o 오케스트레이터의 LangGraph 기반 Multi-Agent 확장 구조 검토
- 의료기관 온프레미스 환경, PACS/EMR 연계, DICOM 가명화, 보안 구조 정리

### 🏆 Awards & Activities

- AI 기반 멘토링 프로젝트 경진대회 대상 / 1등
- 스마트 제조 AI Agent 해커톤 2025 본선 진출
- 2025 글로컬 창업캠프 경진대회 우수상
- 청주대학교 인공지능소프트웨어학과 학부연구생
- 멋쟁이사자처럼 부대표
- 9oormthonUNIV 백엔드 교육 이수 및 해커톤 참여

---

## 📈 GitHub Stats

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=jiwoonkim00&show_icons=true&theme=buefy" alt="GitHub Stats" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=jiwoonkim00&theme=buefy" alt="GitHub Streak" />
</div>

---

## 📧 Contact

- **Email:** jiwoonkim01@naver.com
- **GitHub:** [github.com/jiwoonkim00](https://github.com/jiwoonkim00)

---

> LLM · RAG · Agent를 고객사 업무 환경에 맞는 AI 솔루션으로 구현하는 엔지니어로 성장하겠습니다.
