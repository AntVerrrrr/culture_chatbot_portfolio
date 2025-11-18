**Andong Cultural AI Chatbot** 챗 봇

󾓮 **Andong Cultural AI Chatbot**

지역 문화와 관광을 AI로 연결하는 다국어 챗봇 서비스

**Django · DRF · OpenAI Responses API · Whisper STT · TTS · i18n · MySQL · Redis![ref1]**

🧭 **Project Background –** 기술로** 사람과** 문화를** 연결하다

저는 기술이 단순한 기능 구현이 아니라 사람과** 소통하는** 새로운** 언어라고 믿습니다.

소프트웨어융합학과에서 포토샵·일러스트·프리미어·CAD부터 Python·Java·C 등 다양한 소프트웨어를 배우며,

“코딩은 사용자와 상호작용하는 새로운 형태의 의사소통이다.ˮ 라는 확신을 가지게 되었습니다.![](Aspose.Words.32c84c2c-235c-4678-a8ef-39a4ef724c2f.002.png)

그러던 어느 날, 교육공학과 친구와 나눈

**“AI**로** 교육과** 문화를** 연결해보면** 어떨까**?ˮ**

라는 대화가 계기가 되어 이 프로젝트가 시작되었습니다.

그 아이디어는 이후 친구가 대통령** 인재상을 수상하는 계기가 되었고, 저는 그 비전을 실제 서비스로 구현하기 위한 기술 파트너로 합류했습니다.![ref2]

🚀 대학생 사이드 프로젝트가 실제 사업이 되기까지

대학 3학년 때 첫 프로토타이핑을 시작했습니다.

책에서 배우던 코드와 실제 서비스 개발은 완전히 달랐고, 현실에서는 개발**·**배포**·**비용**·**마케 팅**·**오류** 대응 모든 것이 큰 장벽이었습니다.

특히 프로젝트 초기에는 Django 백엔드, 프론트엔드, OpenAI 연동, Whisper/TTS, 다국 어, 서버 배포까지 모든** 기능을** 혼자** 구현해야** 했으며, 수많은 시행착오를 겪으며 서비스를 

완성해 나갔습니다.

친구는 실제 서비스로 출시하기 위해 개인사업자** 등록을** 직접** 진행했고, 해당 프로젝트를 기 반으로 정식** 회사를** 설립했습니다.

이후 4학년이 되던 해, 출시 이후 직접 창업박람회(한국, 일본), 기관·축제·지자체에 영업을 뛰고 서비스 제안과 데모 시연, 유지보수까지 책임졌고, 안동 지역에서 1년 이상 실제 관광객 대상으로 운영되었습니다. 

또한 4학년 때 졸업작품 전시회에서 해당 프로젝트를 발표하다 안동지역의 소상공인조합을 이끄는 분께서 유심히 보시고 지역의 소상공인들을 위한 홍보 챗봇은 어떠냐고 하시며 명함 과 사업적 로드맵을 제안해 주셨습니다. 

결과적으로  다양한 마케팅으로 홍보가 되어 월** 평균 **200~300**만** 원** 규모의** 유료** 서비스** 매 출을** 기록하며** 실제** 수익이** 발생하는** 서비스로 성장했습니다.![ref1]

🌍** 주요** 성과** 및** 활용

안동 지역의 문화유산·관광·전통주·독립운동 정보를 AI가 **5**개국어로** 안내하는** 챗봇** 서비스 입니다.

✔** 주요** 활용** 사례

- 안동시 문화관광과** 지원으로** 외국인** 여행객** 대상** 실서비스** 운영
- 탈춤축제** 등** 지역축제 기간 전통주, 전통식당 홍보 기능 제공
- 챗봇 세계관 확장시켜 독립운동+보드게임 와디즈 **113%** 펀딩** 성공
- 프로젝트 기반 콘텐츠(독립운동+보드게임) 교육부** 장관상** 수상
- 이후 투자** 유치** 및** 고도화** 진행** 중![ref3]

🧩** 구현된** 기능



|기능|설명|
| - | - |
|🗺 지역 선택 UI|시/도 → 시·군·구 선택 후 어시스턴트 매칭|
|🧠 AI 챗봇|OpenAI Responses API 기반 문화 안내|
|🔍 File Search|벡터 기반 문서 검색(RAG)으로 근거 기반 답변 제공|
|🎤 Whisper STT|웹 음성 녹음 → Whisper-1 전송|



|기능|설명|
| - | - |
|🗣 OpenAI TTS|assistant.voice 기반 음성 출력|
|🌐 5개국어|한/영/일/프/독 지원|
|🔖 태그 추천|문화·전통주·독립운동 기반 추천|
|🧭 프리뷰 페이지|사진·설명·연관 어시스턴트 제공|
|🛠 관리자(Admin)|지역/태그/어시스턴트 관리|
|🔐 Redis Token Limit|IP 기반 하루 토큰 제한|

📂** 프로젝트** 구조도![ref1]

culture\_chatbot/![](Aspose.Words.32c84c2c-235c-4678-a8ef-39a4ef724c2f.005.png)

