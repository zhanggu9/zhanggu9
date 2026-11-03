<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F2027,50:203A43,100:2C5364&height=200&section=header&text=YOUNG-CHAE%20LIM&fontSize=56&fontColor=ffffff&fontAlignY=36&desc=Portfolio%20Manager%20%C3%97%20Quant%20%C3%97%20Trading%20Systems&descSize=18&descAlignY=58&animation=fadeIn" width="100%" />

# 임영채 (Young-Chae Lim)

**펀드를 운용하던 사람이, 이제는 운용 시스템을 직접 만듭니다.**

자산운용사·벤처캐피탈에서 펀드 책임운용, 투자심사, PI 운용을 했습니다. 지금은 그 경험을 코드로 옮겨
가설을 세우고 → 백테스트와 실계좌로 검증하고 → 결과를 다시 규칙에 반영하는 **퀀트 자동매매 시스템**을 설계·운영합니다.

`Portfolio Management` · `Quant Research` · `Algorithmic Trading` · `Risk Control` · `Applied AI`

[![GitHub](https://img.shields.io/badge/GitHub-zhanggu9-181717?style=flat&logo=github&logoColor=white)](https://github.com/zhanggu9)
![투자자산운용사](https://img.shields.io/badge/투자자산운용사-2019-0A5BD8?style=flat)

---

## 🙋‍♂️ About Me

**승률보다 기대값, 신호보다 리스크 가드.**

- 💼 **Fund Management** — 공모주·코넥스하이일드 펀드 책임운용, 운용사 설립 인가 실무, 투자조합 운용·투자심사
- 📈 **Quant & Trading** — 키움·한국투자증권 API로 실계좌 자동매매 엔진을 직접 운영, LEAN 백테스트 플랫폼 구축
- 🧠 **ML & AI** — LightGBM·XGBoost 신호 모델, LLM 진입·보유 판단을 쓰되 주문 권한은 hard safety guard 뒤에 둠
- 🛠 **How I build** — AI 코딩 에이전트(Claude Code 등)와 함께 개발합니다. 범위·설계 결정·검증 기준과 테스트는 제가 정하고 책임집니다

## 🔭 What I'm doing now

- **KORStockScan** 실계좌 스캘핑 엔진 운영 — 매일 장후 리포트로 다음 장전 정책을 bounded 갱신
- 이스트소프트 **AI퀀트 과정** 수강 중 (2026.06 ~) — 글로벌 ETF 자산배분 로보어드바이저 (평균분산·Risk Parity, walk-forward 백테스트)

---

## 🔥 Featured Projects

> 실계좌 코드는 키·계좌·전략 파라미터 보호를 위해 일부 비공개이며, 설계 기록으로 대신 공개합니다.
> LIMSON은 한국투자증권 공식 저장소를 기반으로 확장한 프로젝트로, 원본 커밋 이력을 그대로 보존했습니다.

### 1. [LIMSON](https://github.com/zhanggu9/limson) — 전략 빌더 · LEAN 백테스트 플랫폼

`2026` `개인 프로젝트` `백엔드 · 인프라` `+35 커밋 / +2,400줄`

> 한국투자증권 공식 전략 빌더·LEAN 백테스터를 자체 OHLCV DB와 저사양 클라우드 환경에 맞게 확장

**📌 문제** — 원본은 KIS API로 시세를 받아 백테스트해 느리고 호출 제한이 있으며, 42GB짜리 LEAN 엔진은 1GB 메모리 서버(t3.micro)에서 돌릴 수 없었습니다.

**✅ 해결**

- 자체 수집 **PostgreSQL OHLCV 데이터 공급자** 추가 (식별자 검증으로 SQL 인젝션 차단)
- 불완전한 벤치마크 곡선을 결과에서 제외하고 단계별 실행 시간 로깅 → 백테스트 결과 신뢰성 확보
- **웹은 EC2, 백테스트는 로컬 PC**에서 실행하고 SSH 역터널로 연결하는 하이브리드 구조, nginx 단일 포트 + systemd 배포 자동화

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)
![LEAN](https://img.shields.io/badge/QuantConnect%20LEAN-F5AE29?style=flat)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![nginx](https://img.shields.io/badge/nginx-009639?style=flat&logo=nginx&logoColor=white)
![AWS EC2](https://img.shields.io/badge/AWS%20EC2-FF9900?style=flat&logo=amazonec2&logoColor=white)

### 2. [lumina-invest](https://github.com/zhanggu9/lumina-invest) — 금융 AI 에이전트 웹앱

`2026` `AI퀀트 과정 프로젝트` `풀스택`

> ReAct 챗봇, LightGBM/MLP 퀀트 신호·백테스트, Qdrant RAG 문서 검색을 하나로 묶은 웹앱 — 화면부터 API·배포까지 풀스택으로 다뤄본 과정 프로젝트

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat&logo=tailwindcss&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

### 3. [KORStockScan](https://github.com/zhanggu9/KORStockScan-main) — 실계좌 스캘핑 자동매매 엔진

`2026` `1인 개발` `설계 · 개발 · 운영` `실계좌 운용 중`

> 시장 스캔 → AI 판단 → 주문 가드 → 분할 진입·청산 → 장후 자동 튜닝까지 하나의 lifecycle로 연결한, 매일 데이터로 스스로 보정되는 매매 엔진

**📌 문제** — 단일 날짜 승률이나 백테스트 수익률만 보고 규칙을 바꾸면 과최적화되고, AI 판단이 잘못되면 실계좌 손실로 바로 이어집니다.

**✅ 해결**

- 서로 주문·수량을 공유하지 않는 **독립 주문 owner 3종**(메인 봇 / 위젯 / 에피소드)으로 주문 귀속 분리
- 가격 freshness·호가·주문·수량·cooldown을 **hard safety**로 분리 — 튜닝과 AI가 우회 불가
- 장후 source-quality 검사 → 비용 반영 **EV·반사실 분석** → 표본 하한을 통과한 한 축만 다음 장전에 bounded 적용 + rollback

**📊 규모** — Python 모듈 800+ · 테스트 9,000+ · systemd 서비스·타이머 120+

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-2E7D32?style=flat)
![XGBoost](https://img.shields.io/badge/XGBoost-EB5B25?style=flat)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat&logo=openai&logoColor=white)
![AWS Bedrock](https://img.shields.io/badge/AWS%20Bedrock-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![DuckDB](https://img.shields.io/badge/DuckDB-FFF000?style=flat&logo=duckdb&logoColor=black)
![Kiwoom](https://img.shields.io/badge/Kiwoom%20REST%2FWS-0A5BD8?style=flat)

### 4. [Kiwoom RSI Auto Trader](https://github.com/zhanggu9/KORStockScan-main/blob/main/docs/portfolio/kiwoom-rsi-trader-case-study.md) — 멀티 전략 틱 매매 엔진 (설계 기록)

`2026` `1인 개발` `설계 · 개발` `소스 비공개`

> 키움 OpenAPI+ 실시간 틱을 집계해 전략 10종을 교체 가능하게 돌리는 엔진. KORStockScan의 전신

**✅ 핵심** — Clean Architecture로 증권사 API를 포트 뒤에 분리해 실계좌 없이 테스트 · 주문/TR 큐 분리 + 단일 워커 직렬화 · 슬라이딩 윈도우 rate limiter · 틱 폭주 시 샤드 큐 backpressure

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PyQt5](https://img.shields.io/badge/PyQt5-41CD52?style=flat&logo=qt&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-280%2B%20tests-0A9EDC?style=flat&logo=pytest&logoColor=white)

---

## 💼 Career

| 기간 | 회사 | 역할 | 주요 업무 |
| --- | --- | --- | --- |
| 2022.11 – 2024.11 | 벡터기술투자 | 전략투자본부 과장 | 투자조합 운용, 투자심사, PI·공모주 운용 |
| 2019.08 – 2021.03 | SH자산운용 | 멀티에셋팀 대리 | 펀드 책임운용역 (공모주·코넥스하이일드), 펀드 오퍼레이션, 운용사 인가 실무 |
| 2018.05 – 2019.02 | HL Investment | 리서치팀 대리 | 시황·기업 리서치, 포트폴리오 리밸런싱·리스크 점검 |

## 🎓 Credentials & Education

| 자격 · 교육 | 기관 | 시기 |
| --- | --- | --- |
| 투자자산운용사 | 한국금융투자협회 | 2019.07 |
| 증권투자권유대행인 | 한국금융투자협회 | 2018.05 |
| 벤처투자전문인력 | 한국벤처투자협회 | 2023.09 |
| 외국환업무전문인력 | 금융투자교육원 | 2020.07 |
| AI퀀트 과정 | 이스트소프트 | 2026.06 – 수강 중 |

## 🛠 Tech Stack

`Quant / ML` &nbsp;
![pandas](https://img.shields.io/badge/pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-2E7D32?style=flat)
![XGBoost](https://img.shields.io/badge/XGBoost-EB5B25?style=flat)
![Optuna](https://img.shields.io/badge/Optuna-2C5BB4?style=flat)
![LEAN](https://img.shields.io/badge/QuantConnect%20LEAN-F5AE29?style=flat)

`Trading / Data` &nbsp;
![Kiwoom](https://img.shields.io/badge/Kiwoom%20API-0A5BD8?style=flat)
![KIS](https://img.shields.io/badge/KIS%20Open%20API-1A3E8C?style=flat)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![DuckDB](https://img.shields.io/badge/DuckDB-FFF000?style=flat&logo=duckdb&logoColor=black)
![Parquet](https://img.shields.io/badge/Parquet-50ABF1?style=flat)

`AI / Infra` &nbsp;
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat&logo=openai&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux%20%2F%20systemd-FCC624?style=flat&logo=linux&logoColor=black)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white)

## 💡 일하는 원칙

1. **EV first** — 승률·단순 수익률 합이 아니라 수수료·슬리피지를 반영한 기대값으로 판단합니다
2. **Safety is not tunable** — 가격 freshness, 주문·수량 가드는 어떤 튜닝도 우회할 수 없습니다
3. **Reproducible** — 모든 매매 판단은 입력·정책 버전·결과를 남겨 사후 replay가 가능해야 합니다

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2C5364,50:203A43,100:0F2027&height=100&section=footer" width="100%" />
