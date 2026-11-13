# 한국 LLM 개발사의 실제 진전(2024~2026.11)과 미·중 대비 위치

- 작성 기준일: 2026-11-13. 아래 모든 URL의 접근일은 2026-11-13이다.
- 검증 대상 주장: "LG 등 LLM 서비스를 지향하는 한국 기업들은 거의 향상이 없고 정체되어 있다."
- 표기 규칙
  - **[1차·원문]**: 기업 보도자료, 모델 카드, 평가기관 사이트·데이터 파일을 직접 열어 읽음.
  - **[2차·원문]**: 언론 기사 본문을 직접 열어 읽음(수치의 원출처는 기사에 인용된 기관).
  - **[2차·스니펫]**: 검색 결과 요약으로만 확인. 본문 미확인이므로 인용 전 재확인 필요.
  - **(자체 보고)**: 기업이 스스로 측정·발표한 수치. **(제3자)**: 외부 기관 측정.
  - **불확실**: 확인하지 못했거나 출처 간 충돌이 있는 항목.
- 조사 한계: LMArena는 접속 차단(HTTP 403)으로 확인하지 못했다. Stanford AI Index 2026 원문, 각 사 IR·DART 원문은 열지 못했고 언론 보도로 대체했다.

---

## 1. 개발사별 출시 이력·모델 규모·공개 여부·학습 컴퓨팅 (2024~2026)

### Takeaway
"향상이 거의 없다"는 주장은 출시 이력만 보면 맞지 않는다. LG·SKT·업스테이지·모티프는 2024년 말 32B급에서 2026년 7~8월 250B~750B급 MoE(Mixture-of-Experts) 모델로 규모를 키웠고 대부분 가중치를 공개했다. 반면 네이버·카카오·KT·삼성은 같은 기간 프런티어급 범용 모델 경쟁에서 한발 물러나 있어, "한국 기업" 전체로 묶으면 그림이 갈린다.

### Cited Findings

