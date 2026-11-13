# LLM 개발 비용 검증: 저자 추정(3B 모델 · H200 8장 · 1주 · 1,000회 실험 · 300억 원)의 점검

- 접근일: 모든 URL 2026-11-13 접근. 환율: **1 USD = 1,334.1 KRW, 1 USD = 6.6683 CNY** (ECB 기준환율, 2026-11-12자, [frankfurter API](https://api.frankfurter.dev/v1/latest?base=USD&symbols=KRW,CNY)에서 직접 확인. open.er-api.com 2026-11-13 00:02 UTC 값 1,334.18과 일치).
- 표기: **[1차]** = 원 출처(논문·모델 카드·공시·발표 기관 페이지)를 직접 열어 읽음. **[2차]** = 집계 사이트·언론 기사를 직접 열어 읽음. **[스니펫]** = 검색 결과 요약으로만 확인, 원문 미확인(본문 인용 전 재확인 필요). **[계산]** = 조사자 자체 계산(가정 명시).
- 저자 추정 요약: 3B 파라미터 LLM 사전학습 1회 = H200 8장으로 1주 이상, 1회 2,000만~3,000만 원, 최적 데이터 조합·비율을 찾으려면 최소 1,000회 동시 실행(약 300억 원).

## 1. GPU 가격: 구매가·임차 단가, 그리고 H200 8장 × 1주(1,344 GPU-시간)의 비용

### Takeaway
2026년 11월 초 H200 온디맨드 정가는 GPU-시간당 $3.85~$10.85(11개사 평균 $6.06)이고, 1,344 GPU-시간은 약 690만~1,950만 원이다. 저자의 "1회 2,000만~3,000만 원"은 정확히 1주라면 하이퍼스케일러 정가 상단 이상에 해당하고, 평균 단가로 2주가량 돌리는 경우와 맞는다. 즉 단가는 "다소 높게 잡았지만 범위 안"이다.

### Cited Findings
- H200 온디맨드 단가(2026-11-03 검토, GPU-시간당): Vast.ai $3.85(중앙값), Hyperbolic $3.99, Crusoe $4.29, DigitalOcean $4.47, Modal $4.54, Runpod $5.29, Nebius $5.40, CoreWeave $6.31, AWS p5en $7.91, Oracle $10.00, Azure $10.60(미국 7개 옵션 $10.60~$13.78), Google Cloud $10.85(예약 전용). 11개사 평균은 8월 5일 $5.95 → 11월 3일 $6.06(+1.9%). Runpod는 10월 9일 $4.59→$5.29, Nebius는 9월 29일 $4.50→$5.40으로 인상. **[2차, 직접 읽음]** — [Thunder Compute, NVIDIA H200 Price Comparison (2026-11-04 갱신)](https://www.thundercompute.com/blog/nvidia-h200-pricing). 주의: 경쟁 GPU 클라우드 업체가 만든 집계표이며 각 사 가격 페이지를 개별 확인하지는 못함.
- H200 구매가: 단품 H200 NVL $32,366(리셀러)~$47,500(eBay 신품 최저가, 2026년 10월), 8-GPU HGX 서버 약 $293,000(Newegg 표시가, 품절). NVIDIA는 데이터센터 GPU 정가를 공개하지 않으므로 리셀러·중고 시세임. **[2차]** — [Thunder Compute](https://www.thundercompute.com/blog/nvidia-h200-pricing)
- H100: 임차 $2.99~$15.12/GPU-시간(16개사 중앙값 $4.20), 네오클라우드 평균 $4.09 대 하이퍼스케일러 평균 $10.75, 구매 약 $36,000/장, 8-GPU HGX 서버 $296,000~$309,000 (2026년 11월). H200은 H100보다 평균 13% 비쌈. **[2차]** — [Thunder Compute, H100 pricing](https://www.thundercompute.com/blog/nvidia-h100-pricing)
- B200: 임차 약 $5.99~$16.11/GPU-시간(Google Cloud a4-highgpu-8g 온디맨드 환산 $16.11, 예약·Spot 전용). B300은 B200보다 GPU-시간당 약 $1 높음. **[2차]** — [Thunder Compute, B200 pricing](https://www.thundercompute.com/blog/nvidia-b200-pricing)
- 한국 정부 구매 단가: 「첨단 GPU 확보·구축·운용지원 사업」 2026년 예산 2조 800억 원으로 베라 루빈(Vera Rubin) 2,016장 + B300 7,688장 = 9,704장 확보(네이버클라우드·삼성SDS·엘리스그룹 선정, 2026-06-08 발표). **[2차, 기사 직접 읽음]** — [디지털데일리 2026-06-08](https://www.ddaily.co.kr/page/view/2026060816422801232)
- 2027년 예산안: 차세대 GPU 확보 3조 8,500억 원 = 베라 루빈 서버 대당 275억 원 × 140대. 산·학·연 대여용 GPU(H100, B200 등) 임차 예산은 "장당 350만~700만 원". **[2차, 기사 직접 읽음]** — [머니투데이 2026-11-04](https://www.mt.co.kr/article/2026110416003354291). 주의: 기사에 "장당" 금액의 기간(월/연)이 적혀 있지 않음 → **확인 필요**.
- NIPA 「첨단 GPU 활용 지원 사업」(공고 제2026-0395호, 2026-04-01): H200 신청 단위는 서버 2대(16장)~32대(256장). 대학·연구기관 무상, 중소·스타트업은 시장가의 5~10% 수준이라는 보도. **[스니펫]** — [서울대 컴퓨터공학부 공지(원문 접속 실패)](https://cse.snu.ac.kr/community/notice/25036)

### Inferences
- **[계산]** H200 8장 × 168시간 = 1,344 GPU-시간. 단가별 비용(원화는 1,334.1원/달러):

| 단가($/GPU-h) | 출처 구분 | USD | KRW |
|---|---|---|---|
| 3.85 | Vast.ai 중앙값 | 5,174 | 약 690만 |
| 3.99 | Hyperbolic | 5,363 | 약 715만 |
| 5.29 | Runpod | 7,110 | 약 949만 |
| 6.06 | 11개사 평균 | 8,145 | 약 1,087만 |
| 6.31 | CoreWeave | 8,481 | 약 1,131만 |
| 7.91 | AWS | 10,631 | 약 1,418만 |
| 10.00 | Oracle | 13,440 | 약 1,793만 |
| 10.60 | Azure 최저 | 14,246 | 약 1,901만 |
| 10.85 | Google Cloud | 14,582 | 약 1,945만 |
| 13.78 | Azure 최고 | 18,520 | 약 2,471만 |

- **[계산]** 저자의 2,000만~3,000만 원을 1,344 GPU-시간으로 나누면 $11.15~$16.73/GPU-시간. 이는 조사된 온디맨드 정가의 상단(Azure 고가 리전)과 그 이상이다. "1주 이상"을 2주(2,688 GPU-시간)로 읽으면 평균 단가 $6.06 기준 약 2,170만 원으로 저자 범위에 들어온다.
- **[계산]** 8-GPU H200 서버 구매가 $293,000 ≈ 3억 9,100만 원(전력·상면·인건비 제외). 1주 임차비(평균 단가)의 약 36배.
- **[계산, 가정: "장당 350만~700만 원"이 월 단가이고 월 730시간]** 4,795~9,589원/시간 ≈ $3.59~$7.19/GPU-시간으로 해외 시세와 비슷한 범위. 가정이 틀리면 무효.
- **[계산]** 정부 구매 2조 800억 원 ÷ 9,704장 ≈ 장당 2억 1,400만 원(구축·운용비 포함 사업비 기준, 순수 칩 가격 아님).
- 2026년 하반기 H200·H100 임차 단가는 하락이 아니라 소폭 상승 중이다(위 Thunder 추적치). "GPU 임차료는 계속 싸진다"는 전제는 이 시점 자료로는 뒷받침되지 않는다.

### Gaps
- **국내 사업자(네이버클라우드, NHN클라우드, KT클라우드, 엘리스클라우드)의 H200/H100 시간당 원화 요금을 확인하지 못했다.** ncloud 요금 페이지는 스크립트 렌더링이라 본문 추출 실패, 나머지는 검색으로 공개 요금표를 찾지 못함. 저자 추정을 국내 단가로 검증하려면 각 사 요금표·견적 확인 필요.
- NIPA 지원 사업의 GPU-시간당 자부담 단가(공고문 PDF)는 서버 접속 오류로 읽지 못함.
- 장기 예약(1~3년 약정) 할인 단가는 조사하지 못함. 위 수치는 모두 온디맨드 정가이며 실제 대량 계약가는 더 낮을 수 있음(불확실).
- GB200/베라 루빈의 공식 단가는 공개 자료 없음.

## 2. 처리량: H200 8장 × 1주로 3B 모델을 몇 토큰 학습할 수 있나, 공개된 소형 모델의 토큰 예산과 비교

### Takeaway
공개된 3B 모델 실측 처리량(H100 1장당 약 14,000 토큰/초)을 적용하면 H200 8장 × 1주는 약 680억 토큰으로, 경쟁력 있는 3B급 모델들의 사전학습 예산(3조~36조 토큰)의 0.2~2.3%에 불과하다. 따라서 저자의 "1회"는 **완전한 사전학습이 아니라 공개 사례의 축소 실험(ablation) 1회와 같은 규모**이고, 실제 최종 학습 1회는 그보다 약 90~340배 큰 GPU-시간이 든다.

### Cited Findings
- SmolLM3(3B): 11.2T 토큰, 3단계 학습. 데이터 조합·비율은 "3B 모델을 50B~100B 토큰으로 학습하는 광범위한 ablation"으로 결정. **[1차]** — [Hugging Face blog, SmolLM3 (2025-07)](https://huggingface.co/blog/smollm3) (원문 [raw](https://raw.githubusercontent.com/huggingface/blog/main/smollm3.md))
- SmolLM3 학습 중 기대 처리량 13,500~14,000 토큰/초(H100, GPU당), 1B 기준 모델은 H100 8장 노드에서 45B 토큰에 약 1.5일(GPU당 42k 토큰/초). **[1차]** — [The Smol Training Playbook (Hugging Face, 2025)](https://huggingfacetb-smol-training-playbook.hf.space/)
- SmolLM3 전체 연산 내역(같은 문서 표): 본 학습 384 GPU × 30일 = 276,480 GPU-시간, 사전학습 ablation 192 GPU × 15일 = 69,120, 중간학습(mid-training) ablation 192 × 10일 = 46,080, 재시작·디버깅 46,080, **합계 437,760 GPU-시간**. "ablation과 디버깅이 161,280 GPU-시간으로 본 학습의 절반 이상", "100회 이상의 ablation 수행", 평가 비용 1만 GPU-시간 약간 미만. **[1차]** — [Smol Training Playbook](https://huggingfacetb-smol-training-playbook.hf.space/). (블로그는 본 학습을 "384 H100, 24일"로 적어 문서 간 24일/30일 차이가 있음. Playbook은 30일에 "간헐적 중단 포함"이라고 명시.)
- Llama 3.2 3B: 최대 9T 토큰, 학습 460k H100 GPU-시간(1B는 370k), Llama 3.1 8B·70B의 로짓을 목표로 쓰는 지식 증류(knowledge distillation) 병행(로짓 생성 86k GPU-시간 별도). **[1차]** — [Meta Llama 3.2 Model Card](https://github.com/meta-llama/llama-models/blob/main/models/llama3_2/MODEL_CARD.md)
- Phi-3-mini(3.8B): H100 512장, 10일, 4.9T 토큰(현행 모델 카드). **[1차]** — [microsoft/Phi-3-mini-4k-instruct](https://huggingface.co/microsoft/Phi-3-mini-4k-instruct). Epoch 데이터베이스는 같은 모델을 3.3T 토큰·168시간으로 기록(초기 버전 수치로 보임, 불일치 존재) — [Epoch AI models CSV](https://epoch.ai/data/all_ai_models.csv)
- Phi-4-mini(3.8B): A100 512장, 21일, 5T 토큰. Phi-4(14B): H100 1,920장, 21일, 9.8T 토큰. **[1차]** — [microsoft/Phi-4-mini-instruct](https://huggingface.co/microsoft/Phi-4-mini-instruct), [microsoft/phi-4](https://huggingface.co/microsoft/phi-4)
- Gemma 3: 27B 14T, 12B 12T, 4B 4T, 1B 2T, 270M 6T 토큰. **[1차]** — [Gemma 3 model card](https://ai.google.dev/gemma/docs/core/model_card_3)
- Qwen2.5: 사전학습 데이터 7T → 18T 토큰으로 확대. **[1차, 초록]** — [arXiv 2412.15115](https://arxiv.org/abs/2412.15115). Qwen3-4B 학습 연산 8.64e23 FLOP(Epoch 추정, 신뢰도 Confident; 6×4e9×36T에 해당). **[1차: Epoch DB]** — [Epoch AI models CSV](https://epoch.ai/data/all_ai_models.csv)
- EXAONE 3.5: 2.4B 모델 6.5T 토큰·9.36e22 FLOP, 7.8B 9T·4.21e23, 32B 6.5T·1.25e24. LG는 Qwen 2.5 32B가 EXAONE 3.5 32B의 2.77배 연산을 썼다고 비교. **[1차]** — [EXAONE 3.5 기술보고서, arXiv 2412.04862](https://arxiv.org/html/2412.04862)
- EXAONE 4.0 1.2B: H200 512장 × 336시간(2주), 32B: H200 512장 × 3,192시간. K-EXAONE(236B, 2025-12): B200 512장 × 3,240시간, 11T 토큰. A.X K1(SKT, 519B, 2025-12): H200 1,536장. A.X K2(688B, 2026-07): B200 512장 × 약 70일 ≈ 86만 GPU-시간, 8.5T 토큰, 1.8e24 FLOP(SKT가 Epoch에 이메일로 제공), Epoch 추정 비용 $12.4M(2023 USD). Solar Open 100B(Upstage): 19.7T 토큰·1,572시간. **[1차: Epoch DB 직접 읽음. 각 사 원문은 미확인]** — [Epoch AI models CSV](https://epoch.ai/data/all_ai_models.csv)
- Kanana(카카오): 3T 토큰(1단계 2.7T + 2단계 300B)으로 8B를 처음부터 학습하고, 소형 모델은 가지치기(pruning)·증류와 depth up-scaling으로 파생. "SOTA 모델보다 적은 데이터로 경쟁력 확보"를 표방. **[1차]** — [Kanana 기술보고서, arXiv 2502.18934](https://arxiv.org/html/2502.18934)

### Inferences
- **[계산, 가정: H200의 학습 처리량 = H100(같은 Hopper 세대, 메모리만 큼)과 동일, 3B 모델 14,000 토큰/초/GPU]** 14,000 × 8장 × 604,800초 = **6.77e10 ≈ 677억 토큰**. H200의 큰 메모리로 배치를 키워 10~20% 더 나올 여지는 있으나 출처 없음(불확실).
- **[계산, 검증]** 11.2e12 토큰 ÷ (384장 × 24일 × 86,400초) = 14,066 토큰/초/GPU → Playbook의 13,500~14,000과 일치. 6 × 3e9 × 14,000 = 2.52e14 FLOP/초로 H100 최대치 9.89e14(Epoch 인용값)의 약 25% MFU(Model FLOP Utilization).
- **[계산]** 677억 토큰이 공개 예산에서 차지하는 비율: Qwen3-4B(36T) 0.19%, SmolLM3(11.2T) 0.60%, Llama 3.2 3B(9T) 0.75%, EXAONE 3.5 2.4B(6.5T) 1.04%, Phi-4-mini(5T) 1.35%, Gemma 3 4B(4T) 1.7%, Kanana(3T) 2.3%.
- **[계산]** GPU-시간 배수(저자 1회 = 1,344 GPU-시간 대비): Phi-3-mini 122,880(512×240h) ≈ 91배, EXAONE 4.0 1.2B 172,032 ≈ 128배, SmolLM3 본 학습 276,480 ≈ 206배, Llama 3.2 3B 460,000 ≈ 342배.
- **[계산]** SmolLM3급 본 학습 1회를 2026년 11월 H100 중앙값 $4.20으로 임차하면 276,480 × 4.20 = $1.16M ≈ 15.5억 원, ablation·디버깅 포함 437,760 GPU-시간은 $1.84M ≈ 24.5억 원(온디맨드 정가 가정, 인건비·데이터·저장 제외).
- 저자 추정의 방향성 평가: "3B 모델 사전학습 1회 = H200 8장 1주, 2,000만~3,000만 원"은 **경쟁력 있는 모델의 완전한 사전학습으로는 약 100~300배 과소**하다. 반대로 그 규모(약 680억 토큰)는 SmolLM3 팀이 데이터 비율을 정할 때 쓴 ablation 1회(3B 모델, 50B~100B 토큰)와 거의 같다. **[계산]** 100B 토큰 ablation 1회 = 100e9 ÷ 14,000 ÷ 3,600 ≈ 1,984 GPU-시간으로 저자 단위의 1.5배.
- 한국어 소형 모델(EXAONE, Kanana)은 처음부터 학습하는 대신 큰 모델에서 증류·가지치기하거나 단계별 학습으로 연산을 줄인다. "3B 모델을 처음부터 수천 번"이라는 틀 자체가 공개된 실무와 다르다.

### Gaps
- H200에서 3B급 모델의 학습 처리량 실측 공개치는 찾지 못함(H100 실측을 대입).
- HyperCLOVA X SEED의 학습 토큰·GPU 내역은 공개 자료에서 확인 못함(모델 카드 접근 401, Epoch DB에도 연산량 공란).
- Llama 3.2 3B의 460k GPU-시간에는 증류 관련 추가 연산이 섞여 있어 "순수 사전학습" 비용과 1:1 비교는 부정확.

## 3. 공개된 총비용: 주요 모델의 학습 연산·비용, 최종 학습 대 전체 R&D 실험 연산의 비율

### Takeaway
공개 자료가 있는 세 회사 모두 출시 모델의 최종 학습(final training run)은 R&D 연산 지출의 10~23%에 그치고 나머지 77~90%가 실험·합성 데이터·미출시 모델에 쓰인다. "최종 학습비보다 실험비가 훨씬 크다"는 저자의 직관은 자료로 뒷받침되지만, 그 배수는 공개 사례에서 약 0.6배(SmolLM3)~9배(OpenAI)이지 1,000배가 아니다.

### Cited Findings
- OpenAI 2024년 연산 지출 약 $7B = R&D 약 $5B + 추론 약 $2B. R&D 중 GPT-4.5 최종 학습 약 $400M(90% 신뢰구간 $170M~$890M), 기타 출시 모델 약 $80M, 나머지 약 $4.5B가 그 외 R&D. 투자자 문서·언론 보도 기반 추정. **[1차: Epoch 분석]** — [Epoch AI, Most of OpenAI's 2024 compute went to experiments (2025-10-10)](https://epoch.ai/data-insights/openai-compute-spend)
- 최종 학습이 R&D 연산 지출에서 차지하는 비율: OpenAI 9.6%, MiniMax 22.6%, Z.ai 12.3%. R&D 연산 지출은 OpenAI $5B(2024), MiniMax $141M(2024Q4~2025Q3), Z.ai $216M(2024H2~2025H1) — 후자 둘은 홍콩 IPO 문서 기준. Epoch는 표본이 3개뿐이고 오차 범위가 넓다고 명시. 가정: MFU 0.15~0.35, GPU-시간당 $1.50~$3.00. **[1차: Epoch 분석]** — [Epoch AI, Final training runs account for a minority of R&D compute spending (2026-03-23)](https://epoch.ai/gradient-updates/r-and-d-vs-training-compute)
- 같은 글: 선두를 따라가는 회사는 공개된 아이디어, 선두 모델이 생성한 데이터 등으로 실험을 줄일 수 있어 비율이 높아질 것이라는 가설(catch-up). MiniMax는 부합, Z.ai는 부합하지 않아 결론 유보. 또한 R&D 작업은 대기·실패·디버깅 때문에 GPU 활용률이 낮다고 지적. **[1차]** — [동일 글](https://epoch.ai/gradient-updates/r-and-d-vs-training-compute)
- DeepSeek-V3: "H800 GPU-시간당 $2 가정 시 총 학습비 $5.576M", 그리고 "이 비용은 공식 학습만 포함하며 아키텍처·알고리즘·데이터에 관한 선행 연구와 ablation 실험 비용은 제외". 2.788M H800 GPU-시간, 14.8T 토큰. **[1차]** — [DeepSeek-V3 기술보고서, arXiv 2412.19437](https://arxiv.org/html/2412.19437v1)
- Epoch 데이터베이스의 학습 연산 비용 추정(2023 USD, 최종 학습만): Grok 4 $388M(5e26 FLOP), GPT-4.5 $366M(3.8e26), Grok 3 $218M, Llama 3.1-405B $52.9M, GPT-4 $37.3M, Gemini 1.0 Ultra $30.7M, Claude 3.5 Sonnet $25.9M, A.X K2 $12.4M, A.X K1 $9.6M, DeepSeek-V3 $5.4M. **[1차: Epoch DB]** — [Epoch AI models CSV](https://epoch.ai/data/all_ai_models.csv)
- SmolLM3(3B): 본 학습 276,480 GPU-시간 대 ablation·디버깅 161,280 GPU-시간(본 학습의 58%). **[1차]** — [Smol Training Playbook](https://huggingfacetb-smol-training-playbook.hf.space/)
- Stanford AI Index 2026 1장(R&D): 전 세계 AI 연산 용량이 2022년 이후 연 3.3배 늘어 H100 환산 1,710만 장에 도달. **[1차, PDF 직접 읽음]** — [AI Index 2026 Chapter 1](https://hai.stanford.edu/assets/files/ai_index_report_2026_chapter_1_research_development.pdf)

### Inferences
- **[계산]** 최종 학습 대비 "그 외 R&D 연산" 배수: OpenAI 약 9.4배(90.4/9.6), Z.ai 약 7.1배, MiniMax 약 3.4배, SmolLM3 약 0.58배. 저자의 구도(1회 학습 대 1,000회 실험)는 배수가 1,000이지만, 저자의 "1회"가 실제로는 ablation 단위이므로 직접 비교는 부적절하다. 올바른 비교는 "실험 총량 대 최종 학습"이며 공개 범위는 0.6~9배다.
- 소형 모델·후발 주자일수록 배수가 낮은 경향(SmolLM3 < MiniMax < OpenAI)은 Epoch의 catch-up 가설과 방향이 같지만 표본이 4개 수준이라 일반화할 수 없다(불확실).
- 달러 비율과 FLOP 비율은 다르다. 실험은 활용률이 낮아 같은 돈으로 더 적은 연산을 한다(Epoch 지적). "실험에 돈이 90% 들었다"가 "실험 연산이 90%"를 뜻하지는 않는다.

### Gaps
- AI Index 2026 1장 PDF 본문에서 모델별 학습 비용 추정표를 찾지 못했다(키워드 검색 기준). 2025년판의 GPT-4 $78M, Gemini Ultra $191M 등은 **[스니펫]** 수준이며 2026년판 수록 여부 미확인. Epoch DB 수치($37.3M, $30.7M)와 큰 차이가 나는 것은 추정 방법(클라우드 임차가 대 상각 하드웨어+에너지) 차이로 보이나 확인 필요.
- DeepSeek의 총 하드웨어 투자에 대한 외부 추정(SemiAnalysis 등)은 이번에 원문을 읽지 못했다. "$5.6M은 최종 학습만"이라는 점은 DeepSeek 자체 문서로 확인됨.
- Anthropic, Google, Meta의 실험 대 최종 학습 비율은 공개 자료 없음.

## 4. 실험 실무: 데이터 조합·하이퍼파라미터를 어떻게 정하는가

### Takeaway
공개된 실무는 "전체 규모 학습 1,000회"가 아니라 (1) 목표 모델을 짧게(50B~100B 토큰) 돌리는 ablation 약 100회, (2) 중간 체크포인트에서 이어 학습하는 annealing 실험, (3) 소형 프록시 모델과 스케일링 법칙 외삽(10~32회 실행으로 적합)의 조합이다. 다만 Hugging Face는 자동 조합 탐색 기법이 수작업 ablation을 이기지 못했다고 보고해, 실험 횟수를 이론적으로 크게 줄일 수 있다는 주장에도 한계가 있다.

### Cited Findings
- "ablation의 목표는 소규모로 실험해 최종 학습에 외삽하는 것." 방법은 두 가지: 목표 크기 모델을 적은 토큰으로 학습(SmolLM3: 3B 모델을 11T 대신 100B 토큰), 또는 더 작은 프록시 모델 사용(Kimi K2는 1T 파라미터·활성 32B 모델의 일부 ablation을 3B MoE·활성 0.5B로 수행). **[1차]** — [Smol Training Playbook](https://huggingfacetb-smol-training-playbook.hf.space/)
- 전이 가능성에 대한 경험칙: "소규모에서 성능을 해치는 것은 대규모에서도 배제 가능. 소규모에서 좋은 것은 충분한 토큰으로 학습해야 외삽을 믿을 수 있다." **[1차]** — [동일](https://huggingfacetb-smol-training-playbook.hf.space/)
- 아키텍처 ablation은 1B 모델·45B 토큰(H100 8장 1.5일)으로, **데이터 조합 ablation은 목표 규모(3B)에서** 수행. 이유: "작은 모델과 큰 모델은 용량이 달라 너무 작은 규모의 데이터 ablation은 최적 조합에 대해 잘못된 결론을 낼 위험". **[1차]** — [동일](https://huggingfacetb-smol-training-playbook.hf.space/)
- annealing 실험: 본 학습 중간 체크포인트(예: 7T 토큰 지점)에서 데이터 구성을 바꿔 이어 학습. SmolLM2, Llama 3, OLMo 2에서도 쓰인 방식. **[1차]** — [동일](https://huggingfacetb-smol-training-playbook.hf.space/)
- 자동화 기법 평가: "DoReMi와 RHO-LOSS를 써봤으나 데이터셋 크기의 자연 분포에 가까운 쪽으로 수렴했고 신중한 수작업 ablation을 넘지 못했다. 최근 SOTA 모델은 여전히 체계적 ablation과 annealing을 통한 수작업 조합 조정에 의존." **[1차]** — [동일](https://huggingfacetb-smol-training-playbook.hf.space/)
- 총량: SmolLM3 개발 전체에서 "100회 이상의 ablation", 사전학습 ablation 20일·중간학습 ablation 10일·장애 복구 7일. **[1차]** — [동일](https://huggingfacetb-smol-training-playbook.hf.space/)
- Data Mixing Laws(Ye et al., ICLR 2025): 70M·160M 모델을 30B 토큰씩 학습, 3개 도메인에서 32개 조합(24개로 적합, 8개로 검증). 학습 스텝·모델 크기 스케일링 법칙과 중첩해 소규모 실험만으로 큰 모델의 조합별 손실을 예측. 1B 모델·100B 토큰에서 최적화한 조합이 기본 조합으로 48% 더 학습한 것과 비슷한 성능. 단 같은 논문이 "조합의 순위가 모델 크기와 학습 스텝에 따라 달라진다"고도 명시. **[1차]** — [arXiv 2403.16952](https://arxiv.org/html/2403.16952v2)
- Scaling Laws for Optimal Data Mixtures(Shukor et al., Apple, 2025): 소규모 실행으로 법칙을 적합해 더 큰 모델·새 조합의 손실을 예측. 검증 규모는 LLM 최대 7B 파라미터·150B 토큰. "법칙 적합에 10~20회 실행이면 충분"(도메인 수 k=3~8), 적합 파라미터 수가 도메인 수에 선형 비례하므로 도메인이 많을수록 필요 실행 수가 늘어남. "표준 방식은 시행착오이며 대규모 사전학습에서는 비현실적"이라고 문제 제기. **[1차]** — [arXiv 2507.09404](https://arxiv.org/html/2507.09404v2)
- 증류·합성 데이터: Llama 3.2 1B/3B는 Llama 3.1 8B·70B 로짓을 사전학습 목표로 사용. SmolLM3는 Qwen3-32B가 생성한 합성 선호쌍·추론 데이터 사용. Kanana는 가지치기·증류로 소형 모델 파생. **[1차]** — [Llama 3.2 Model Card](https://github.com/meta-llama/llama-models/blob/main/models/llama3_2/MODEL_CARD.md), [SmolLM3 blog](https://huggingface.co/blog/smollm3), [Kanana 보고서](https://arxiv.org/html/2502.18934)
- Kanana의 한국어 데이터 품질 검증 방식: 새 모델을 처음부터 학습하지 않고 **기존 Llama 3 8B를 25B 토큰만 추가 학습(continual pre-training)** 해 한국어 말뭉치·필터 조합을 비교. **[1차]** — [Kanana 보고서](https://arxiv.org/html/2502.18934)

### Inferences
- **[계산]** 저자의 1,000회 × 1,344 GPU-시간 = 134.4만 GPU-시간. 이는 SmolLM3 프로젝트 전체(437,760)의 3.07배, 그 ablation·디버깅 총량(161,280)의 8.3배다. 동시에 돌리려면 H200 8,000장이 필요한데, 이는 2026년 정부 구매 물량 9,704장의 82%에 해당한다.
- **[계산]** 1,000회 비용을 조사된 정가로 다시 계산하면 134.4만 × $3.85~$10.85 = $5.17M~$14.58M ≈ **69억~195억 원**(평균 단가 $6.06이면 약 109억 원). 저자의 300억 원은 단가를 높게 잡은 결과다.
- 저자 주장별 판정(공개 자료 기준):
  - "실험 1회 규모와 단가": 3B 모델 ablation 1회로서는 현실적(공개 사례의 0.7배 규모), 단가는 높은 편.
  - "최소 1,000회": 공개된 유일한 정량 사례(SmolLM3, 100회 이상)의 약 10배. 논문상 기법(10~32회 적합)과 비교하면 30~100배. **과다 추정으로 볼 근거가 더 많다.** 다만 프런티어 연구소의 실제 실험 횟수는 비공개이고, OpenAI가 R&D 연산의 90%를 최종 학습 외에 쓴다는 점은 "실험이 매우 많다"는 방향과 부합한다. 횟수 자체를 반증하는 프런티어급 자료는 없다(불확실).
  - "그 뒤로 훨씬 더 필요": 방향은 맞음. 가장 큰 비용은 1,000회의 소형 실험이 아니라 **최종 학습(저자 단위의 약 100~340배)과 스케일을 키운 검증 실험**이다. 저자 모형은 실험 횟수는 과대, 최종 학습 규모는 과소 평가했을 가능성이 있다.
- 조합 순위가 규모에 따라 바뀐다는 점(Data Mixing Laws, Playbook 모두 언급)은 "작은 실험을 많이 하면 답이 나온다"는 저자 전제와 "작은 실험 몇 번으로 외삽하면 된다"는 반론 양쪽 모두를 제약한다.

### Gaps
- OpenAI, Google, Anthropic, Meta 등 프런티어 연구소가 데이터 조합 결정에 쓴 실험 횟수는 공개 자료를 찾지 못함.
- 하이퍼파라미터 탐색(학습률·배치 크기 등)에 대한 정량 사례는 SmolLM3 외에 확보하지 못함.
- RegMix, DoReMi 원 논문의 실험 수·비용은 직접 읽지 못함(Playbook의 2차 서술만 확인).

## 5. 데이터 파이프라인 비용: 확보·라이선스·정제·라벨링, 한국어 특수성

### Takeaway
데이터 쪽 지출은 연산비와 별개의 큰 항목이라는 저자 주장은 방향이 맞다. 전문가 라벨링 업체의 연 환산 매출이 수십억 달러대로 보도되고, 한국 정부도 2027년 예산안에 프런티어 AI 학습 데이터 구매비 7,500억 원(2026년 300억 원의 25배)을 넣었다. 다만 이 절의 금액 대부분은 1차 자료로 확인하지 못했다.

### Cited Findings
- 한국 정부 2027년 예산안: 프런티어 AI 학습용 데이터 구매 7,500억 원(2026년 300억 원), 사이버 보안 AI용 학습데이터 500억 원. 과기정통부 AI 관련 사업 총 9조 4,591억 원(전년 대비 +93.3%). **[2차, 기사 직접 읽음. 원자료는 과기정통부 국회 제출 자료]** — [머니투데이 2026-11-04](https://www.mt.co.kr/article/2026110416003354291)
- Mercor: 2026년 상반기 총매출(gross) $614M, 연 환산 총매출이 2025년 말 $760M → 2026년 6월 $2B → 10월 말 $3B(Sacra 추정). 총매출은 계약 전문가에게 지급하는 금액을 포함한 수치. **[2차: Sacra 페이지 직접 읽음, 추정치]** — [Sacra, Mercor](https://sacra.com/c/mercor/)
- Surge AI 연 환산 매출 2025년 말 $1.2B·2026년 초 $1.4B, Turing ARR 약 $300M(2025년 3월), Scale AI 2024년 연 환산 $1B 돌파, Handshake 2026년 초 연 환산 $1B. **[스니펫, 추적 사이트 추정치. 비상장사라 공시 없음]** — [Enterprise DNA AI map](https://enterprisedna.co/resources/ai-map/data), [Dealroom 2026-04-14](https://dealroom.co/news/127345-handshakes-arr-crosses-1b-as-ai-training-revenue-surges/)
- 라이선스 계약: News Corp–OpenAI 5년 $250M, Amazon–NYT 연 $20M~$25M, Wiley 2026 회계연도 AI 라이선스 매출 $49M(누적 $110M 초과). 알려진 계약 약 100건 중 금액 공개는 소수. **[스니펫]** — [LLM Pulse 계약 지도](https://llmpulse.ai/blog/ai-content-licensing-deals/), [CASRAI](https://casrai.org/news/scholarly-publisher-ai-licensing-deals-2026)
- Anthropic은 공개된 라이선스 계약이 없고 저자 집단소송에 $1.5B 합의금을 지급하기로 했다는 서술. **[2차, 뉴스레터 직접 읽음]** — [Media and the Machine, 2026년 6월 업데이트](https://mediaandthemachine.substack.com/p/ai-content-licensing-deals-june-2026)
- 한국어 공개 말뭉치: FineWeb-2의 한국어(kor_Hang) 부분은 60,874,355개 문서, 48,613,120,582 단어, 213.43GB. **[1차: 데이터셋 카드 표]** — [HuggingFaceFW/fineweb-2](https://huggingface.co/datasets/HuggingFaceFW/fineweb-2). (열 이름 해석 — 단어 수/문서 수/UTF-8 크기 — 은 표 머리글 재확인 필요.)
- 카카오는 FineWeb-2를 "최대 규모의 공개 한국어 말뭉치"로 지칭하고, 공개된 고품질 한국어 분류기가 없어 FastText 기반 edu 필터를 자체 반복 학습. 파이프라인은 중복 제거 → 휴리스틱 필터 → 개인정보(PII) 익명화 → 언어별 모델 기반 필터. 또 "한국어 데이터 품질과 무관하게 고품질 영어 데이터가 KMMLU·HAE-RAE 등 한국어 벤치마크 점수를 올린다", "한국어처럼 토큰이 많지 않은 언어는 양보다 질"이라고 보고. **[1차]** — [Kanana 보고서, arXiv 2502.18934](https://arxiv.org/html/2502.18934)
- EXAONE 3.5: 벤치마크 오염 제거(decontamination)를 위해 50자 슬라이딩 윈도 부분 문자열 대조를 전체 학습 데이터에 적용. **[1차]** — [arXiv 2412.04862](https://arxiv.org/html/2412.04862)
- 토크나이저: 저자원 언어·독자 데이터 조합이면 자체 토크나이저 학습이 필요하고, 조합을 정하려면 토크나이저가 필요한 "닭과 달걀" 문제가 있어 본 학습 전에 재학습한다. **[1차]** — [Smol Training Playbook](https://huggingfacetb-smol-training-playbook.hf.space/)
- 국내 뉴스: 네이버는 언론사와 개별 협약(네이버가 AI 기술 제공, 언론사가 학습 이용권 부여) 방식을 취하고, 지상파 3사와는 AI 학습 저작권 소송 중. 다음은 AI 요약 인용량 기반 지급 구상(연 20억 원 예산 예시). **[스니펫]** — [기자협회보](https://journalist.or.kr/news/article.html?no=61771), [MTN 2026-04-09](https://news.mtn.co.kr/news-detail/2026040915330140911)
- 크라우드웍스 2026년 1분기 연결 영업수익 28억 4,934만 원(전년 동기 +50%), 영업손실 21억 6,074만 원(DART 기준이라고 보도). **[스니펫]** — [디지털데일리 2026-05-16](https://www.ddaily.co.kr/page/view/2026051600354775121)

### Inferences
- **[계산]** 한국어 공개 웹 말뭉치 규모: 486억 단어. 한국어 단어당 토큰 수는 토크나이저마다 달라 환산하지 않았지만, 수조 토큰 단위의 영어 말뭉치(SmolLM3 11.2T, Kanana 3T 중 대부분 영어)보다 한두 자릿수 작다. 한국어 모델의 데이터 조합 문제는 "한국어 대 영어 비율" 문제가 되고, 카카오 결과는 영어 품질이 한국어 성능을 좌우한다고 시사한다.
- **[계산]** 규모 대비: 크라우드웍스 분기 매출 약 28억 원(연 환산 약 114억 원 ≈ $8.5M)은 Mercor 연 환산 총매출 $3B의 약 0.3%. 단 Mercor는 총매출(지급액 포함)이라 순매출 기준으로는 격차가 다소 줄어든다.
- 저자의 "데이터 작업이 방대하다"는 정성 주장은 여러 기술보고서의 파이프라인 서술로 뒷받침되지만, **한 프로젝트의 데이터 작업 인건비·기간을 금액으로 밝힌 공개 자료는 찾지 못했다.** 금액으로 주장하려면 근거가 부족하다.

### Gaps
- Reddit–Google(연 약 $60M으로 알려짐) 계약과 Reddit S-1의 데이터 라이선스 총액은 SEC 문서 접근 차단(403)으로 확인 못함.
- AI Hub 데이터셋 수·누적 예산, 셀렉트스타·테스트웍스 매출, 국내 라벨링 시장 규모는 자료를 찾지 못함.
- 작업당 라벨링 단가(전문가 시급 등), 국내 언론사–AI 기업 간 계약 금액은 확인 못함.
- 정제·중복 제거·토큰화 자체의 연산 비용(CPU-시간) 공개 수치는 찾지 못함.

## 6. 규모 비교: 미·중 선두 기업의 연간 투자 대 한국 기업·정부 예산

### Takeaway
미국 4대 기업의 2026년 설비투자 가이던스 합계는 약 $730B, 중국 13개 상장사 AI 인프라 투자는 약 $139B로 추정되고, 한국 과기정통부의 2026년 GPU 확보 사업은 2조 800억 원(약 $1.56B)이다. 저자의 300억 원은 이 규모에서 Amazon 한 회사의 2026년 3분기 설비투자 약 40분어치다.

### Cited Findings
- Microsoft·Alphabet·Amazon·Meta의 2026년 3분기(7~9월) 유형자산 취득 합계 $201.9B(전년 동기 $97.3B, +108%): Amazon $77.3B, Alphabet $51.4B, Microsoft $39.4B, Meta $33.9B. 2026년 1~9월 누계 $496.7B(2025년 연간 $376.1B). 가이던스: Amazon 약 $220B(2026-10-29), Alphabet $195B~$205B, Meta $135B~$145B, Microsoft 2026 역년 약 $170B(금융리스 포함) → 합계 약 $730B. NVIDIA 데이터센터 매출 $89.0B(2026-07-26 종료 분기). **[2차: 10-Q 기반 집계 사이트 직접 읽음, 각 사 공시 원문은 미확인]** — [Walnut AI Capex Tracker (2026-11-08 갱신)](https://walnutinvest.com/stats/ai-capex-statistics)
- 중국: 13개 상장사(하이퍼스케일러·통신사·AI 연구소·데이터센터 운영사) AI 인프라 설비투자가 2026년 9,320억 위안($139B, +103%), 2027년 1.2조 위안($193B) 전망. 미국 데이터센터 투자 추정 약 $800B의 15~20% 수준. Alibaba·Tencent·Baidu 합산 설비투자 2026년 상반기 2,080억 위안, 3사 합산 잉여현금흐름은 2025년 +1,700억 위안 → 2026년 상반기 −160억 위안. ByteDance의 상향된 투자 계획이 올해 최대 증가 요인. **[1차: Rhodium Group 보고서 웹페이지 직접 읽음]** — [Rhodium Group, Examining China's AI Financing (2026-09-10)](https://rhg.com/research/examining-chinas-ai-financing/)
- 중국 프런티어 연구소(Zhipu, MiniMax, DeepSeek, Moonshot)의 PE/VC·IPO·사모 조달: 2025년 90억 위안 → 2026년 1~8월 1,790억 위안. **[1차]** — [동일](https://rhg.com/research/examining-chinas-ai-financing/)
- ByteDance 2026년 투자액은 출처별로 1,600억 위안(Caixin 인용)~2,000억 위안~$70B(Moody's가 Bloomberg 인용)로 엇갈림. **[스니펫, 불확실]** — [Crowdfund Insider 2026-08](https://www.crowdfundinsider.com/2026/08/303278-chinese-tech-giants-ramp-up-ai-spending-but-trail-us-peers-moodys/)
- OpenAI: 2026년 연산 지출 약 $50B(2025년의 3배) 계획이라는 서술. Anthropic: 연산 계약 총액 최대 $517B 보도 등. **[스니펫, 원문 미확인]** — [Epoch AI, Frontier labs don't use most AI compute (yet)](https://epoch.ai/gradient-updates/frontier-labs-dont-use-most-ai-compute), [The Decoder](https://the-decoder.com/anthropic-reportedly-signs-517-billion-in-compute-deals-after-dario-amodei-warned-rivals-about-reckless-risk/)
- 한국 정부: 2026년 GPU 확보 사업 2조 800억 원(9,704장), 2027년 예산안 과기정통부 AI 사업 9조 4,591억 원 중 GPU 확보 3조 8,500억 원. **[2차]** — [디지털데일리 2026-06-08](https://www.ddaily.co.kr/page/view/2026060816422801232), [머니투데이 2026-11-04](https://www.mt.co.kr/article/2026110416003354291)
- 2026년 정부 AI 예산 10.1조 원(2025년 8월 예산안 기준, 과기정통부 몫 5.1조 원). **[스니펫]** — [헤럴드경제 2025-08-28](https://www.heraldk.com/article/2025082818341706955)
- 네이버: 2025년 GPU 포함 인프라 투자 약 1조 원, 2026년 이후 GPU에만 1조 원 이상 필요하다는 CFO 발언(2025년 3분기 실적 발표). **[스니펫]** — [디지털데일리 2025-11-05](https://www.ddaily.co.kr/page/view/2025110511015654112)
- 국내 프런티어급 학습 사례: A.X K2는 B200 512장 × 70일, K-EXAONE은 B200 512장 × 135일(3,240시간). **[1차: Epoch DB]** — [Epoch AI models CSV](https://epoch.ai/data/all_ai_models.csv)

### Inferences
- **[계산]** 원화 환산(1,334.1원/달러): 미국 4사 가이던스 $730B ≈ 974조 원. 중국 $139B ≈ 185조 원. 한국 2026년 GPU 사업 2.08조 원 ≈ $1.56B → 미국 4사의 약 0.21%, 중국 추정치의 약 1.1%. 2027년 GPU 예산 3.85조 원 ≈ $2.89B.
- **[계산]** 저자의 300억 원 ≈ $22.5M. Amazon 2026년 3분기 설비투자 $77.3B ÷ 92일 ÷ 24시간 ≈ 시간당 $35M → 300억 원은 약 39분어치. 한국 2026년 GPU 사업 예산의 약 1.4%.
- **[계산]** 저자의 1,000회 동시 실행에 필요한 H200 8,000장은 국내 최대급 단일 학습 사례(512장)의 약 16배 물량이다. 국내에서 "실험용으로만 8,000장을 1주 동시 확보"는 2026년 정부 구매분 전체에 가까운 규모라 현실적으로 순차 실행이 될 것이다(추론).
- 설비투자(capex)는 데이터센터·토지·전력까지 포함하고 추론용 비중이 크므로 "학습에 쓰는 돈"과 같지 않다. 규모 비교에는 쓸 수 있으나 학습 예산 비교로 직접 쓰면 과장이 된다.
- 한국에 유리한 사실도 있다: 정부 예산이 2026년 → 2027년 안에서 GPU 확보 2.08조 → 3.85조 원, 데이터 구매 300억 → 7,500억 원으로 급증했고, SKT·LG·Upstage가 500~700B급 모델을 512~1,656장으로 학습해 공개했다. 격차는 크지만 정체 상태는 아니다.

### Gaps
- 각 사 10-Q·실적 발표 원문으로 가이던스 수치를 교차 확인하지 못했다(Walnut 집계에 의존). Microsoft 가이던스는 검색 결과에서 $170B와 $190B가 엇갈림.
- 네이버·카카오·SKT·LG의 2026년 설비투자 실적치(IR 자료)는 확인 못함.
- OpenAI·Anthropic·xAI의 2026년 연산 지출은 원문 미확인. 학습 대 추론 분할도 불확실.
- ByteDance 수치는 출처 간 2배 이상 차이.