├─ manage.py

├─ culture\_chatbot/ │  ├─ settings.py

│  ├─ urls.py

│  └─ ...

├─ assistant/

│  ├─ models.py

│  ├─ views.py

│ ├─ urls.py

│  ├─ api\_urls.py │  ├─ utils.py

│  ├─ serializers.py │  ├─ translation.py │  └─ admin.py ├─ templates/

├─ static/

├─ locale/

├─ media/

├─ data/

└─ requirements.txt

🛠** 기술** 스텍



|**Category**|**Technologies**|
| - | - |
|**Backend**|Django 4.2 · DRF · MySQL · Redis · django-modeltranslation · python- dotenv · Gunicorn · Nginx|
|**AI**|OpenAI Responses API · File Search(RAG) · Whisper STT · OpenAI TTS|
|**Frontend**|Django Template · HTML/CSS/JS · Swiper.js · Django i18n · jsi18n|
|**Infra**|Vultr Ubuntu Server · Nginx Reverse Proxy · HTTPSCertbot) · .env 기 반 운영|

🏗** 프로젝트 URL & API 구조

이 프로젝트는 페이지** 라우팅과 **API** 라우팅을** 명확하게** 분리하고![](Aspose.Words.32c84c2c-235c-4678-a8ef-39a4ef724c2f.006.png)

i18n(다국어 URL  **OpenAI** 기반** 챗봇 **API**를** 함께** 사용하는** 구조로** 설계되었습니다**.**

📍페이지 **URL** 목록 **(**사용자에게 보여지는 페이지는 모두 다국어** 지원**(i18n)** 을 기반으로 라우팅)



|**URL**|설명|
| - | - |
|/|메인 페이지 (지역 선택 진입점)|
|/local/|지역 선택 UI|
|/thema/|테마 기반 카테고리 페이지|
|/independence/|독립운동 인물/역사 콘텐츠|
|/sommelier/|전통주 소믈리에 페이지|
|/search/|검색 결과 페이지|
|/chatbot\_preview/<id>/|어시스턴트 상세 & 프리뷰|
|/chatbot/<id>/|실제 AI 챗봇 대화 페이지|

📌**Assistant API **페이지와 다르게, API는 언어와** 무관한** 고정 **URL**



|**Endpoint**|**Method**|**Description**|
| - | - | - |
|/api/assistant/list/|GET|지역/카테고리 기반 어시스턴트 목록 조회|
|/api/assistant/chatbot/<id>/|POST|챗봇 대화 (OpenAI Responses  RAG)|
|/api/assistant/stt/|POST|Whisper STT 음성→텍스트)|
|/api/assistant/tts/|POST|OpenAI TTS 텍스트→음성)|

🔧** 데이터** 구조

![](Aspose.Words.32c84c2c-235c-4678-a8ef-39a4ef724c2f.007.jpeg)

※ 다국어는 django-modeltranslation을 사용하며, Assistant의 name, greeting, welcome\_message, question\_110 필드에 대해 ko/en/ja/fr/de 5개 언어 필드가 자동 확장.![ref2]

🧪** 시스템** 흐름도

flowchart LR![](Aspose.Words.32c84c2c-235c-4678-a8ef-39a4ef724c2f.008.png)

%% 1행 (왼쪽 → 오른쪽)

A"👤 사용자<br>(텍스트/음성 입력)"]

 B"🌐 프론트엔드<br>HTML · CSS · JS"]![](Aspose.Words.32c84c2c-235c-4678-a8ef-39a4ef724c2f.009.png)

B  C"🖥 Django API 서버<br>· 요청 검증<br>· Redis 토큰 체크<br>· MySQL 조회"]

%% 꺾임 (아래로 이동)

C  D"🔍 File Search<br>(임베딩 기반 문단 검색)<br>text-embedding- 3"}}

%% 2행 (왼쪽 → 오른쪽)

D  E"🤖 Responses API<br>근거 기반 답변 생성"]

E  F"🔊 OpenAI TTS<br>텍스트 → mp3 변환"]

F  G"💬 프론트엔드 UI<br>· 텍스트 출력<br>· mp3 자동 재생<br>· 타이핑 효 과"]

G  H"🎯 최종 사용자 경험"]

%% 보조 흐름: STT 위에서 아래로)

B  STT"🎤 Whisper STT<br>음성 → 텍스트"] STT  C

%% RAG OFF 우회 흐름 C |RAG OFF| E

🧪** 마주한** 위기와** 해결