**Epoch AI "Notable AI Models" 데이터(제3자, 2026-10-28까지 수록) [1차·원문]** — [Epoch AI CSV](https://epoch.ai/data/notable_ai_models.csv). 파라미터·학습 연산량(FLOP)·하드웨어는 Epoch의 기록·추정치다.

| 공개일 | 모델 | 개발사 | 파라미터 | 학습 연산량(FLOP) | 학습 하드웨어 |
|---|---|---|---|---|---|
| 2024-12-09 | EXAONE 3.5 32B | LG AI연구원 | 32B | 1.25e24 | 기록 없음 |
| 2025-03-16 | EXAONE Deep 32B | LG AI연구원 | 32B | 1.26e24 | H100 512장 |
| 2025-07-15 | EXAONE 4.0 (32B) | LG AI연구원 | 32B | 2.69e24 | H200 512장 |
| 2025-12-29 | HyperCLOVA X SEED 32B Think | 네이버 | 32B | 기록 없음 | 기록 없음 |
| 2025-12-30 | A.X K1 | SK텔레콤 | 519B | 기록 없음 | H200 1,536장 |
| 2025-12-30 | VAETKI | NC AI | 100B | 기록 없음 | H100 1,016장 |
| 2025-12-31 | K-EXAONE | LG AI연구원 | 236B | 1.52e24 | B200 512장 |
| 2025-12-31 | Solar Open 100B | 업스테이지 | 102B | 1.4e24 | 기록 없음 |
| 2026-04-09 | EXAONE 4.5 | LG AI연구원 | 33.2B | 3.85e24 | 기록 없음 |
| 2026-06-28 | Solar Open2 250B | 업스테이지 | 250.3B | 1.05e24 | B200·H200 1,656장 |
| 2026-07-29 | A.X K2 | SK텔레콤 | 688B | 1.8e24 | 기록 없음 |
| 2026-07-31 | K-EXAONE 2.0 | LG AI연구원 | 750B | 3.55e24 | 기록 없음 |
| 2026-08-07 | Motif-3 | 모티프테크놀로지스 | 314B | 1.1e24 | B200 768장 |

- **LG AI연구원**
  - K-엑사원(236B-A23B)은 2026년 1월 공개. LG는 "보유 데이터의 절반 정도만 사용해 1차수 모델을 만들었다"고 밝혔다 (자체 보고) [1차·원문] — [LG 보도자료 29770](https://www.lg.co.kr/media/release/29770)
  - Hugging Face 등록일 기준 K-EXAONE-236B-A23B 2025-12-26, EXAONE-4.5-33B 2026-04-04, K-EXAONE-2.0-750B-A37B 2026-07-29. 모두 가중치 공개 [1차·원문] — [Hugging Face API](https://huggingface.co/api/models?author=LGAI-EXAONE&sort=createdAt&direction=-1&limit=12)
  - 2026-11-09 'K-엑사원 2.5' API 무료 개방. 8월 2차 모델에 추가 학습을 적용한 "기술 검증 모델"이며, 24개 지표 종합 성능이 8월 모델 대비 70% 이상 향상됐다고 발표 (자체 보고, 내부 분석) [1차·원문] — [LG 보도자료 30760](https://lg.co.kr/media/release/30760)
  - LG는 "내년 1월까지 프런티어급 성능의 엑사원 모델 완성"을 목표로 제시 (자체 보고, 계획) [1차·원문] — [LG 보도자료 30760](https://lg.co.kr/media/release/30760)
  - 2026-09-14 'LG AI 토크 콘서트 2026'에서 범용 모델보다 산업 특화 모델(EXAONE Tabular, Discovery, Business Intelligence)을 전면에 내세움. 임우형 공동 연구원장은 "훌륭한 답을 내는 범용 모델은 이미 많다"는 취지로 발언 [2차·원문] — [Korea Times](https://www.koreatimes.co.kr/business/companies/20260914/lg-ai-research-seeks-to-address-industrial-challenges-with-expert-ai-models)
- **SK텔레콤**
  - A.X K2: 총 688B, 활성 33B, MoE(라우팅 전문가 256개), Apache-2.0 공개 가중치, 사전학습 약 8.2조 토큰, 컨텍스트 256K. 전작 A.X K1은 519B [1차·원문] — [A.X K2 모델 카드](https://huggingface.co/skt/A.X-K2)
  - 후속 모델을 조 단위 파라미터로 확장할 계획 (자체 보고, 계획) [2차·스니펫] — [SKT 뉴스룸](https://news.sktelecom.com/229153)
- **업스테이지**
  - Solar Open 2: 총 250B, 활성 15B, 사전학습 약 12조 토큰, B200 GPU 200만 GPU시간, 컨텍스트 1M. 라이선스는 자체 'Upstage Solar License'(표준 오픈소스 라이선스 아님) [1차·원문] — [Solar Open2 모델 카드](https://huggingface.co/upstage/Solar-Open2-250B)
  - 상용 API 모델 'Solar Pro 4'가 Artificial Analysis에 등재돼 있음(공개일·규모는 확인 못함) [1차·원문] — [Artificial Analysis](https://artificialanalysis.ai/leaderboards/models)
- **모티프테크놀로지스**
  - Motif 3: 총 314B, 활성 13.2B, MIT 라이선스, 사전학습 약 12.5조 토큰. 아키텍처를 자체 설계했다고 설명 [1차·원문] — [Motif-3 모델 카드](https://huggingface.co/Motif-Technologies/Motif-3)
- **네이버**
  - 2025년 4월 SEED 경량 3종 공개, 2025-06-30 추론 모델 HyperCLOVA X THINK 발표, 2025년 7월 SEED 14B Think 공개. 이후 SEED 32B Think·SEED 8B Omni 공개 [2차·스니펫] — [바이라인네트워크](https://byline.network/2025/06/30_naver_hyperclovaxthink/), [네이버 보도자료](https://navercorp.com/media/pressReleasesDetail?seq=34214)
  - 2026년에 32B를 넘는 신규 범용 모델을 공개했다는 자료는 찾지 못함(아래 Gaps).
- **KT**
  - 믿:음 K 2.0(2025): 11.5B Base, 2.3B Mini. 믿:음 K 2.5 Pro(2026): 32B, B2B용 비공개 모델 [2차·원문] — [딜사이트](https://dealsite.co.kr/articles/168235)
- **카카오**
  - Hugging Face에 kanana-2-30b-a3b-instruct-2601, kanana-2-3b-instruct 등 30B 이하 모델 공개 [1차·원문] — [Hugging Face API](https://huggingface.co/api/models?author=kakaocorp&sort=downloads&direction=-1&limit=6)
  - 2026-10-13 개발자 행사에서 난도별 모델 분담(SLM·온디바이스·플래그십), 어려운 요청은 "프론티어 모델에 맡긴다"는 전략 발표 [2차·원문] — [바이라인네트워크](https://byline.network/2026/10/14_29182883)
- **삼성전자**
  - 가우스2는 2024년 공개(콤팩트·밸런스드·슈프림 3종), 사내 코딩 지원 등에 활용. 2026년 신규 가우스 모델 소식은 찾지 못함 [2차·스니펫] — [테크42](https://www.tech42.co.kr/?p=93238)
- **트릴리온랩스**
  - Tri-21B, Tri-70B, 확산 기반 Trida-7B 등 공개. Hugging Face에 Gravity-30B-A5B 등 등록 [2차·스니펫] — [바이라인네트워크](https://byline.network/?p=9004111222577227); [1차·원문] — [Hugging Face API](https://huggingface.co/api/models?author=trillionlabs&sort=downloads&direction=-1&limit=6)
- **NC AI**: 독파모 1차 모델 VAETKI(100B) 공개 후 1차 평가에서 탈락 [1차·원문] — [Epoch AI CSV](https://epoch.ai/data/notable_ai_models.csv)
- **솔트룩스**: 루시아3 LLM·Deep·VLM 3종, 2026년 5월 온톨로지 결합 플랫폼 공개. 대표가 "순수 LLM만으로는 한계"라는 취지로 발언 [2차·스니펫] — [MTN](https://news.mtn.co.kr/news-detail/2026051209402959958)

### Inferences
- LG의 공개 모델은 2024-12(32B) → 2026-07(750B)로 약 23배 커졌고 Epoch 추정 학습 연산량은 1.25e24 → 3.55e24 FLOP으로 약 2.8배 늘었다. 규모는 커졌지만 연산량 증가는 그에 못 미친다.
- 독파모 참여 4개사의 2026년 모델은 모두 Epoch 추정 1e24~4e24 FLOP 범위에 몰려 있다. 정부 지원 GPU(팀당 수백~1,000장대)가 사실상 학습 규모의 상한으로 작용한 것으로 보인다.
- 네이버·KT·카카오의 공개 모델은 2026년에도 32B 이하에 머문다. "정체"라는 표현은 이들 기업의 범용 모델 규모에는 들어맞고, 독파모 잔류 3사에는 들어맞지 않는다.

### Gaps
- 미·중 프런티어 모델의 학습 연산량과 직접 비교할 수치는 이번 조사에서 수집하지 못했다.
- 네이버의 2026년 신규 모델 목록, Solar Pro 4의 공개일·규모, 삼성 가우스의 2025~2026년 버전은 확인하지 못했다.
- 코난테크놀로지의 모델 사양은 확인하지 못했다(실적만 확인, 3번 항목).

---

## 2. 독립 벤치마크 위치와 미·중 대비 격차

### Takeaway
제3자 측정에서 한국 모델은 2026년 내내 미국 프런티어와 중국 상위 모델보다 뚜렷이 낮다. 2026년 8월 AAII v4.1.1에서 한국 최고점은 47점(미국 최고 63점)이었고, 11월의 새 지수 v5에서는 점수가 매겨진 한국 모델이 14점·8점(최고 65점, 중국 최고 46점)이다. 다만 한국 모델 자체는 세대마다 크게 향상됐으므로, "향상이 없다"기보다 "향상했지만 격차는 좁혀지지 않았다"가 자료에 더 가깝다. 격차의 추세는 지수 버전이 바뀌어 엄밀히 판정할 수 없다.

### Cited Findings

**Artificial Analysis Intelligence Index(AAII) — 제3자**

- 2026년 1월: K-엑사원(236B) 32점, 오픈 웨이트 모델 기준 세계 7위·국내 1위. 당시 오픈 웨이트 상위 10개는 중국 6, 미국 3, 한국 1 (점수는 제3자 측정, 순위 해석은 LG 보도자료) [1차·원문] — [LG 보도자료 29770](https://www.lg.co.kr/media/release/29770)
- 2026-08-13 AAII v4.1.1: 모티프3 47점, 솔라 오픈2 37점, A.X-K2 35점, K-엑사원 2.0 31점 [2차·원문] — [아이뉴스24](https://inews24.com/view/1994693)
- 같은 시점 프런티어: 클로드 오퍼스 63점, 페이블5 62점, GPT 5.6 61점. 독파모 목표인 "프런티어의 95%"를 충족하려면 57점 이상이어야 한다는 계산 [2차·원문] — [머니투데이](https://www.mt.co.kr/article/2026081812375747016)
- 2026-11-13 AAII v5(v5.0.1) 리더보드 [1차·원문] — [Artificial Analysis](https://artificialanalysis.ai/leaderboards/models)
  - 미국: Claude Fable 5.2 (max) 65, Gemini 4 Carbon (high) 60, Claude Opus 5.5 (max) 59, GPT-6 Astra (max) 57, Muse Wonder Full (max) 50
  - 중국: Kimi K3.1 Pro 46, Tencent Hy4 35, Qwen3.8 Max 34, DeepSeek V4.1 Flash (max) 33, GLM-5.3 (max) 32
  - 한국: Solar Pro 4 14, K-EXAONE 2.0 8
  - 점수 없이 등재만 된 한국 모델: A.X-K2, Motif 3, Solar Open2 250B, EXAONE 4.5 33B, HyperCLOVA X SEED Think (32B), Mi:dm K 2.5 Pro, Tri-21B-Think 등
- 정부는 벤치마크 과적합('벤치맥싱') 의혹에 대해 Artificial Analysis에 분석을 의뢰했고, 과적합·암기를 입증할 단서를 찾지 못했다는 답을 받았다고 밝힘 [2차·원문] — [머니투데이 일문일답](https://www.mt.co.kr/tech/2026/08/18/2026081812313869772)
- KT 믿:음 K 2.5 Pro가 AAII 48점이라는 개인 게시물이 있으나 리더보드에는 점수가 없다. **불확실** [2차·스니펫] — [LinkedIn 게시물](https://kr.linkedin.com/in/hojae-lee-kr)

**세대 간 향상 — 자체 보고(모델 카드)**

- A.X K1 → A.X K2: KMMLU-Pro 68.9 → 80.5, Humanity's Last Exam 8.3 → 27.8, LiveCodeBench v6 74.9 → 84.0, AA-LCR 26.0 → 66.0 (자체 보고, 일부 항목은 Artificial Analysis 측정) [1차·원문] — [A.X K2 모델 카드](https://huggingface.co/skt/A.X-K2)
- 같은 표에서 A.X K2는 수학·한국어에서 비교 대상 중 최고점이지만 에이전트 항목은 중국 모델보다 낮다: Terminal Bench v2.1 36.0(Kimi-K2.6 65.9), BrowseComp 9.3(GLM-5.1 29.1), GDPval Elo 1031(GLM-5.1 1257) [1차·원문] — [A.X K2 모델 카드](https://huggingface.co/skt/A.X-K2)
- Solar Open 100B → Solar Open 2: SWE-Bench Verified 15.4 → 70.4, GPQA-Diamond 66.2 → 86.3, HLE 11.5 → 28.8. DeepSeek-V4-Flash(73.8 / 88.9 / 32.3)에는 대부분 근소하게 못 미침 (자체 보고) [1차·원문] — [Solar Open2 모델 카드](https://huggingface.co/upstage/Solar-Open2-250B)
- Motif 3: SWE-Bench Verified 76.2(GLM-5.1 76.4, Qwen-3.7 max 80.4), Terminal-Bench 2.1 74.9(Qwen-3.7 max 75.0) (자체 보고, 타 모델 점수는 리더보드 인용) [1차·원문] — [Motif-3 모델 카드](https://huggingface.co/Motif-Technologies/Motif-3)
- K-엑사원 2.5: AutomationBench 74.6(딥시크 V4.1 Flash 74.9, GLM 5.3 max 71.6), Claw-Eval 77.3(75.8 / 77.6), BrowseComp 78.0(75.8 / 79.0), SWE-Bench Pro 59.2(58.4 / 64.0) (자체 보고, 오픈 데이터셋 기반 자체 측정) [1차·원문] — [LG 보도자료 30760](https://lg.co.kr/media/release/30760)
- SKT A.X K2: IMO 2026 문제 42점 만점 중 29점(금메달 기준선), MathArena AIME 2026 공동 최고점. 중국 dots-note-3.0은 42점 만점 (자체 보고, MathArena는 외부 리더보드) [1차·원문] — [SKT 뉴스룸](https://news.sktelecom.com/229153)

**Epoch AI 주목할 만한 모델 수 — 제3자 [1차·원문]** — [Epoch AI CSV](https://epoch.ai/data/notable_ai_models.csv). 공개 연도별로 직접 집계했고, 다국적 모델은 국가별로 중복 계산했다.

| 공개 연도 | 미국 | 중국 | 한국 |
|---|---|---|---|
| 2023 | 133 | 33 | 4 |
| 2024 | 79 | 33 | 1 |
| 2025 | 69 | 43 | 8 |
| 2026 (10-28까지) | 63 | 31 | 5 |

- 2024년 이후 한국 14개 중 9개가 LG AI연구원 모델이다 [1차·원문] — [Epoch AI CSV](https://epoch.ai/data/notable_ai_models.csv)

**Stanford AI Index 2026**

- 2025년 출시 주목할 만한 모델 수에서 한국이 미국(50개)·중국(30개)에 이어 3위. 당초 5개였으나 과기정통부 요청으로 8개로 정정 예정이라고 과기정통부가 2026-04-23 발표 [2차·원문] — [아시아경제 영문판](https://www.asiae.co.kr/en/article/2026042314254059369)
- 같은 보고서가 한국의 민간 AI 투자 부진과 인재 순유출(OECD 38개국 중 35위)을 지적했다는 요약이 있음 [2차·스니펫] — [Pebblous](https://blog.pebblous.ai/report/hai-ai-index-2026-part2/en/)

**Hugging Face 최근 30일 다운로드 — 제3자 [1차·원문]** (API의 downloads 값, 2026-11-13 조회)

- 한국: EXAONE-3.5-7.8B-Instruct 410,490 / Solar-Open-100B 88,133 / A.X-K2-NVFP4 83,675 / EXAONE-4.5-33B 23,057 / K-EXAONE-2.0-750B-A37B 14,184 / Solar-Open2-250B 8,131 / A.X-K2 4,576 / Motif-3 2,383 — [LG](https://huggingface.co/api/models?author=LGAI-EXAONE&sort=downloads&direction=-1&limit=6), [업스테이지](https://huggingface.co/api/models?author=upstage&sort=downloads&direction=-1&limit=6), [SKT](https://huggingface.co/api/models?author=skt&sort=downloads&direction=-1&limit=6), [모티프](https://huggingface.co/api/models?author=Motif-Technologies&sort=downloads&direction=-1&limit=6)
- 중국·미국: Qwen3-0.6B 19,718,599 / DeepSeek-V3.2 8,260,197 / GLM-5.3-Flash 6,397,774 / gemma-4-31B-it 6,692,367 / gpt-oss-20b 5,685,450 / Kimi-K3 772,893 — [Qwen](https://huggingface.co/api/models?author=Qwen&sort=downloads&direction=-1&limit=3), [DeepSeek](https://huggingface.co/api/models?author=deepseek-ai&sort=downloads&direction=-1&limit=3), [Z.ai](https://huggingface.co/api/models?author=zai-org&sort=downloads&direction=-1&limit=3), [Google](https://huggingface.co/api/models?author=google&sort=downloads&direction=-1&limit=3), [OpenAI](https://huggingface.co/api/models?author=openai&sort=downloads&direction=-1&limit=3), [Moonshot](https://huggingface.co/api/models?author=moonshotai&sort=downloads&direction=-1&limit=3)
- K-엑사원은 공개 직후 Hugging Face 트렌드 2위에 올랐다고 LG가 발표 (자체 보고) [1차·원문] — [LG 보도자료 29770](https://www.lg.co.kr/media/release/29770)

### Inferences
- 같은 지수 버전 안에서의 비율: 2026년 8월(v4.1.1) 한국 최고 47 / 미국 최고 63 = 약 75%, LG 31 / 63 = 약 49%. 2026년 11월(v5) Solar Pro 4 14 / 65 = 약 22%, K-EXAONE 2.0 8 / 65 = 약 12%, 중국 최고 46 / 65 = 약 71%.
- v5에서 한국 비율이 급락한 것처럼 보이지만 해석에 주의가 필요하다. 지수 구성이 바뀌었고, 8월 한국 최고점이던 Motif 3·A.X-K2·Solar Open2는 v5 점수가 아직 없다. 이 숫자만으로 "격차가 벌어졌다"고 단정할 수 없다.
- 그래도 v5에서 중국 상위 오픈 웨이트(DeepSeek 33, GLM 32)와 K-EXAONE 2.0(8)의 차이는 크다. LG가 K-엑사원 2.5로 이 두 모델과 "경쟁 가능"하다고 주장한 것은 자체 측정이며, 제3자 검증은 아직 없다.
- LG는 독파모 1차(2026-01)에서 세 평가 부문 모두 1위였으나 2차(2026-08) AAII에서는 4개 팀 중 최하위(31점)였다. 저자가 LG를 지목한 직관과 부합하는 자료이나, 같은 기간 LG 모델 자체는 32점(1월, 구버전 지수) 모델에서 750B 모델로 바뀌었고 11월에 70% 개선을 주장했다. "상대적으로 뒤처졌다"와 "향상이 없다"는 구분해야 한다.
- 한국 모델의 강점은 수학·한국어 벤치마크에, 약점은 에이전트·코딩 실행 벤치마크에 몰려 있다(SKT 모델 카드 기준). 최신 지수가 에이전트 과제 비중을 키웠다면 한국 모델에 불리하게 작용했을 수 있다(v5 구성은 확인하지 못함).
- Hugging Face 다운로드에서 한국 최다 모델(약 41만)은 Qwen 최다 모델(약 1,972만)의 약 2% 수준이고, 한국에서 가장 많이 받는 모델은 2024년 12월의 소형 EXAONE 3.5다. 2026년 대형 모델의 실사용은 제한적이다.

### Gaps
- **LMArena**: 접속 차단으로 확인 못함.
- **한국 벤치마크**(KMMLU, KoBEST, HAE-RAE, Open Ko-LLM Leaderboard, 호랑이 리더보드): 리더보드 원문을 열지 못했다. 확인한 것은 SKT 모델 카드의 KMMLU-Pro·KoBALT·CLIcK 자체 보고뿐이다.
- 2024년 시점의 AAII 한·미·중 점수를 확보하지 못해 "2024년 대비 격차 변화"는 정량 판정 불가. AAII v5의 구성 항목과 변경 사유도 확인하지 못했다.
- Stanford AI Index 2026 원문에서 한국 수치와 정정 반영 여부를 직접 확인하지 못했다.
- 2026년 1월 K-엑사원 32점 당시의 프런티어 점수와 지수 버전을 확인하지 못했다.

---

## 3. 상업적 성과: 이용자, 매출, 도입

### Takeaway
소비자 시장에서 한국 서비스는 뚜렷이 밀리고 있다. 2026년 10월 챗GPT·제미나이·클로드가 수백만~2,500만 명대인 반면 에이닷은 약 90만~107만, 뤼튼은 37만 명이고 전년 대비 감소했다. B2B에서는 업스테이지·코난테크놀로지의 LLM 매출이 빠르게 늘었으나 절대 규모가 수백억 원대이고 적자다.

### Cited Findings

**모바일 앱 MAU**

- 와이즈앱·리테일, 2026년 10월: 챗GPT 2,551만, 제미나이 914만, 클로드 500만(전년 동월 46만), 코파일럿 195만, 퍼플렉시티 134만, 그록 129만, 에이닷 89만, 뤼튼 37만. 표본조사 추정치이며 PC 웹 이용은 제외 [2차·원문] — [파이낸셜뉴스](https://www.fnnews.com/news/202611100846384439)
- 와이즈앱·리테일, 2026년 9월: 챗GPT 2,470만, 제미나이 987만, 클로드 404만, 에이닷 110만, 뤼튼 38만. 상위 10개 앱 중복 제외 이용자 3,075만(전년 동월 대비 +19%) [2차·원문] — [바이라인네트워크](https://byline.network/2026/10/13_2918273-4/)
- 와이즈앱, 2026년 2월: 뤼튼 135만, 에이닷 119만 [2차·스니펫] — [AI매터스](https://aimatters.co.kr/news-report/46796/)
- 모바일인덱스, 2026년 10월: 챗GPT 18,762,276명(전년 동월 13,048,025명), 클로드 2,095,157명(전년 139,131명), 에이닷 약 107만(전년 대비 -42.5%). 조사 대상 AI 앱 이용자 중 챗GPT 이용 비율 약 84% → 약 91% [2차·원문] — [메트로신문](https://www.metroseoul.co.kr/article/20261108500058)
- SKT는 에이닷이 "월간 사용자 1,000만 명 규모"라고 밝힘 (자체 보고). 와이즈앱·모바일인덱스 수치와 약 10배 차이가 나며, 집계 범위 차이로 보이나 **불확실** [2차·원문] — [인사이트](https://www.insight.co.kr/news/568910)
- 카카오 '카나나' 앱은 2026-10-15 서비스 종료(2025년 5월 베타 출시) [2차·원문] — [MTN](https://news.mtn.co.kr/news-detail/2026091514285345922)
- 카나나 MAU가 출시 직후 69,631명에서 10,488명으로 줄었다는 모바일인덱스 인용 보도 [2차·스니펫] — [다음 뉴스](https://v.daum.net/v/W2VFKLx2H2)
- 네이버 '클로바X'와 AI 검색 '큐:'는 출시 약 2년 8개월 만에 종료. 기사에는 "지난 9일"로만 표기돼 정확한 월은 **확인 필요**(2023년 8월 출시 기준 2026년 4월로 추정) [2차·원문] — [디지털 인사이트](https://ditoday.com/?p=142700)

**결제·구독**

- 한경에이셀(신용카드 결제 데이터 기반 추정): 국내 생성형 AI 결제 점유율 챗GPT 76.9%(2025년 1분기) → 48.5%(2026년 1분기), 클로드 6.7% → 31.7%. 2026년 3월에는 클로드 42.4%, 챗GPT 40.4% [2차·원문] — [다음 뉴스(한국경제)](https://v.daum.net/v/20260426174335658)
- 카카오톡 내 '챗GPT 포 카카오' 누적 가입자 1,100만 명 돌파, MAU는 전 분기 대비 약 2배 (자체 보고, 2026-05-07 1분기 실적 발표) [2차·원문] — [SBS Biz](https://biz.sbs.co.kr/amp/article/20000308721)

**매출·기업 가치**

- 업스테이지: 매출 2024년 138억 원 → 2025년 248억 원(+79%), 영업적자 지속. 2026년 3월 시리즈 C 기업가치 1조 6,000억 원, 상장 희망 기업가치 3조 5,000억~5조 원 [2차·원문] — [비즈워치](https://news.bizwatch.co.kr/article/mobile/2026/05/12/0014)
- 업스테이지 2024년 영업손실 402억 원 [2차·스니펫] — [스마트투데이](https://www.smarttoday.co.kr/ko-kr/articles/99331)
- 업스테이지는 포털 다음 운영사 AXZ를 인수하고 2026-06-16 '업스테이지 컴퍼니' 출범. 다음 주간 이용자 1,000만 명, 타임리 600여 기관 (자체 보고) [2차·원문] — [뉴시스](https://mobile.newsis.com/view/NISX20260616_0003671084)
- 업스테이지의 약 2,000억 원 프리IPO에 기존 주요 투자자들이 불참 [2차·원문] — [딜사이트](https://dealsite.co.kr/articles/168342)
- 코난테크놀로지: 매출 2023년 244억 → 2024년 263억 → 2025년 340억 원. 영업손실 110억·141억·99억 원. LLM 매출 2024년 11억 → 2025년 88억 원, 2026년 상반기 35억 원(전체의 43.4%) (DART 인용) [2차·원문] — [딜사이트](https://dealsite.co.kr/articles/169083)
- LG 사내 적용 사례: EXAONE Discovery가 LG생활건강 후보 물질 42만 개를 하루 만에 선별(통상 22개월), EXAONE Tabular가 제조 현장 모델 변경 대응 시간을 85% 단축 (자체 보고) [2차·원문] — [Korea Times](https://www.koreatimes.co.kr/business/companies/20260914/lg-ai-research-seeks-to-address-industrial-challenges-with-expert-ai-models)
- 국내 기업의 55.7%가 생성형 AI를 전사 또는 일부 부서에서 활용(CIO Korea 설문 884명, 2025년 10~11월) [2차·스니펫] — [CIO Korea](https://www.cio.com/article/4045735)

### Inferences
- 소비자 앱 기준으로 한국 서비스의 위치는 "정체"보다 나쁜 "후퇴"다. 에이닷·뤼튼 이용자는 줄었고 클로바X·카나나 앱은 종료됐다. 같은 기간 시장 전체는 커졌다.
- 이용자 감소가 곧 모델 성능 정체를 뜻하지는 않는다. 뤼튼은 자체 파운데이션 모델 회사가 아니고, 네이버·카카오는 별도 챗봇 앱을 접고 기존 서비스에 AI를 넣는 쪽으로 옮겼다.
- B2B·공공에서는 성장 신호가 있다(업스테이지 +79%, 코난 LLM 매출 8배). 다만 매출 규모가 수백억 원대라 미·중 선두 기업과 같은 척도로 비교하기 어렵다.

### Gaps
- 각 사의 API 사용량, 유료 고객 수, 국산 대 외산 모델의 기업 도입 점유율을 직접 보여주는 자료는 찾지 못했다.
- 네이버의 사우디·태국 수출 실적, 공공 부문 계약 규모는 확인하지 못했다.
- 업스테이지 2026년 실적, 상장 일정 확정 여부는 **불확실**(보도마다 다름).
- 카나나 MAU와 2026년 2월 와이즈앱 수치는 스니펫으로만 확인했다.

---

## 4. 전략적 후퇴·전환·제휴

### Takeaway
2026년에 네이버·카카오·KT는 프런티어 범용 모델 경쟁에서 서비스·인프라·제휴 쪽으로 무게를 옮겼다. 반대로 LG·SKT·업스테이지는 정부 과제 안에서 대형 모델 개발을 이어가고 있다. LG도 대외 메시지는 산업 특화 모델에 무게를 싣고 있다.

### Cited Findings
- **네이버**: 독파모 탈락 후 재공모에 "검토하지 않는다"고 밝힘 [2차·스니펫] — [뉴시스](https://www.newsis.com/view/NISX20260115_0003478770)
- 네이버가 하이퍼클로바X를 엔비디아 '네모트론 3 울트라' 기반으로 고도화하고, 자체 LLM 경쟁보다 AI 검색 서비스 중심으로 이동한다는 분석 [2차·원문(기사 요약·도입부)] — [딜사이트](https://dealsite.co.kr/articles/166551)
- 네이버는 2026년 7월 엔비디아 대상 10억 달러 제3자 배정 유상증자를 결정, 2026-10-27 브룩필드와 90억 달러 컴퓨팅 인프라 계약. GPU 임대에 자체 모델·서비스를 얹는 '네오클라우드' 형태 [2차·원문] — [비즈워치](https://news.bizwatch.co.kr/article/mobile/2026/11/02/0028/)
- **카카오**: 2025-10-28 카카오톡에 '챗GPT 포 카카오' 탑재 [2차·스니펫] — [뉴시스](https://www.newsis.com/view/NISX20251028_0003379420)
- 카카오 정신아 대표는 2026-08-06 실적 발표에서 대규모 AI 인프라 사업에 적극 나서지 않겠다고 밝힘. 모델·서비스에 집중하고 인프라는 외부 협력 활용 [2차·원문] — [머니투데이](https://www.mt.co.kr/tech/2026/08/08/2026080710413460885)
- 카카오는 독파모 재공모에도 불참 [2차·스니펫] — [헤럴드경제](https://www.heraldk.com/article/2026011518241406921)
- **KT**: 5년간 18조 원 투자 계획 중 AI 인프라(AIDC·해저케이블)에 6조 원. 박윤영 대표는 KT를 "무대 위 주인공이 아니라 무대를 비추는 조명"에 비유. 기사는 "AI 기술 기업보다 인프라 사업자 색채가 짙다"고 평가 [2차·원문] — [딜사이트](https://dealsite.co.kr/articles/165235)
- KT는 2026년 8월 믿:음 K 2.5 Pro와 리벨리온 NPU를 묶은 구축형 제품 출시(공공·국방·금융 대상) [2차·원문] — [딜사이트](https://dealsite.co.kr/articles/168235)
- **SK텔레콤**: 2026-07-24 엔비디아와 최대 2GW AIDC 협력, 앤트로픽과 국내 GW급 AI 데이터센터 투자·협력 추진, AWS와 울산 AIDC 확대 [2차·원문] — [파이낸셜뉴스](https://www.fnnews.com/news/202607260912143864)
- SKT는 에이닷·A.X K2·데이터센터를 묶어 정부 '모두의 AI' 사업에 컨소시엄으로 참여 [2차·원문] — [인사이트](https://www.insight.co.kr/news/568910)
- **삼성전자**: 2026-02-22 갤럭시 플래그십에 구글 제미나이 외 퍼플렉시티를 기본 탑재한다고 발표, '멀티 AI' 전략 [2차·스니펫] — [삼성 뉴스룸](https://news.samsung.com/uk/galaxy-ai-expands-multi-agent-ecosystem-to-give-users-more-choice-and-flexibility)
- **LG**: Artificial Analysis 공동 창립자가 LG의 특화 모델 노선을 인프라 비용 장벽을 감안한 실리적 선택으로 평가했다는 보도 [2차·스니펫] — [비즈워치](https://news.bizwatch.co.kr/article/industry/2026/09/14/0027)
- **업스테이지**: 포털 다음 인수, 퓨리오사AI NPU 결합으로 "풀스택" 구성 [2차·원문] — [머니투데이](https://www.mt.co.kr/article/2026081812375747016)

### Inferences
- 플랫폼·통신 대기업 다수가 "모델을 직접 만들어 이긴다"에서 "남의 모델도 쓰면서 서비스·인프라로 번다"로 이동했다. 저자의 "정체" 인식은 이 전략 전환을 성능 정체로 읽은 것일 수 있다.
- LG는 양면적이다. 정부 과제에서는 750B 모델과 "2027년 1월 프런티어급" 목표를 내걸고, 대외 행사에서는 범용 모델 경쟁의 의미를 낮춰 말한다.
- SKT는 자체 모델을 키우면서 동시에 앤트로픽·엔비디아·AWS와 인프라 제휴를 맺고 있어, 자체 개발과 제휴가 배타적이지 않다.

### Gaps
- KT–마이크로소프트 제휴의 2026년 현황(SOTA K 포함), SK–OpenAI·삼성–OpenAI 협력 내용은 이번 조사에서 자료를 찾지 못했다.
- 감원·조직 개편·핵심 인력 이탈에 대한 신뢰할 만한 자료를 찾지 못했다.
- 네이버의 네모트론 기반 고도화는 딜사이트 기사 요약으로만 확인했으며 네이버 공식 발표는 확인하지 못했다. **확인 필요**.

---

## 5. 정부 '독자 AI 파운데이션 모델(독파모)' 단계평가 결과

### Takeaway
1차(2026-01)에서 네이버클라우드·NC AI가 탈락했고, 2차(2026-08)에서 추가 합류한 모티프가 글로벌 벤치마크 1위임에도 탈락했다. 정부 스스로 최고 모델도 프런티어의 95% 목표에 못 미친다고 인정하고 사업 재편을 예고했다.

### Cited Findings
- **1차 평가(2026-01-15 발표)**: 5개 팀(네이버클라우드, 업스테이지, SKT, NC AI, LG AI연구원) 중 네이버클라우드·NC AI 탈락 [2차·원문] — [SBS Biz](https://biz.sbs.co.kr/amp/article/20000285199)
- LG AI연구원이 세 부문 모두 최고점: 벤치마크 33.6/40, 전문가 31.6/35, 사용자 25.0/25. NIA 벤치마크는 SKT·LG가 9.2/10, 글로벌 공통 벤치마크는 LG 14.4/20 [2차·원문] — [SBS Biz](https://biz.sbs.co.kr/amp/article/20000285199)
- LG는 1차 평가 13개 벤치마크 중 10개에서 1위, 평균 72점이라고 발표 (자체 보고) [1차·원문] — [LG 보도자료 29770](https://www.lg.co.kr/media/release/29770)
- 네이버클라우드는 성능이 아니라 '독자성' 기준 부적격으로 탈락. 정부는 독자 모델을 "해외 모델의 미세조정이 아닌, 설계부터 사전학습 전 과정을 수행한 국산 모델"로 규정하고 가중치 초기화를 최소 요건으로 삼음 [2차·원문] — [헤럴드경제](https://www.heraldk.com/article/2026011423560506561)
- 네이버 모델의 이미지·음성 인코더에 알리바바 큐웬(Qwen) 2.5 계열이 쓰였고 비전 인코더 코사인 유사도 99.5%라는 분석이 제기됨 [2차·스니펫] — [노컷뉴스](https://www.nocutnews.co.kr/news/6457194)
- 당초 1개 팀만 탈락시키려던 계획이 2개 팀 탈락으로 바뀌었고, 기업이 고른 개별 벤치마크가 점수에 반영된 점을 두고 공정성 논란. 국회예산정책처도 2026-01-22 보고서에서 논란을 언급 [2차·원문] — [Pebblous](https://blog.pebblous.ai/report/korea-dokpamo-benchmark-scorecard-2026-08/ko/)
- 추가 공모에 네이버·카카오·NC AI는 불참, 모티프테크놀로지스와 트릴리온랩스가 도전 [2차·스니펫] — [유니콘팩토리](https://www.unicornfactory.co.kr/article/2026012011314144167)
- **2차 평가(2026-08-18 발표, 08-27 세부 점수 공개)** [2차·원문] — [MTN](https://news.mtn.co.kr/news-detail/2026082720102251703)

| 팀 | 종합(100) | 벤치마크(40) | 전문가(35) | 사용자(25) | AAII 원점수 |
|---|---|---|---|---|---|
| SK텔레콤 | 70.6 | 22.2 | 29.3 | 19.1 | 35 |
| 업스테이지 | 69.9 | 22.7 | 29.1 | 18.1 | 37 |
| LG AI연구원 | 69.0 | 20.6 | 29.5 | 18.9 | 31 |
| 모티프테크놀로지스(탈락) | 65.8 | 24.6 | 27.1 | 14.1 | 47 |

- AAII 원점수 출처 [2차·원문] — [아이뉴스24](https://inews24.com/view/1994693)
- 사용자 평가는 AI 전문 사용자 49명과 일반 국민 185명이 참여 [2차·원문] — [MTN](https://news.mtn.co.kr/news-detail/2026082720102251703)
- 모티프는 세부 점수 공개를 요구하며 이의 제기. AAII 원점수 격차가 배점 환산에서 줄었다는 점을 문제 삼음 [2차·스니펫] — [MTN](https://news.mtn.co.kr/news-detail/2026082708384979814)
- 류제명 2차관은 "프론티어 모델에 버금갈 수 있는 방식으로 재편하자는 공감대가 있다"고 발언. 한정된 예산을 여러 기업에 나누기보다 한 곳에 집중 지원하는 방안을 검토 [2차·원문] — [머니투데이 일문일답](https://www.mt.co.kr/tech/2026/08/18/2026081812313869772), [머니투데이](https://www.mt.co.kr/article/2026081812375747016)
- 잔류 3개 팀에 대한 GPU 지원을 768장에서 1,000장으로 확대할 계획. 최종 2개 팀 선정 시점은 보도마다 다름(연말 또는 내년 상반기). **불확실** [2차·스니펫] — [디지털데일리](https://www.ddaily.co.kr/page/view/2026081811112476409)
- "탈락 낙인" 우려로 기업들이 도전을 꺼린다는 비판 보도 [2차·스니펫] — [MTN](https://news.mtn.co.kr/news-detail/2026082015220930821)

### Inferences
- 정부 평가 자체가 "향상은 있으나 프런티어에는 못 미친다"는 결론을 담고 있다. 최고점 47점 대 목표선 57점이라는 정부 측 계산이 그 근거다.
- LG는 1차 전 부문 1위에서 2차 종합 3위·AAII 최하위로 내려갔다. 다만 네 팀의 종합 점수 차는 4.8점, 잔류 3팀은 1.6점 차로 근소하다.
- 글로벌 벤치마크 1위 팀이 사용자 평가로 탈락한 구조는, 평가가 "모델 성능"보다 "활용·확산"에 무게를 뒀음을 보여준다. 이 사업 순위를 모델 성능 순위로 읽으면 안 된다.

### Gaps
- 과기정통부 보도자료 원문을 직접 열지 못했고 모든 점수는 언론 보도를 거쳤다.
- 1차 평가의 팀별 전체 점수는 공개되지 않았다(부문별 최고점만 공개).
- 3차 평가 일정과 재편안의 확정 내용은 확인하지 못했다.

---

## 6. 투자 규모: AI 설비투자와 GPU 보유

### Takeaway
한국 기업의 AI 인프라 투자는 2026년에 조 단위 계약으로 커졌지만 미국 4대 빅테크의 연간 설비투자(약 7,250억 달러)와는 자릿수가 두세 개 다르다. 한국 모델의 학습에 실제 쓰인 GPU는 팀당 수백~1,600장대로 확인된다.

### Cited Findings
- 구글·아마존·마이크로소프트·메타의 2026년 설비투자 계획 합계 7,250억 달러, 전년(4,100억 달러) 대비 +77%(파이낸셜타임스 집계 인용) [2차·원문] — [Tom's Hardware](https://www.tomshardware.com/tech-industry/big-tech/big-techs-ai-spending-plans-reach-725-billion)
- 알파벳은 2026년 설비투자 계획을 최대 2,050억 달러로 상향 [2차·스니펫] — [파이낸셜뉴스](https://www.fnnews.com/news/202607260912143864)
- 네이버: 2025년 설비투자 1조 3,171억 원 중 약 88%가 데이터센터 서버·비품. 2026년 1월 엔비디아 B200 4,000장 클러스터 구축. 2026-08-07 GPU·CPU 감가상각 기간을 5년에서 6년으로 변경(연 약 1,000억 원 비용 이연) [2차·원문] — [머니투데이](https://www.mt.co.kr/tech/2026/08/08/2026080710413460885)
- 네이버–브룩필드 90억 달러 계약: 각 세종에서 2027년 상반기 55MW, 2027년 말 100MW, 2028년 200MW(GPU 약 10만 장 수용 규모). 네이버의 사용료 지급 보증액은 최대 18조 7,400억 원 [2차·원문] — [비즈워치](https://news.bizwatch.co.kr/article/mobile/2026/11/02/0028/), [머니투데이](https://www.mt.co.kr/tech/2026/08/08/2026080710413460885)
- 네이버가 엔비디아 블랙웰 GPU 6만 장 확보를 발표(2025년 11월 3분기 실적 발표) [2차·스니펫] — [디지털데일리](https://www.ddaily.co.kr/page/view/2025110511015654112)
- 네이버·카카오 2026년 1분기 연구개발비: 네이버 6,020억 원(매출 대비 18.6%), 카카오 3,316억 원(17.1%). AI 외 서비스 개발비 포함 [2차·원문] — [SBS Biz](https://biz.sbs.co.kr/amp/article/20000327497)
- KT: 5년간 AI 인프라에 6조 원 [2차·원문] — [딜사이트](https://dealsite.co.kr/articles/165235)
- SKT: AI 데이터센터를 2029년 5GW 규모로 확대 계획 (자체 보고) [2차·원문] — [인사이트](https://www.insight.co.kr/news/568910)
- 정부 '모두의 AI' 사업은 2~3개 사업자에 2026년 B200 GPU 최대 512장 배분 [2차·원문] — [딜사이트](https://dealsite.co.kr/articles/165585)
- 모델별 학습 GPU(Epoch 기록): K-EXAONE B200 512장, A.X K1 H200 1,536장, VAETKI H100 1,016장, Solar Open2 B200·H200 1,656장, Motif-3 B200 768장 [1차·원문] — [Epoch AI CSV](https://epoch.ai/data/notable_ai_models.csv)

### Inferences
- 네이버의 2025년 설비투자(약 1.3조 원)는 미국 4대 빅테크 2026년 계획 합계의 약 0.1% 수준이다(환율 가정에 따라 달라지는 대략의 비교).
- 한국의 대형 인프라 계약(네이버–브룩필드, SKT–엔비디아)은 자체 모델 학습용이라기보다 GPU 임대·데이터센터 사업 성격이 강하다. 인프라 투자 확대가 곧 모델 개발 투자 확대를 뜻하지 않는다.
- 모델 학습에 쓴 GPU가 수백~1,600장대라는 점은 2번 항목의 성능 격차를 설명하는 유력한 요인이지만, 인과를 입증하는 자료는 아니다.

### Gaps
- 중국 기업(알리바바, 텐센트, 바이트댄스)의 2026년 설비투자 수치를 확보하지 못했다.
- LG AI연구원·카카오·SKT·업스테이지의 AI 전용 설비투자액과 GPU 보유량 공시는 찾지 못했다. LG의 GPU 보유량은 **불확실**.
- 미·중 프런티어 연구소의 모델별 학습 GPU 수와 직접 비교할 자료를 수집하지 못했다.

---

## 종합: 주장에 대한 증거 정리

### Takeaway
"거의 향상이 없고 정체"라는 문장은 그대로는 지지되지 않는다. 자료가 지지하는 더 정확한 서술은 "독파모 참여사들은 2년간 모델을 크게 키우고 성능을 올렸지만, 제3자 지수에서 미국·중국 상위 모델과의 격차는 여전히 크고, 소비자 시장에서는 오히려 후퇴했으며, 네이버·카카오·KT는 범용 모델 경쟁에서 물러났다"이다.

### Cited Findings
- **주장을 지지하는 증거**
  - AAII v5(2026-11)에서 한국 모델 14점·8점, 미국 최고 65점, 중국 최고 46점 (제3자) — [Artificial Analysis](https://artificialanalysis.ai/leaderboards/models)
  - 정부가 인정한 목표 미달: 최고 47점 대 목표선 57점 (2026-08) — [머니투데이](https://www.mt.co.kr/article/2026081812375747016)
  - LG가 2차 평가 AAII에서 4팀 중 최하위 — [아이뉴스24](https://inews24.com/view/1994693)
  - 에이닷 이용자 전년 대비 -42.5%, 클로바X·카나나 앱 종료 — [메트로신문](https://www.metroseoul.co.kr/article/20261108500058), [디지털 인사이트](https://ditoday.com/?p=142700), [MTN](https://news.mtn.co.kr/news-detail/2026091514285345922)
  - 네이버·카카오·KT의 전략 전환 — [딜사이트](https://dealsite.co.kr/articles/166551), [머니투데이](https://www.mt.co.kr/tech/2026/08/08/2026080710413460885), [딜사이트](https://dealsite.co.kr/articles/165235)
- **주장에 반하는 증거**
  - LG 공개 모델 32B(2024-12) → 750B(2026-07), 2026-11 추가 70% 개선 주장(자체 보고) — [Epoch AI CSV](https://epoch.ai/data/notable_ai_models.csv), [LG 보도자료 30760](https://lg.co.kr/media/release/30760)
  - SKT·업스테이지의 세대 간 큰 폭 향상(자체 보고) — [A.X K2 모델 카드](https://huggingface.co/skt/A.X-K2), [Solar Open2 모델 카드](https://huggingface.co/upstage/Solar-Open2-250B)
  - Epoch 주목 모델 수 한국 2024년 1개 → 2025년 8개, Stanford AI Index 3위(2차 자료) — [Epoch AI CSV](https://epoch.ai/data/notable_ai_models.csv), [아시아경제](https://www.asiae.co.kr/en/article/2026042314254059369)
  - 업스테이지 매출 +79%, 코난 LLM 매출 11억 → 88억 원 — [비즈워치](https://news.bizwatch.co.kr/article/mobile/2026/05/12/0014), [딜사이트](https://dealsite.co.kr/articles/169083)
  - 2026년 1월 K-엑사원이 오픈 웨이트 세계 7위 (제3자 점수) — [LG 보도자료 29770](https://www.lg.co.kr/media/release/29770)

### Inferences
- 저자가 "LG"를 대표 사례로 든 것은 약점이 있다. LG는 Epoch 주목 모델 수 국내 최다, 독파모 1차 전 부문 1위였고 모델 규모를 가장 크게 키웠다. 다만 가장 최근의 제3자 점수(v5 8점, 8월 AAII 최하위)는 저자 쪽에 유리하다.
- "향상 없음"(절대적 정체)과 "격차 미축소"(상대적 정체)를 구분하면 전자는 반증되고 후자는 대체로 지지된다. 저자의 의도가 어느 쪽인지는 저자에게 확인해야 한다.
- 2026년의 긍정적 증거 상당수는 자체 보고이거나 정부 과제 맥락의 수치다. 제3자 측정만 놓고 보면 그림이 더 어둡다.

### Gaps
- 2024년 기준선의 제3자 점수가 없어 "2년간 격차가 좁혀졌나 벌어졌나"는 정량적으로 답하지 못했다.
- 뉴시스 기사에 "미국 정부가 최상위 AI 모델의 외국인 접근을 전면 차단"했다는 서술이 있으나 이번 조사에서 별도 확인하지 못했다. 사실이라면 소버린 모델 논의의 전제가 바뀌므로 **확인 필요** — [뉴시스](https://mobile.newsis.com/view/NISX20260616_0003671084)
