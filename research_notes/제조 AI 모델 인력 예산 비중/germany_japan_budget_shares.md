# 독일(EU 포함)·일본의 제조 AI 공공지출: 모델 개발/재사용 대 현장 인력 양성 비중 (2026년 11월 기준)

조사일(접근일): 2026-11-13. 모든 URL의 접근일은 같은 날이다.

**읽는 법**

- 분류 체계: (A) 모델 개발·재사용·파인튜닝·배포, (B) 제조 데이터 수집·표준·데이터 스페이스·데이터 인프라, (C1) 현장·재직자·직업훈련·도메인 엔지니어 교육, (C2) 학위·대학 과정, (D) 컴퓨팅·물리 인프라, (E) 기타.
- 출처 등급: **[1차-원문]** = 1차 문서를 내려받아 해당 수치를 직접 읽음. **[1차-스니펫]** = 1차 사이트 문서이나 검색 결과 요약으로만 확인(원문 미열람). **[2차]** = 언론·협회 등 2차 자료.
- "판단" 표시는 분류가 조사자의 판단임을 뜻한다. 계산값은 "계산"으로 표시했다.
- 접근 제약: `bundeswirtschaftsministerium.de`(BMWE)의 HTML 페이지는 Radware CAPTCHA로 차단되어 curl과 헤드리스 Chromium 모두 본문을 읽지 못했다(우회 시도하지 않음). 같은 사이트의 PDF 1건(Manufacturing-X 브로슈어)은 내려받아 읽었다. `bundeshaushalt.de`의 2026년 개별계획(Einzelplan) PDF는 503 오류, `web.archive.org`는 연결이 끊겼다. 따라서 독일 연방예산 타이틀 단위 수치는 확인하지 못했다.

---

## 핵심 질문 1. 독일(EU 자금 포함): Manufacturing-X, 산업 AI 프로그램, 재직자 훈련 지출

### Takeaway

독일 연방정부의 제조 분야 디지털 지출 중 1차 문서로 항목별 확인이 되는 것은 Manufacturing-X이며, 이것은 전액 (B) 데이터 스페이스·표준이지 모델 개발이 아니다(핵심 11개 과제 국가지원 약 1.53억 유로, 2024~2027). 제조용 파운데이션 모델(foundation model)에 해당하는 연방 전용 예산 항목은 찾지 못했고, 재직자 훈련은 고용보험(BA) 재원으로 연 13억 유로(2025년, 전 산업) 규모여서 **같은 분모로 묶은 비중은 계산할 수 없다**.

### Cited Findings

#### 표 1-1. Manufacturing-X 핵심 과제 11개 (BMWE 브로슈어, 기준 시점 2026년 3월) [1차-원문]