|구분|문제|해결|결과|
| - | - | - | - |
|🔧 1. 다국어 시스템 (i18n + modeltranslation) 충돌 해결|<p>- 정적 번역(i18n)과 DB 번역 (modeltranslation)이 서로 다른 기준으로 작동</p><p>- URL 언어 프리픽스(/en/, /ja/)와 DB 필드 언어 불일치</p><p>- 일부 페이지에서 UI 언어와 DB 데이터 언어가 섞여 출력 되는 문제 발생</p>|<p>- 언어 프리픽스를 기준 으로 DB 언어 필드를 자 동 매핑하는 로직 구현</p><p>- i18n.js  Django i18n</p><p>&emsp;+ modeltranslation을 하나의 언어 파이프라인 으로 통합</p><p>- 캐시된 모델 데이터를 언어별로 분리해 반환하 도록 API 구조 개선</p>|<p> UI와 DB 데이터 가 5개국어에서 완 전 동기화</p><p>• 언어 전환 시 페 이지 전체가 즉시 갱신</p>|
|🎤 2. Whisper STT  TTS 동시 사용 시 오디오 피드 백 루프 문제| TTS가 출력한 음성이 STT 입력으로 다시 들어가는 피드 백 루프 발생|<p>- isSpeaking , ![](Aspose.Words.32c84c2c-235c-4678-a8ef-39a4ef724c2f.010.png)isRecording 상태 플래그 기반 상태 머신 설계</p><p>- STT 시작 시 TTS 음소</p>|<p>•• 음성 기반 대화 안정화</p><p>• 중복 응답률 0% 달성</p>|



||• 녹음 중 음성 출력 시 중복 응답 또는 무한 응답 발생|<p>거 처리</p><p>• debounce + r lock으로 race condition 제거</p><p>equest</p>||
| :- | :- | - | :- |
|🔍 3. File Search(RAG) 품질 편차 및 불필요한 벡 터 검색 문제|<p>- document\_id 없는 Assistant도 RAG 쿼리가 실 행되어 엉뚱한 문단 검색</p><p>- 유사 키워드가 많은 문화/ 전통주 데이터에서 매칭 정확 도 흔들림</p>|<p> Assistant별 RAG ON/OFF 플래그 도입</p><p>- document\_id 없을 때 벡터 검색 완전 비활성화</p><p>- “키워드 검색 + 임베딩 검색ˮ의 하이브리드 구조 로 품질 보정</p><p>- Responses API 프롬 프트에 근거 문단 구조화 하여 삽입</p>|<p>- 근거 기반 답변 품질 향상</p><p>- 불필요한 벡터 검색 제거로 응답 성능 개선</p>|
|⚙ 4. 서버 배포 (Nginx + Gunicorn) 안정화 과정|<p>- 초기 Gunicorn 서비스가 권한 문제로 반복 종료</p><p>- 정적 파일 경로 mismatch</p><p>&emsp;로 이미지 404 빈번</p><p>&emsp;• CORS/ALLOWED\_HOSTS 설정 오류로 API 호출 실패 발생</p><p>- 외부 MySQL 연결 시 설정 충돌</p>|<p>- systemd 환경변수 정</p><p>비 → Gunicorn 안정화</p><p>- Nginx 정적 파일 루트 경로 통일</p><p>- HTTPSCertbot) 인증</p><p>&emsp;& 자동갱신 설정</p><p>- MySQL 외부 커넥션 구조 분리 및 환경변수화</p>|<p>- 1년 이상 무중단 운영</p><p>- 실제 트래픽 증 가 상황에서도 안 정성 유지</p>|
|<p>🗺 5. 지역 기반 동 적 로딩(Province</p><p> City) 다국어 처 리 문제</p>|<p> AJAX로 로드된 지역 데이 터가 UI 언어와 불일치</p><p>• modeltranslation과 JS i18n 충돌</p>|<p>- 지역 데이터를 locale 기반으로 자동 변환하는 middleware 구현</p><p>- 지역 캐싱 구조를 언어 별로 분리</p>|• 지역 선택 UI 언 어 일관성 100%|
|<p>💬 6. 대화 UI/UX 개선</p><p>(자동 스크롤, 액션 버튼, 프리뷰)</p>|<p>- 긴 응답에서 자동 스크롤 미 작동</p><p>- 모바일 화면에서 버튼 UI가 콘텐츠를 가림</p><p>- 답변 후 액션 버튼(복사/좋 아요/싫어요) 동적 생성 필요</p>|<p>• IntersectionObserver 기반 자동 스크롤 구현</p><p>• 프리뷰 페이지 추천 구 역 ON/OFF 기능 추가 • createActionButtons() 로 동적 액션 버튼 생성</p>|• 자연스러운 사용 자 경험 구현|

👨‍💻 **My Role![ref2]**

- Django 백엔드 전체 설계 및 구현
- 프론트엔드 템플릿 및 UI 개발
- OpenAI Responses · Whisper STT · TTS 연동
- 다국어(i18n + modeltranslation) 구조 설계
- Nginx  Gunicorn 서버 배포
- Redis 기반 토큰 제한 시스템 구축
- 관리자 페이지 개발
- 데이터 구축(문화·독립운동·전통주 등)![ref3]
Andong Cul tural AI Chatbot  챗봇 9

[ref1]: Aspose.Words.32c84c2c-235c-4678-a8ef-39a4ef724c2f.001.png
[ref2]: Aspose.Words.32c84c2c-235c-4678-a8ef-39a4ef724c2f.003.png
[ref3]: Aspose.Words.32c84c2c-235c-4678-a8ef-39a4ef724c2f.004.png
