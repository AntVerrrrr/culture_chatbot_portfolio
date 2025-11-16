# 🇰🇷 Andong Cultural AI Chatbot  
지역 문화와 관광을 AI로 연결하는 다국어 챗봇 서비스  
(Django · DRF · OpenAI Responses API · Whisper STT · TTS · i18n · MySQL · Redis)

---

## 🧭 Project Background – 기술로 사람과 문화를 연결하다

저는 기술이 단순한 기능 구현이 아니라 **사람과 소통하는 새로운 언어**라고 믿습니다.  
소프트웨어융합학과(구 멀티미디어공학과)에서 포토샵·일러스트·프리미어·CAD부터  
Python·Java·C 등 다양한 소프트웨어를 배우며,

> **“코딩은 사용자의 의도를 이해하고 응답하는 새로운 형태의 의사소통이다.”**

라는 확신을 가지게 되었습니다.

그 무렵, 교육에 관심이 많던 교육공학과 친구와 나눈  
“AI로 교육과 문화를 연결하면 어떨까?”  
라는 대화가 계기가 되었고,  
그 친구는 이후 대통령 인재상을 수상하게 되었습니다.  

저는 그 비전을 기술적으로 실현하기 위해 합류했고,  
그렇게 **‘안동 관광문화 챗봇’** 프로젝트가 시작되었습니다.

프로젝트 초반 대부분의 기능을 **혼자 구현**해야 했고,  
처음 경험하는 기술(TTS/STT, 다국어, 배포 등)로 인해  
많은 시행착오를 겪었습니다.  
특히 창업박람회 참가 당일 발생한 오류를  
현장에서 급히 수정하는 경험은 큰 교훈이 되었습니다.

하지만 이 과정을 거치며 서비스는 안정화되었고,  
현재는 외국인 관광객을 위한 **실사용 문화 안내 서비스**로 운영되고 있습니다.

---

## 🌍 Overview

**Andong Cultural AI Chatbot**은  
안동 지역의 문화유산·관광명소·전통주·독립운동 인물을  
AI 기반으로 안내하는 다국어 챗봇 서비스입니다.

### 📌 실제 활용 사례
- 안동시 **문화관광과**와 협업해 관광 안내 서비스로 운영  
- 탈춤축제 기간 **전통주 장인·상점 홍보 기능** 제공  
- 챗봇 세계관을 보드게임으로 확장 → **와디즈 113% 펀딩 성공**  
- 교육용 콘텐츠로 **교육부 장관상 수상**  
- 이후 **투자 유치 및 서비스 고도화 진행 중**

---

## 🧩 Features

| 기능 | 설명 |
|------|------|
| 🗺️ 지역 선택 UI | 시/도 → 시군구 별 어시스턴트 자동 매칭 |
| 🧠 AI 챗봇 | OpenAI Responses API + File Search 문화 안내 |
| 🔍 File Search | assistant.document_id 기반 근거 기반 응답 |
| 🎤 STT | Whisper API 기반 음성 인식 |
| 🗣️ TTS | OpenAI TTS 기반 음성 출력 |
| 🌐 다국어 | 한국어/영어/일본어/프랑스어/독일어 |
| 🔖 태그 추천 | 전통주·문화·독립운동 등 태그 기반 추천 |
| 🧭 프리뷰 페이지 | 어시스턴트 소개, 질문 10개, 관련 추천 |
| 🛠 Admin | 지역/태그/어시스턴트/번역/사진 관리 |
| 🔐 토큰 제한 | Redis 기반 IP 일일 토큰 제한 |

---

## 🏗 Architecture

```mermaid
flowchart LR
    User --> Frontend[Frontend (HTML/CSS/JS)]
    Frontend --> API[Django REST API]

    API -->|Chat| OpenAI_Responses[OpenAI Responses API]
    API -->|File Search| OpenAI_Files[File Search]
    API -->|STT| Whisper[Whisper STT]
    API -->|TTS| TTS[OpenAI TTS]

    API --> DB[(MySQL)]
    API --> Cache[(Redis)]