출처: BMWE, "Manufacturing-X" 프로그램 브로슈어(Stand März 2026) — [bundeswirtschaftsministerium.de PDF](https://www.bundeswirtschaftsministerium.de/Redaktion/DE/Publikationen/Digitale-Welt/manufacturing-x-programm.pdf?__blob=publicationFile&v=27)

"국가지원액"은 브로슈어의 과제 총액 × BMWE 지원율로 조사자가 계산한 값이다(브로슈어에는 총액과 지원율만 있음).

| 과제 | 내용(브로슈어 부제) | 기간 | 과제 총액(백만 유로) | BMWE 지원율 | 국가지원액(계산, 백만 유로) | 분류 |
|---|---|---|---|---|---|---|
| Factory-X | 공장 설비 산업 데이터 스페이스 (Siemens·SAP 주관, 46개 파트너) | 2024-02 ~ 2026-06 | 149 | 47.9% | 71.4 | B |
| Aerospace-X | 항공우주 공급망 데이터 생태계 (Airbus) | 2024-04 ~ 2026-06 | 39.5 | 49.1% | 19.4 | B |
| Semiconductor-X | 반도체 공급망 디지털화 (Intel Deutschland) | 2024-05 ~ 2026-09 | 30.4 | 56.1% | 17.1 | B |
| CX-NEXT | Catena-X Automotive Network NEXT (BMW) | 2024-08 ~ 2026-09 | 25.2 | 44.3% | 11.2 | B |
| Chem-X | 화학산업 데이터 생태계, 디지털 제품 여권 (BASF) | 2024-12 ~ 2026-11 | 19.5 | 45.8% | 8.9 | B |
| DataFleX | 전력망 유연성 연결 데이터 생태계 (TenneT) | 2025-10 ~ 2027-01 | 12.6 | 57.3% | 7.2 | B |
| Robot-X | Catena-X와 AI를 이용한 로봇의 모델 기반 개발·운영 | 2024-04 ~ 2026-06 | 9.9 | 46% | 4.6 | B (판단: AI 요소 있으나 데이터 생태계 과제) |
| Decide4ECO | 순환 가치창출 의사결정 지원 데이터 생태계 | 2024-04 ~ 2026-09 | 6 | 52.8% | 3.2 | B |
| HealthTrack-X | 보건산업 생산·공급망 (Roche) | 2024-05 ~ 2026-07 | 5.3 | 57.3% | 3.0 | B |
| SCALE-MX | Manufacturing-X 기술이전 확산 (VDMA·ZVEI) | 2024-10 ~ 2026-09 | 4.4 | 84.9% | 3.7 | E (판단: 중소기업 대상 이전·확산. 교육 요소가 있으면 C1 일부) |
| DAVID | 자산관리셸(Asset Administration Shell) 적용 지원 | 2024-05 ~ 2026-07 | 3 | 93.3% | 2.8 | B (표준) |
| **합계(계산)** | | | **304.8** | | **152.5** | |

- 브로슈어 본문은 "137개 세부과제, 총 규모 약 3.08억 유로, 국가지원 약 1.53억 유로 승인", "89개 제안 중 11개 연합과제 선정"이라고 적고 있어 위 계산 합계(152.5)와 맞는다. [1차-원문] — [BMWE 브로슈어](https://www.bundeswirtschaftsministerium.de/Redaktion/DE/Publikationen/Digitale-Welt/manufacturing-x-programm.pdf?__blob=publicationFile&v=27)
- **문서 내 불일치**: 같은 브로슈어 본문은 Factory-X를 "약 1.53억 유로 규모로 2024년 2월 2일 시작"이라고 쓰고, 과제 표지에는 "149 Mio. EUR(지원율 47.9%)"로 적는다. 1.53억은 프로그램 전체 국가지원액과 같은 숫자여서 본문 쪽이 혼동일 가능성이 있다(추정, 확인 필요). [1차-원문] — 같은 문서
- BMWE 도시에(Dossier) 페이지는 "약 1.4억 유로", "124개 이상 기업·연구기관", "15개 유스케이스"(2025-10-16 기준)라고 적는다고 검색 요약에 나온다. 원문은 CAPTCHA로 열람하지 못했다. [1차-스니펫] — [BMWE Dossier](https://www.bundeswirtschaftsministerium.de/Redaktion/DE/Dossier/manufacturing-x.html)
- 2023년 8월 공고 당시 규모는 "최대 1.5억 유로"였다. [1차-스니펫] — [BMWK 보도자료 2023-08-21](https://www.bundeswirtschaftsministerium.de/Redaktion/DE/Pressemitteilungen/2023/08/20230821-foerderaufruf-manufacturing-x-zum-bau-des-digitalen-oekosystems-gestartet.html). 공고문 원문(연방관보)에서는 과제 기간 "통상 30개월 이내", 지침 효력 "2026-12-31까지"를 직접 확인했다(총액은 관보 본문 검색에서 확인하지 못함). [1차-원문] — [BAnz AT 18.08.2023 B1](https://www.bundesanzeiger.de/pub/publication/CdbQD7Ob1ph0219js0B/content/CdbQD7Ob1ph0219js0B/BAnz%20AT%2018.08.2023%20B1.pdf)
- Factory-X "8,000만 유로 지원" 보도는 통보 예정액을 전한 언론 보도다. 위 계산값 7,140만 유로와 다르다. [2차] — [Handelsblatt](https://www.handelsblatt.com/technik/it-internet/factory-x-siemens-und-sap-planen-neue-cloud-fuer-die-industrie/29508128.html)

#### 표 1-2. "확장된 Manufacturing-X 과제 지형"(다른 프로그램 재원 포함) [1차-원문]

출처: 같은 BMWE 브로슈어. 국가지원액은 계산값.

| 과제 | 내용 | 기간 | 총액(백만 유로) | 지원율 | 지원액(계산) | 분류 |
|---|---|---|---|---|---|---|
| RoX | AI 기반 로보틱스 디지털 생태계 (ABB, 23개 파트너) | 2024-09 ~ 2027-02 | 51.4 | 52.1% | 26.8 | B/A 혼합 (판단: 분리 불가) |
| Construct-X | 건설·플랜트 데이터 협업 | 2025-03 ~ 2028-02 | 42.5 | 66.1% | 28.1 | B |
| DIAMOND | 중립 데이터 포맷 설비 모델링 (BMW) | 2022-11 ~ 2025-10 | 26.5 | 47.3% | 12.5 | B |
| Fluid 4.0 | 유체기술 데이터 생태계 (Bosch Rexroth) | 2024-01 ~ 2026-07 | 13.4 | 60% | 8.0 | B |
| growING | 디지털 트윈 공동 엔지니어링 (Bosch) | 2024-11 ~ 2027-01 | 12.8 | 47.2% | 6.0 | B |
| Railway-X | 철도산업 데이터 스페이스 | 2025-01 ~ 2026-12 | 12.1 | 45.9% | 5.6 | B |
| energy data-X | 에너지산업 데이터 스페이스 (PT Jülich) | 2023-10 ~ 2026-09 | 9.5 | 약 60% | 5.7 | B |
| Wind-X | 풍력산업 데이터 스페이스 | 2024-11 ~ 2027-07 | 5.5 | 58.7% | 3.2 | B |
| Antrieb 4.0 | 전기 구동 시스템 실증 | 2023-01 ~ 2026-05 | 5.1 | 94.7% | 4.8 | B |
| **합계(계산)** | | | **178.8** | | **약 100.7** | |

#### 표 1-3. 산업 AI·로보틱스·컴퓨팅 관련 항목 (확인된 금액만)

| 항목 | 금액·기간 | 내용 | 분류 | 출처 등급·URL |
|---|---|---|---|---|
| Robotics Institute Germany (RIG, BMFTR) | 2,017.7만 유로, 2024-07-01 ~ 2028-06-30 | 로봇 연구 거점 네트워크 | C2/E (판단: 연구 네트워크) | [1차-원문] [BT-Drs. 21/6189](https://dserver.bundestag.de/btd/21/061/2106189.pdf) (2026-05-27) |
| BMWE 로보틱스 R&D | 금액 미제시. "BMWE 지원은 기술 개방형(technologieoffen)" | 로보틱스 전용 예산 구분 없음 | 분류 불가 | [1차-원문] 같은 문서 |
| Robo-Hubs(AI 기반 로보틱스 혁신랩 개념 공모, BMFTR) | 연합과제당 120만 유로, 24~30개월. 총액 미기재 | 중소기업 대상 로봇 혁신랩 | E/C1 혼합 (판단) | [1차-원문] [BAnz AT 25.06.2026 B2](https://www.bundesanzeiger.de/pub/publication/cfyovDNzNru1xp9Tfa3/content/cfyovDNzNru1xp9Tfa3/BAnz%20AT%2025.06.2026%20B2.pdf) |
| InProKI(AI 통합 생산시스템, BMFTR "Zukunft der Wertschöpfung") | 연합과제당 약 500만~1,000만 유로. 총액 미기재 | 생산 현장 AI 솔루션과 "필요한 역량" 구축 | A(응용)/C1 혼합 (판단) | [1차-원문] [BAnz AT 17.03.2026 B1](https://www.zukunft-der-wertschoepfung.de/wp-content/uploads/2026/02/InProKI_BAnz-AT-17.03.2026-B1.pdf) |
| KI-Robotikbooster (Hightech Agenda, BMFTR) | **금액 확인 못함** | 다목적 로봇 선도과제, embodied AI 쇼케이스, 연구 인프라 확충, "실증·재교육 센터(Erprobungs- und Weiterbildungszentren)" 구축 | A/D/C1 혼합 | 내용은 [1차-원문] [BT-Drs. 21/1100 Hightech Agenda](https://dserver.bundestag.de/btd/21/011/2101100.pdf); 금액은 미확인 |
| AI Gigafactory 국내 유치 대비 재원 | 특별기금(Sondervermögen)에 8.05억 유로. EU 집행위 추정 건설비 40~50억 유로 | 대규모 AI 컴퓨팅 | D | [1차-원문] [BT-Drs. 21/5271](https://dserver.bundestag.de/btd/21/052/2105271.pdf) (2026-04-07) |
| Hightech Agenda 전체 | 2029년까지 약 180억 유로, 특별기금 약 55억 유로 | 6대 핵심기술 전체(AI만이 아님) | 분류 불가 | [2차] 검색 요약 — [Börsen-Zeitung](https://www.boersen-zeitung.de/konjunktur-politik/die-hightech-agenda-ist-prall-gefuellt) |
| BMWE "산업 AI 고혁신 과제 아이디어 공모"(2025-12-05) | **금액 확인 못함** (페이지 CAPTCHA 차단) | — | — | [BMWE 보도자료](https://www.bundeswirtschaftsministerium.de/Redaktion/DE/Pressemitteilungen/2025/12/20251205-bmwe-sucht-hochinnovative-projektideen-fuer-industrielle-ki.html) 미열람 |
| EU Apply AI Strategy | 약 10억 유로(Horizon Europe·Digital Europe 등 기존 프로그램 재원). 제조 부문 배분액 미공개 | 제조 플래그십에 "프런티어 AI 모델과 가속 파이프라인" 포함 | A 중심(부문 분리 불가) | [2차] [Pearl Cohen 요약](https://www.pearlcohen.com/eu-launches-apply-ai-strategy-to-accelerate-ai-adoption/), [Mobile World Live](https://www.mobileworldlive.com/ai-cloud/ec-sets-aside-e1b-to-fuel-ai-across-industry/) |

#### 표 1-4. 인력 양성·중소기업 지원 (C1 중심)

| 항목 | 금액·기간 | 대상 | 분류 | 출처 등급·URL |
|---|---|---|---|---|
| 연방고용청(BA) 직업 재교육 예산 2025 | 34억 유로, 그중 **재직자 자격 향상(Qualifizierung beschäftigter Menschen) 13억 유로** | 전 산업(제조 구분 없음) | C1 | [1차-원문] [BA 보도자료 2024-45](https://www.arbeitsagentur.de/presse/2024-45-investitionen-in-die-zukunft-trotz-konjunktureller-belastungen) |
| BA 재교육 지원 예산 2026 | 41.2억 유로(2025 대비 약 6.9억 유로 증가. 일부는 Jobcenter 수급자 재교육 비용 이관분). 재직자 몫은 보도자료에 없음 | 전 산업 | C1 | [1차-원문] [BA 보도자료 2025-46](https://www.arbeitsagentur.de/presse/2025-46-ba-haushalt-2026) |
| SGB III 재직자 재교육 신규 참여 | 2024년 61,517명, 2024년 전년 대비 약 35% 증가 | 전 산업 | C1 | [2차] 검색 요약(Bitkom 가이드 인용). 원 통계 미확인 — [Bitkom Leitfaden 2026](https://www.bitkom.org/sites/main/files/2026-08/bitkom-leitfaden-qualifizierung-von-beschaeftigten.pdf) |
| Zukunftszentren (BMAS, ESF Plus) | 총 약 1.25억 유로(ESF Plus + 연방), 14개 컨소시엄, 2023년 초 ~ 2026년 말. ESF Plus 몫 약 7,590만 유로 | 중소기업·재직자의 디지털 전환 상담·역량 | C1 | [1차-원문] [BMAS](https://www.bmas.de/DE/Arbeit/Fachkraeftesicherung/Fachkraeftesicherung-in-der-Praxis/Zukunftszentren/zukunftszentren.html), [esf.de](https://www.esf.de/portal/DE/ESF-Plus-2021-2027/Foerderprogramme/bmas/zukunftszentren.html) |
| Mittelstand-Digital (센터 네트워크, KI-Trainer 포함) | 2026년 5,300만 유로(기존 계획 대비 300만 유로 증액). KI-Trainer 단독 금액 없음 | 중소기업·수공업 AI 도입 지원 | E/C1 혼합 (판단) | [1차-스니펫] [BMWE Haushalt 2026](https://www.bundeswirtschaftsministerium.de/Redaktion/DE/Artikel/Ministerium/haushalt-2026.html) 원문 미열람 |
| Mittelstand-Digital 센터의 향후 | "네트워크는 2026년 말 종료, 2027년부터 축소된(verschlankt) 네트워크로 대체" | — | — | [1차-원문] [Bundesbericht Forschung und Innovation 2026, Kap. 3](https://www.bundesbericht-forschung-innovation.de/wp-content/uploads/Bundesbericht-Forschung-und-Innovation-2026_Kapitel-03.pdf) |

### Inferences

- **비중 계산 불가 선언**: 독일은 (i) 제조 AI를 하나로 묶은 예산 패키지가 없고, (ii) 데이터 스페이스는 연방 보조금(다년 과제), 재직자 훈련은 고용보험 재원(연 단위, 전 산업), 컴퓨팅은 특별기금으로 재원과 기간이 모두 다르다. 같은 분모의 비중은 낼 수 없다.
- 규모 감각만 보면(서로 다른 분모, 참고용): Manufacturing-X 핵심 11개 과제 국가지원 약 1.53억 유로는 2024~2027년 약 3년에 걸친 금액이라 연 5,000만 유로 안팎(계산)이다. BA의 재직자 자격 향상 예산은 2025년 한 해 13억 유로(전 산업)다. 제조업 몫을 알 수 없어 직접 비교는 안 되지만, 독일의 "사람" 쪽 지출은 산업정책 예산이 아니라 사회보험 제도 안에 들어 있다는 구조는 분명하다.
- 확인된 연방 항목 중 "제조용 모델 개발"(A)로만 분류되는 것은 없다. Manufacturing-X는 전부 B이고, AI 모델과 가장 가까운 Robot-X·RoX도 데이터 생태계 과제다. Hightech Agenda가 "산업용 주권·고특화 AI 모델"을 언급하는 수단은 계획 단계의 IPCEI AI이며 금액은 찾지 못했다.
- 독일 중앙정부 차원의 신규 대형 지출은 컴퓨팅(D, AI Gigafactory 8.05억 유로 대비 재원) 쪽에 있다.
- 한국 M.AX와 비교할 때 독일은 "모델 대 인력" 구도가 아니라 "데이터 스페이스·표준(B) + 사회보험형 재직자 훈련(C1)" 구도로 읽는 편이 자료에 부합한다(조사자 해석).

### Gaps

- 연방예산 Einzelplan 09(BMWE)·30(BMFTR)의 2026년 타이틀별 금액(Manufacturing-X, Mittelstand-Digital, "Entwicklung digitaler Technologien", KI 관련 타이틀): `bundeshaushalt.de` PDF 503 오류로 미확인.
- KI-Robotikbooster 총액, BMWE 산업 AI 공모(2025-12) 규모, KI-Aktionsplan의 산업 관련 집행액, IPCEI AI의 독일 분담액: 출처를 찾지 못함.
- EU Digital Europe AI Factories 중 독일 소재(JUPITER/JAIF, HammerHAI)의 EU·독일 분담액: 검색에서 확인하지 못함.
- Qualifizierungschancengesetz/Weiterbildungsgesetz의 제조업 참여자 수와 지출, Qualifizierungsgeld 집행액, 2026년 BA 재직자 몫: BA 통계 원문 미확인. `arbeitsagentur.de`의 2026년 예산서 PDF는 404였다.
- INVITE(직업 재교육 디지털 플랫폼 공모), 이원화 직업교육(dual training) 현대화 예산, KI-Trainer 인원: 조사하지 못함.
- Catena-X 1기(2021~2024, 경기부양 패키지 "KoPa 35c")의 공적 지원액: 브로슈어에 금액이 없어 미확인.

---

## 핵심 질문 2. 일본: METI/NEDO 모델·데이터 예산과 MHLW 리스킬링 예산

### Takeaway

"약 3,830~3,870억 엔" 수치는 **2026회계연도 당초예산 3,873억 엔**으로 METI 1차 문서에서 확인되며, 대상은 로봇 전용 모델이 아니라 NEDO를 통한 "국산 멀티모달 파운데이션 모델" 개발 위탁사업(5년 사업의 1년 차 금액)이다. METI는 2027회계연도에 같은 사업 8,964억 엔과 AI 로보틱스 신규 사업 4,542억 엔을 요구했고, 제조 현장 인력에 특정된 AI 교육 예산 항목은 찾지 못했다(인력 예산은 MHLW의 전 산업 대상 제도에 있음).

### Cited Findings

#### 표 2-1. 모델·로봇·데이터 (METI/NEDO)

| 항목 | 금액·회계연도 | 내용(문서 표현) | 분류 | 출처 등급·URL |
|---|---|---|---|---|
| AIロボット・フィジカルAIを見据えたマルチモーダル基盤モデル開発事業 | **FY2026 당초 3,873억 엔(신규)**. GX 추진대책비. 국가 → NEDO(교부금) → 민간기업 등(위탁) | "AI 로봇·피지컬 AI의 개발 기반이 되는 국산 AI 파운데이션 모델을 개발", "멀티모달 기반 모델의 개발을 행한다" | A | [1차-원문] [METI 令和8年度当初予算の概要(2026-04-07)](https://www.meti.go.jp/main/yosan/yosan_fy2026/pdf/01.pdf), [PR資料 GX推進対策費](https://www.meti.go.jp/main/yosan/yosan_fy2026/pr/pdf/pr_gx.pdf) |
| 같은 사업, FY2027 개산요구 | **8,964억 엔(R8 당초 3,873억 엔)**. "令和8年度から5年間の事業" | 언어·이미지·영상·음성과 물리 특성 등 실공간 정보를 통합 처리하는 모델을 개발해 "일본의 모델 개발·활용 사업자에게 학습 완료 모델을 널리 제공" | A | [1차-원문] [METI 令和9年度概算要求等概要(2026-08)](https://www.meti.go.jp/main/yosangaisan/fy2027/pdf/01.pdf), [PR資料 一般会計](https://www.meti.go.jp/main/yosangaisan/fy2027/pr/pdf/pr_ippan.pdf) |
| マルチモーダル基盤モデルの安全性評価検証事業 | FY2027 요구 5.2억 엔(신규), FY2027~2030 | IPA/AISI의 안전성 평가 벤치마크 | A(부수) | [1차-원문] 같은 PR資料 |
| AIロボティクス戦略事業 | FY2027 요구 3,209억 엔(신규). NEDO 기금 조성 | (1) "민간사업자 등의 로봇 파운데이션 모델 개발", 오픈 플랫폼, 핵심 부품(액추에이터·감속기·센서) R&D (2) AI 로봇·부품 **양산 라인 설비투자** 지원 | A/E 혼합 (판단: 문서에 내역 구분 없음. 양산 지원은 E) | [1차-원문] 같은 PR資料 |
| AIロボティクスの中核拠点事業 | FY2027 요구 1,333억 엔(신규). 국가 → 산업기술총합연구소(AIST) | 제조·물류·소매·건설·방재 대상 대규모 목업 시설, 로봇 시험 설비, 시뮬레이션, 계산 자원, 데이터 기반 정비와 "대규모·고품질 데이터 수집" | D/B 혼합 (판단) | [1차-원문] 같은 PR資料 |
| ポスト5G情報通信システム基盤強化研究開発事業 (GENIAC의 모체) | FY2026 당초 6,738억 엔(전년 1,617억 엔) + FY2025 보정 1,537억 엔. FY2027 요구 3,706억 엔 | 반도체·통신·AI 포괄. GENIAC 몫은 예산서에 구분 없음 | 분류 불가 | [1차-원문] [FY2026 概要](https://www.meti.go.jp/main/yosan/yosan_fy2026/pdf/01.pdf), [FY2027 概要](https://www.meti.go.jp/main/yosangaisan/fy2027/pdf/01.pdf) |
| GENIAC: 競争力ある生成AI基盤モデル開発 (공모 2026-01-27 ~ 03-19) | 공모 예산 규모 "100억 엔 정도" | 파운데이션 모델 개발(계산 자원 지원) | A | [1차-원문] [NEDO 공모요령](https://www.nedo.go.jp/content/800046928.pdf) |
| GENIAC: ロボット基盤モデルの研究開発 (공모 2026-02-20 ~ 03-23, 보조) | "200억 엔 정도"(건당 상한 없음). 2026~2029년도 중 최대 3년. 2026-05-14 2개 주제 채택 | METI 영문 보도는 대상을 공도 자율주행차, 드론·무인항공기, 자율운항 선박 등 "공공 인프라"용 기계 제어 모델로 설명. **공장 로봇이 아님** | A (제조 외) | [1차-원문] [NEDO 공모 설명회 자료(2026-02-26)](https://www.nedo.go.jp/content/800050658.pdf), [METI 영문 보도 2026-05-14](https://www.meti.go.jp/english/press/2026/0514_001.html) |
| GENIAC: ロボット基盤モデルの研究開発(補助)【GX】 (설명회 2026-05-25) | "240억 엔 정도", 스테이지 게이트까지 건당 원칙 100억 엔 이하 | 신청서 예시에 "제조업 피킹·팔레타이즈 공정을 대체하는 세미 휴머노이드용 VLA 모델" | A | [1차-원문] [NEDO 설명회 자료](https://www.nedo.go.jp/content/800056040.pdf) |
| ロボティクス分野の生成AI基盤モデルの開発に向けたデータプラットフォームに係る開発 (AIRoA 채택, 2025-08) | **205억 엔(48개월 합계)**, 2025~2029년도(예정) | "데이터 수집, 기반 모델 개발, 실현장 실증". 주제명 "AI 로봇 사회실장용 데이터셋 구축과 기반/개별 모델 개발" | B/A 혼합 (판단: 사업명은 데이터 플랫폼, 내용에 모델 개발 포함. 분리 불가) | [1차-원문] [NEDO 보도 AA5_101877](https://www.nedo.go.jp/news/press/AA5_101877.html) |
| GENIAC: 製造業データ等のAI Ready化に関する研究開発 (공모 2026-01-27 ~ 02-26, 위탁) | **이 주제의 예산액은 공모요령에서 찾지 못함**. 36건 제안 중 9개 주제 채택(2026-05-13). 2026~2027년도 중 1년 | 채택 예: 제조 설계 지식의 AI-Ready화, 생산 기능자 암묵지의 구조 데이터화(FastLabel), 제조 데이터의 산업 데이터 스페이스 대응(히타치) 등 | B | [1차-원문] [NEDO 채택 목록](https://www.nedo.go.jp/content/800054839.pdf), [NEDO 공모요령](https://www.nedo.go.jp/content/800046838.pdf), [METI 영문 보도](https://www.meti.go.jp/english/press/2026/0514_001.html) |
| ウラノス・エコシステムの実現のためのデータ連携システム構築・実証事業 | FY2026 당초 19억 엔(전년 22억 엔). FY2027 요구 28억 엔 | 기업 간 데이터 연계(Ouranos Ecosystem) | B | [1차-원문] [FY2026 概要](https://www.meti.go.jp/main/yosan/yosan_fy2026/pdf/01.pdf), [FY2027 概要](https://www.meti.go.jp/main/yosangaisan/fy2027/pdf/01.pdf) |
| デジタル・ロボットシステム技術基盤構築事業 | FY2026 당초 2.3억 엔(전년 2.3억 엔) | 로봇 소프트웨어 오픈 개발 환경 | E | [1차-원문] [FY2026 概要](https://www.meti.go.jp/main/yosan/yosan_fy2026/pdf/01.pdf) |
| AX(AI·반도체·로봇) 묶음 전체 | FY2027 요구 1조 9,913억 엔(R8 당초 1조 2,557억 엔, R7 보정 2,693억 엔). 이 중 AI·반도체 산업기반 강화 프레임 5,272억 엔 | 반도체 포함 | 분류 불가 | [1차-원문] [FY2027 概要](https://www.meti.go.jp/main/yosangaisan/fy2027/pdf/01.pdf) |

- 주의: NEDO 공모요령에 적힌 "特定公募型研究開発業務勘定 2,684,022百万円"은 포스트 5G 사업 전체의 계정 규모이며 AI-Ready 주제의 예산이 아니다. [1차-원문] — [NEDO 공모요령](https://www.nedo.go.jp/content/800046838.pdf)
- "METI·NEDO가 205억 엔을 투자해 로봇 기반 모델을 구축, 제조·물류에 적용"이라는 보도는 위 AIRoA 사업을 가리킨다. 같은 보도는 이 사업이 "데이터 생태계 구축, 인재 육성을 병행하는 포괄적 대응"이며 기획 단계에서 투자 규모와 기술 불투명성 때문에 찬반 논란이 있었다고 전한다. [2차] — [ニュースイッチ(日刊工業新聞)](https://newswitch.jp/p/46804)
- 5년 총액 "1조 엔" 식의 다년 합계는 이번 조사에서 1차 문서로 확인하지 못했다. FY2026 당초 3,873억 + FY2027 요구 8,964억 = 1조 2,837억 엔(계산. FY2027은 요구액이며 확정 예산이 아님).

#### 표 2-2. 인력·리스킬링 (METI·MHLW·MEXT)

| 항목 | 금액·회계연도 | 대상 | 분류 | 출처 등급·URL |
|---|---|---|---|---|
| 人材開発支援助成金(업계단체 등 훈련 프로그램 개발 지원, 훈련 경비·임금 조성 포함) | FY2026 당초 539억 엔 → FY2027 요구 602억 엔 | 전 산업 사업주·업계단체. 제조업 몫 미구분 | C1 | [1차-원문] [MHLW 人材開発統括官 令和9年度概算要求の概要(2026-08)](https://www.mhlw.go.jp/content/11801000/001759403.pdf) |
| 教育訓練給付金 등 노동자 주체적 능력개발 지원 | FY2026 558억 엔 → FY2027 요구 582억 엔 | 전 산업 개인 | C1 | [1차-원문] 같은 문서 |
| 「17の戦略分野等におけるリ・スキリング人材育成加速化プラン」 공동요구(MHLW·METI·MEXT) | FY2027 요구 합계 **1,909억 엔** | 17개 전략 분야 등. 스킬 표준 → 프로그램 개발 → 제공 | C1+C2 | [1차-원문] 같은 문서 |
| ├ 스킬 표준 책정 지원(METI) | 11.2억 → 13.0억 엔 | 산업 횡단·산업별 스킬 표준 | C1 | [1차-원문] 같은 문서; [METI FY2027 概要](https://www.meti.go.jp/main/yosangaisan/fy2027/pdf/01.pdf)의 "戦略分野等におけるスキル可視化・リスキリング基盤整備事業 13억 엔(R7 보정 11억 엔)"과 일치 |
| ├ 커리어 래더 기업 도입 환경 정비(MHLW) | 0.9억 → 1.2억 엔. "제조·음식 5개 직종" 모델 개발 언급 | 제조 직종 포함 | C1 | [1차-원문] 같은 MHLW 문서 |
| ├ 직업능력검정 창설 지원(MHLW) | 1.6억 엔(신규) | — | C1 | [1차-원문] 같은 문서 |
| ├ 성장 분야 리스킬링 프로그램 개발(MEXT, 대학 등 단기 실천형) | 22억 → 337억 엔 | 대학 등 | C2 | [1차-원문] 같은 문서(MEXT 수치를 MHLW 문서에서 읽음) |
| ├ 대학 전학적 체제 정비 지원(MEXT) | 210억 엔(신규) | 대학 | C2 | [1차-원문] 같은 문서 |
| ├ 산학 연계 사회인 석·박사 육성(MEXT) | 53억 엔(신규) | 대학원 | C2 | [1차-원문] 같은 문서 |
| ├ 전문학교 활용 실천적 직업인재 고도화(MEXT) | 102억 엔(신규) | 전문학교 | C2 (판단: 직업교육이지만 학교 과정) | [1차-원문] 같은 문서 |
| └ 스킬 정보 데이터 연계·일원 제공(MHLW) | 4.5억 → 7.1억 엔 | — | C1 | [1차-원문] 같은 문서 |
| 地域デジタル人材育成・確保推進事業(METI) | FY2026 당초 8.4억 엔(전년 8.6억 엔) | 지역 디지털 인재(제조 특정 아님) | C1 | [1차-원문] [METI FY2026 概要](https://www.meti.go.jp/main/yosan/yosan_fy2026/pdf/01.pdf) |
| 産業構造変化を見据えたスキル可視化・リスキリング基盤整備事業(METI) | FY2025 보정 11억 엔 | 스킬 가시화·강좌 정보 연계 | C1 | [1차-원문] [METI 令和7年度補正予算の概要(2025-12)](https://www.meti.go.jp/main/yosan/yosan_fy2025/hosei/pdf/r7_gaiyo.pdf) |
| 地方の若手人材発掘育成支援事業(AKATSUKI, METI) | FY2025 보정 8.9억 엔 | 지방 청년 디지털 인재 | C2/E (판단) | [1차-원문] [METI FY2026 概要](https://www.meti.go.jp/main/yosan/yosan_fy2026/pdf/01.pdf) |
| MHLW "처우 향상을 위한 리스킬링 지원·생산성 향상" 묶음 | FY2027 요구 951억 엔(전년 862억 엔) | 전 산업 | C1 | [1차-원문] [MHLW 문서](https://www.mhlw.go.jp/content/11801000/001759403.pdf) |

#### 표 2-3. 참고용 비중 시산 (조사자 계산. 공식 수치 아님)

분모가 다른 항목을 섞은 시산이다. 인력 항목은 전 산업 대상이어서 제조 현장 몫은 이보다 작다. FY2027은 요구액이다.

| 시나리오 | 포함 항목(억 엔) | 계산 결과 |
|---|---|---|
| ① FY2026, METI의 AI 특정 항목만 | A 3,873 / B 19(우라노스) / C1 19.4(지역 디지털 인재 8.4 + 스킬 가시화 보정 11). 합계 3,911.4 | A 99.0%, B 0.5%, C 0.5% |
| ② FY2026, MHLW 전 산업 제도 포함 | ①에 人材開発支援助成金 539 + 教育訓練給付 558 추가. 합계 5,008.4 | A 77.3%, B 0.4%, C1 22.3% |
| ③ FY2027 개산요구 | A 8,969.2(멀티모달 8,964 + 안전성 5.2) / A·E 혼합 3,209(AI 로보틱스 전략) / D·B 혼합 1,333(중핵 거점) / B 28 / C 1,909(C1 1,206.9, C2 702). 합계 15,448.2 | A 58.1%, A·E 혼합 20.8%, D·B 혼합 8.6%, B 0.2%, C 12.4%(C1 7.8%, C2 4.5%) |

- 시산에서 제외한 것: 포스트 5G 사업 본체(반도체와 구분 불가), GENIAC 공모 3건(100억·200억·240억 엔, 포스트 5G 기금 재원이라 연도 귀속 불명), AIRoA 205억 엔(2025~2029 다년), AI-Ready 주제(금액 미확인), 폐로 피지컬 AI 470억 엔, 방재 AX 221억 엔(제조 외).

#### 모노즈쿠리 백서 2026 (2026-05-29 공표)

- 개요판 표제: "제조 현장의 데이터를 데이터 기반으로 정비하고, AI를 결합한 사회실장과 데이터 축적이 앞으로의 승리 방정식(勝ち筋)". [1차-원문] — [2026年版ものづくり白書 概要](https://www.meti.go.jp/report/whitepaper/mono/2026/pdf/gaiyo.pdf)
- "AI·디지털 기술 활용에서는 지식·노하우와 인재 확보의 어려움이 과제. 활용 촉진에는 환경 정비가 불가결." [1차-원문] — 같은 문서
- "우리나라 제조 현장의 가공·가동 데이터 등을 수집하고, AI 모델을 실장한 제조 플랫폼 개발을 지원하는 「製造AX拠点」을 정비." [1차-원문] — 같은 문서
- 백서 메시지: "제조 현장의 데이터를 수집·축적해 피지컬 AI 확립 등을 추진하고 제조업 전체의 경쟁력 강화를 촉진한다." [1차-원문] — 같은 문서
- 기업 간 데이터 연계는 "진전이 없고 2년 전과 거의 변화가 없다". 제조 공정 데이터를 취득하는 사업자는 약 70%. [1차-원문] — 같은 문서
- 능력개발(MHLW 집필): 제조업의 OFF-JT 실시율은 사업소 규모가 작을수록 낮고 규모별 격차가 크다. 자기계발 지원 사업소 비율 83.7%. [1차-원문] — 같은 문서, [MHLW 백서 개요](https://www.mhlw.go.jp/content/11801500/001704747.pdf)
- 2040년 제조업 전체 약 400만 명 부족, 그중 AI·로봇 활용 인재 340만 명 부족이라는 METI "2040년 취업구조 추계" 인용. [2차] 검색 요약 — [RIETI BBL](https://www.rieti.go.jp/jp/events/bbl/26062601.html)

### Inferences

- 수치 검증 결과: 의뢰서의 "약 3,830~3,870억 엔"은 3,873억 엔(FY2026 당초)이 맞다. 다만 (i) 사업명과 내용은 "멀티모달 파운데이션 모델"이며 로봇 파운데이션 모델은 GENIAC 공모(200억·240억 엔)와 FY2027 신규 "AI 로보틱스 전략 사업"에 따로 있다. (ii) 3,873억 엔은 5년 사업의 첫해 금액이고 FY2027 요구는 8,964억 엔으로 2.3배다.
- 일본은 조사 대상 중 모델(A) 쪽 쏠림이 가장 뚜렷하다. METI의 AI 특정 항목만 보면 FY2026에 A가 99%다(시산 ①). 전 산업 리스킬링 제도를 모두 더해도 A가 77%다(시산 ②).
- 일본 문서에서 데이터(B)는 수사(백서의 "勝ち筋")에서는 최상위지만, 독립 예산 항목으로는 작다(우라노스 19억 엔, AI-Ready 주제 금액 미상). 데이터 수집은 모델 사업(AIRoA 205억 엔)이나 거점 사업(1,333억 엔 요구) 안에 묻혀 있어 B가 과소 집계될 수 있다.
- 제조 현장 작업자 대상 AI 교육에 특정된 국가 예산 항목은 확인되지 않았다. 인력 예산은 MHLW의 범용 제도(人材開発支援助成金, 教育訓練給付)이며, FY2027 공동요구 1,909억 엔에서 가장 큰 증액은 대학 쪽(MEXT 22억 → 337억 엔, 신규 210억 엔)이다.
- 한국 M.AX와 비교 시 주의: 일본 FY2027 수치는 개산요구(재무성 사정 전)이고, METI는 FY2027부터 보정예산 의존을 줄이고 당초 요구에 넣는다고 밝혔으므로 전년 대비 증가율을 그대로 해석하면 안 된다. [2차] — [MONOist 2026-09-05](https://monoist.itmedia.co.jp/mn/spv/2609/05/news011.html)

### Gaps

- GENIAC "제조업 데이터 등의 AI-Ready화" 주제의 예산액: 공모요령·채택 발표에서 찾지 못함.
- 멀티모달 기반 모델 사업(FRONTia로 보도됨)의 채택 사업자, 5년 총액, 사업 내 데이터·인재 배분: 미확인. "FRONTia" 명칭은 검색 요약(2차)으로만 확인.
- FY2026 보정예산: 2026-11-13 현재 METI 사이트에 해당 페이지가 없다(403/부재). 편성 여부 불확실.
- FY2025 보정의 포스트 5G 1,537억 엔 중 GENIAC·로봇 데이터 몫: PR 자료에서 구분을 찾지 못함.
- 人材開発支援助成金의 제조업 수급 실적·인원, マナビDX 이용 실적, DX 인재 목표(230만 명 등)의 최신 진척: 조사하지 못함.
- 「製造AX拠点」의 예산액: 백서 개요에는 금액이 없다. FY2027 "AI 로보틱스 중핵 거점 사업"(1,333억 엔)과 같은 것인지 불확실.
- 모노즈쿠리 백서 본문(전체판)의 인적 투자 대 기술 투자 서술: 개요판만 읽었다.

---

## 핵심 질문 3. 두 나라 공통: 모델 구축과 사람·데이터를 명시적으로 견준 공식 서술

### Takeaway

두 나라 모두 "모델 대 인력"을 예산 비율로 직접 견준 공식 문장은 찾지 못했다. 일본 문서는 "현장 데이터가 승부처"라고 쓰면서 예산은 국산 모델에 두고, 독일 문서는 모델을 유럽 공동(IPCEI AI)에 맡기고 국내에서는 응용·이전·컴퓨팅을 내세운다.

### Cited Findings

- 일본 METI(FY2027 PR 자료)의 모델 개발 논거: "우리나라에 파운데이션 모델을 공급할 수 있는 주체가 존재하지 않고, 영역 특화 모델 개발의 베이스를 해외 파운데이션 모델에 의존하는 현 상황에서는 … 경제안전보장 등의 관점에서도 큰 리스크." [1차-원문] — [METI FY2027 PR資料](https://www.meti.go.jp/main/yosangaisan/fy2027/pr/pdf/pr_ippan.pdf)
- 같은 자료: 피지컬 AI 실현에는 "우리나라 산업 데이터의 투입이 예상되며, 데이터를 지키면서 장래에도 안심하고 활용할 수 있는 국산 AI 멀티모달 기반 모델의 확립이 필요". [1차-원문] — 같은 문서
- 일본 METI(FY2027 개산요구 개요)의 AX 방침: "고령자 헬스케어, 재해·폐로, 제조업 등의 현장 데이터를 활용하면서 현장 기점의 AI·로봇 실장을 가속하고 반도체까지 일체로 경쟁력 강화". [1차-원문] — [METI FY2027 概要](https://www.meti.go.jp/main/yosangaisan/fy2027/pdf/01.pdf)
- 일본 METI(FY2026 당초예산 개요): 모델·반도체 지원과 "동시에, 생성 AI 시대에 대응한 디지털 인재 강화 시책을 강화"한다고 병기하나, 해당 인재 항목은 8.4억 엔이다. [1차-원문] — [METI FY2026 概要](https://www.meti.go.jp/main/yosan/yosan_fy2026/pdf/01.pdf)
- 일본 METI·NEDO(GENIAC 2026-05): "웹 공개 데이터를 이용한 학습이 진행된 만큼, 앞으로는 기업·조직이 보유한 실데이터의 활용이 한층 중요". [1차-원문] — [METI 영문 보도](https://www.meti.go.jp/english/press/2026/0514_001.html)
- 일본 모노즈쿠리 백서 2026: AI 활용의 과제로 "지식·노하우와 인재 확보"를 지목. [1차-원문] — [백서 개요](https://www.meti.go.jp/report/whitepaper/mono/2026/pdf/gaiyo.pdf)
- 독일 Hightech Agenda(2025, BT-Drs. 21/1100): KI-Offensive 목표는 "2030년까지 경제 성과의 10%를 AI 기반으로 창출". 수단으로 KI-Robotikbooster(재교육 센터 포함), 핵심 업종 이전 선도과제, "중소기업의 생성 AI·AI 에이전트 적응과 주권적 활용을 위한 청사진"을 든다. [1차-원문] — [BT-Drs. 21/1100](https://dserver.bundestag.de/btd/21/011/2101100.pdf)
- 같은 문서: 모델에 대해서는 "계획 중인 IPCEI Künstliche Intelligenz에 참여해 산업용 주권·고특화 AI 모델 개발을 유럽 차원에서 추진". [1차-원문] — 같은 문서
- 같은 문서 목표 2: "AI 역량(알고리즘, 데이터, 컴퓨터, 소프트웨어 도구, AI 칩)의 가용성과 이용 가능성을 측정 가능하게 개선", AI Gigafactory 최소 1곳 유치. [1차-원문] — 같은 문서
- 독일 BMFTR InProKI 공고(2026-03): "성공의 열쇠는 맞춤형 AI 솔루션과 필요한 역량의 구축". [1차-원문] — [BAnz AT 17.03.2026 B1](https://www.zukunft-der-wertschoepfung.de/wp-content/uploads/2026/02/InProKI_BAnz-AT-17.03.2026-B1.pdf)
- 독일 Hightech Agenda AI 로드맵(2026-05) 목표에 "최소 3개의 도메인 특화 …" 모델 관련 지표와 AI 활용 기업 비율 50% 초과 목표가 보인다. PDF 레이아웃이 깨져 문장 전체는 확인하지 못했다(불확실). [1차-원문 일부] — [HTAD Leporello KI](https://hightech-agenda-deutschland.de/fileadmin/Redaktion/Media_Kit/Leporellos/Leporello_Kuenstliche-Intelligenz_HTAD-Roadmaps.pdf)

### Inferences

- 일본은 서술(데이터·인재가 과제)과 예산 배분(국산 모델에 집중)이 어긋난다. 저자가 한국 M.AX의 "모델 대 인력" 논지를 펼 때 일본은 반례가 아니라 같은 방향의 더 극단적 사례가 될 수 있다(조사자 해석. 표 2-3의 시산 한계를 함께 적어야 함).
- 독일은 모델 자체 개발을 국가 단독 과제로 두지 않는 점에서 한국·일본과 다르다. 다만 독일이 "인력에 더 쓴다"는 주장은 이번 자료로는 입증되지 않는다. 독일 인력 지출은 사회보험 재원이고 제조 AI 특정 몫을 알 수 없기 때문이다.

### Gaps

- 일본 「人工知能基本計画」(2025-12 책정, METI 자료상 2026-07-14 개정 각의결정) 본문에서 모델·데이터·인재의 우선순위 서술: 원문을 열람하지 못함.
- 독일 자문기구(EFI 보고서, Plattform Industrie 4.0, Plattform Lernende Systeme)의 모델 대 인력 논의: 조사하지 못함.
- 양국 모두 "모델 예산 대 인력 예산" 비율을 공식적으로 제시하거나 목표로 삼은 문서는 발견하지 못했다. 없다고 단정할 수는 없다(검색 범위 한계).
