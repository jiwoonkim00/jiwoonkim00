# 👋 안녕하세요, AI 에이전트 엔지니어 김지운입니다.

**Vision · LLM · RAG를 연결해 실제 동작하는 AI 에이전트 시스템**을 만드는 데 집중하고 있습니다.

---

## 💡 About Me

* **AI Agent 설계:** LLM을 단순 호출이 아닌 **도구(Tool)를 사용하는 에이전트**로 설계합니다. RAG 검색 → 멀티모달 분석 → 리포트 자동 생성까지 파이프라인 전체를 직접 구현합니다.
* **Vision + LLM 통합:** 이미지/영상 처리 결과를 LLM이 활용할 수 있는 구조화된 증거(Evidence)로 변환하고, 안전하게 리포트로 연결하는 **멀티모달 에이전트** 구조에 강점이 있습니다.
* **제품 수준의 안전 설계:** 의료·제조 등 고위험 도메인에서 Fail-closed, Validator-gated, Evidence-first 원칙을 적용한 에이전트를 구현한 경험이 있습니다.
* **빠른 프로토타이핑:** 데이터 모델 → API → 에이전트 워크플로우까지 혼자 설계하고 시연 가능한 수준으로 완성합니다.

---

## 🛠️ Tech Stacks

| 분야 | 기술 스택 |
| :--- | :--- |
| **Language** | <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/> <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black"/> |
| **AI Agent** | <img src="https://img.shields.io/badge/LangGraph-000000?style=for-the-badge&logo=langchain&logoColor=white"/> <img src="https://img.shields.io/badge/RAG-47A248?style=for-the-badge&logo=searxng&logoColor=white"/> <img src="https://img.shields.io/badge/FAISS-00599C?style=for-the-badge&logo=facebook&logoColor=white"/> <img src="https://img.shields.io/badge/Chroma-47A248?style=for-the-badge&logo=chroma&logoColor=white"/> |
| **AI/ML** | <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white"/> <img src="https://img.shields.io/badge/MONAI-00ADD8?style=for-the-badge&logo=python&logoColor=white"/> <img src="https://img.shields.io/badge/PEFT_LoRA-000000?style=for-the-badge&logo=huggingface&logoColor=white"/> <img src="https://img.shields.io/badge/YOLOv8-00ADD8?style=for-the-badge&logo=yolo&logoColor=white"/> |
| **Backend/Infra** | <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white"/> <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/> <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white"/> |

---

## 🔗 Key Projects

### 1. 🏥 CT Chest AI Agent — 의료 영상 판독 보조 시스템 *(PoC)*
> MONAI Vision + Upstage Solar Pro 3 + RAG 기반 폐결절 자동 검출 및 판독 보조 리포트 생성

* **에이전트 구조:** CT DICOM 입력 → 폐 분할 → 결절 검출 → Evidence 생성 → RAG Prior 비교 → 리포트 자동 작성
* **핵심 설계:** Evidence-first / Fail-closed / Validator-gated — LLM은 Narrative 다듬기만 허용, 수치·소견 변경 불가
* **기술:** MONAI (LUNA16 RetinaNet, DynUNet), Solar Pro 3, Solar Embedding, ChromaDB, FastAPI
* **GitHub:** [chest-ct-ai-agent-PoC](https://github.com/MedicalStandard-dev/chest-ct-ai-agent-PoC)

---

### 2. 🏭 AI 자율 운영 공정 시스템 — 이상 탐지 & 8D 리포트 자동 생성
> 프레스 설비 이상 탐지 후 LangGraph Multi-Agent로 원인 분석 및 8D 리포트 자동 생성

* **에이전트 구조:** 시계열 이상 탐지 → RAG 지식 검색 → LangGraph Multi-Agent 원인 분석 → 8D 리포트 생성
* **주요 기여:** TimesNet + Anomaly Transformer 앙상블, 제조 특화 RAG 지식 베이스 (ChromaDB), LangGraph 워크플로우 설계
* **GitHub:** [AI Factory Repository](https://github.com/jiwoonkim00/ai_factory)

---

### 3. 🍳 CookDuck — AI 요리 추천 LLM Agent *(캡스톤)*
> 식재료 인식 (YOLOv8) + FAISS RAG + 파인튜닝 LLM 기반 멀티모달 요리 도우미

* **에이전트 구조:** 사진 → 식재료 인식 → 벡터 검색 → RAG 레시피 추천 → 음성(STT/TTS) 응답
* **주요 기여:** RAG 파이프라인 설계, 요리 Q&A 파인튜닝 데이터셋 10,000건 구축, Spring + FastAPI 통합 및 Docker 배포
* **GitHub:** [CookDuck Repository](https://github.com/jiwoonkim00/CookDuck_final)

---

## 📈 GitHub Stats

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=jiwoonkim00&show_icons=true&theme=buefy" alt="GitHub Stats" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=jiwoonkim00&theme=buefy" alt="GitHub Streak" />
</div>

---

## 📧 Contact

* **Email:** jiwoon1201@gmail.com
* **Phone:** 010-8699-1782
* **GitHub:** [github.com/jiwoonkim00](https://github.com/jiwoonkim00)
