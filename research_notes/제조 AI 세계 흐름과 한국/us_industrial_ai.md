# US Industrial / Manufacturing AI: Product Architecture, Field Deployment, and the FDE Trend (as of Nov 2026)

Research note on method and reliability: findings below come from web search result summaries retrieved 2026-11-13. Two primary pages I tried to open directly (fortune.com, a16z.com) were unreachable from this session's network, so those items rest on search-result excerpts, not on a full read of the page. Items labelled "secondary" or "unverified" should be re-checked before being quoted in a final report. Hypothesis under test (H): "field data people and purpose-built models matter more than reusing/fine-tuning models from other industries."

## 1. How do US industrial AI players structure their products (generic vs per-site models, data ingestion and labeling)?

### Takeaway
The dominant US pattern in 2026 is a hybrid: a reusable platform or pretrained layer (ontology, fleet-trained machine models, LLMs, first-principles models, simulation) combined with site-specific data integration done by embedded or vendor-side engineers. Nobody in the evidence found sells a purely generic model that works without site data work, and nobody found builds everything from scratch per site.

### Cited Findings

Palantir (Foundry / AIP / Warp Speed)
- Palantir describes Warp Speed as a "manufacturing operating system" powering workflows such as dynamic material resource planning and reducing material and labor variances; inaugural cohort announced December 2024 (older, 2024) — [Business Wire, 2024-12-11](https://www.businesswire.com/news/home/20241211204864/en/Palantirs-Inaugural-Warp-Speed-Cohort-to-Power-Manufacturing-and-Production-Capabilities-Through-Advanced-AI-Technology)
- "Warp Speed for Warships" (with BlueForge Alliance) launched July 2025 to connect shipbuilders, suppliers and Navy partners on one platform (2025) — [Business Wire, 2025-07-02](https://businesswire.com/news/home/20250702113396/en/BlueForge-Alliance-and-Palantir-Launch-Warp-Speed-for-Warships-to-Digitally-Transform-the-U.S.-Maritime-Industrial-Base)
- Customer Ursa Major says the Palantir-built system uses the Ontology and AIP to link engineering decisions, shop-floor execution and supply chain data, and projects 10,000 to 15,000 engineering hours saved per year (customer projection, not a measured result) — [Ursa Major blog](https://ursamajor.com/media/blog/how-ursa-major-and-palantir-are-solving-manufacturing-challenges-at-hypersonic-speeds/)
- Palantir's own job posting for "Forward Deployed Software Engineer - Warp Speed" describes embedded engineers working with customers "from the factory floor to the board room"; listed salary range $135,000 to $200,000, US person status, up to 25% travel (posting date not confirmed) — [Palantir Lever posting](https://jobs.lever.co/palantir/2da5e0f5-8d8d-45f4-bb56-6889c568ad00/)
- Palantir Q3 2026 (quarter ended 2026-09-30): US commercial revenue $984 million, up 148% year over year and 29% quarter over quarter; US commercial customers 686 (+29% YoY); US commercial remaining deal value $6.517 billion (+79% YoY) — [Palantir 8-K press release, Q3 2026](https://www.sec.gov/Archives/edgar/data/0001321655/000132165526000045/a2026q3ex991pressrelease.htm)
- Same quarter: total revenue about $2.31 billion (+96% YoY), full-year guidance raised to about $8.53 billion; US commercial ($984M) passed US government ($953M) for the first time (secondary summaries of the release) — [Futurum](https://futurumgroup.com/?p=97554); [AI Weekly](https://aiweekly.co/alerts/palantir-q3-revenue-nearly-doubles-to-231b-guides-to-853b)
- Contradicting signal: analysts note US commercial customer-count growth slowed to 5% sequentially (6% in Q2) and quarterly TCV growth in that business was 11% (secondary) — [Runtimewire](https://runtimewire.com/article/palantir-raises-u-s-commercial-guidance-to-143-as-enterprise-ai-demand-fuels-rev)

C3 AI (generic enterprise AI application platform)
- Fiscal Q4 2026 (ended 2026-04-30): total revenue $51.6 million, down 52.5% YoY; professional services revenue $3.2 million, down 85% YoY; nine initial production deployments (IPDs) signed; FY2027 revenue guidance $210 to $240 million with non-GAAP operating loss $128 to $160 million (secondary, Zacks-syndicated) — [Chartmill / Zacks](https://www.chartmill.com/news/external/33625/c3-ai-tops-q4-earnings-revenue-estimates-on-restructuring-push)
- Fiscal Q3 2026 (ended 2026-01-31): 14 IPDs signed (five generative AI); cumulative 408 IPDs, 258 still active; professional services $5.1 million, down 61.1% YoY (secondary) — [Zacks](https://www.zacks.com/stock/news/2881597/c3ais-q3-revenues-decline-can-restructuring-aid-the-stocks-growth)
- FY2026 revenue expected $246.7 to $250.7 million versus $389.1 million in FY2025; cash $66.2 million at FY2026 end versus $164.4 million a year earlier; restructuring with 26% headcount reduction (secondary) — [SiliconANGLE, 2026-02-25](https://siliconangle.com/2026/02/25/c3-ai-shares-plunge-earnings-miss-shrinking-sales-weak-outlook-rattle-investors/); [Chartmill / Zacks](https://www.chartmill.com/news/external/33625/c3-ai-tops-q4-earnings-revenue-estimates-on-restructuring-push)

Emerson / AspenTech
- Emerson introduced its AVA industrial AI platform on 2026-05-11. Per the company, AVA embeds Emerson expertise and first-principles models into operational skills and workflows while using large language models; it is data-source agnostic and uses the AspenTech Inmation Data Platform to organize OT data across cloud, edge and on-premise — [Emerson press release, 2026](https://www.emerson.com/en/corporate/news/2026/new-emerson-industrial-ai-platform-delivers-enterprise-scale-ai)

Honeywell
- Honeywell Forge connected more than 324,000 customer sites (as of March 2026) and added Forge Cognition, an agentic AI and digital twin platform (October 2026). Honeywell is described as fine-tuning selected open-source models and building industrial agents on Google Gemini (agreement October 2024) alongside its own deterministic and physics-based models (secondary profile, verify) — [imagine.ai Honeywell profile](https://imagine.ai/research/honeywell)

Rockwell Automation
- Rockwell is described as most visible in production systems, PLC-based automation and plant-floor analytics, and has collaborated with NVIDIA on Omniverse-based industrial applications (secondary; thin evidence) — [Rankereports 2026 ranking](https://rankereports.com/best-industrial-ai-companies-worldwide-2026-ranking-of-the-leaders-moving-ai-into-real-operations/); [Advisor Perspectives / Bloomberg, 2025-06-24](https://www.advisorperspectives.com/articles/2025/06/24/siemens-battling-big-tech-ai-supremacy-factories)

NVIDIA (Omniverse, Mega, industrial partnerships)
- NVIDIA expanded the Mega Omniverse blueprint (multi-robot fleet testing) with libraries for factory-scale digital twins; Siemens was first to build digital twin software supporting it; FANUC and Foxconn Fii among first to connect robot models (announced 2025) — [NVIDIA investor release, 2025](https://investor.nvidia.com/news/press-release-details/2025/NVIDIA-Omniverse-Physical-AI-Operating-System-Expands-to-More-Industries-and-Partners/default.aspx)
- Foxconn uses the Siemens digital twin stack on Omniverse to validate its Houston facility virtually, then Mega and Isaac Sim to design, simulate, train and validate robot fleets — [NVIDIA case study](https://www.nvidia.com/en-us/case-studies/foxconn-develops-physical-ai-enabled-smart-factories-with-digital-twins/)
- NVIDIA and US manufacturing and robotics companies announced physical-AI "reindustrialization" partnerships (2025) — [NVIDIA investor release, 2025](https://investor.nvidia.com/news/press-release-details/2025/NVIDIA-and-US-Manufacturing-and-Robotics-Leaders-Drive-Americas-Reindustrialization-With-Physical-AI/default.aspx)
- Siemens and NVIDIA (January 2026) plan an "Industrial AI Operating System" and AI-driven adaptive manufacturing sites, starting in 2026 with the Siemens electronics factory in Erlangen, Germany as blueprint (non-US reference; announcement, not results) — [AI Business](https://aibusiness.com/generative-ai/siemens-nvidia-industrial-ai-reduce-engineering-effort)
- Siemens' Industrial Foundation Model (announced 2025, with Microsoft) is described as a GPT-like generative model fine-tuned for industry, built on 150 petabytes of product data and patents (non-US, comparison point) — [Automation World](https://www.automationworld.com/factory/digital-transformation/article/55296419/siemens-digital-industries-software-siemens-bets-big-on-industrial-ais-future-with-altair-acquisition-and-industrial-foundation-model)

Startups
- Augury: company blog says its algorithms can be trained on over 450 million machine hours across more than 100 machine types and dozens of industries, and that it uses an LLM to process customer repair and feedback data to retrain Machine Health models continuously (blog date not confirmed; may be dated) — [Augury blog](https://www.augury.com/blog/machine-health/big-news-at-scale-augury-achieves-continuous-learning-for-its-machine-health-ai/)
- Augury (May 2026) announced an "Industrial AI Workforce" of role-based agents on top of Machine Health, with Google Cloud and AVEVA, centered on an "Industrial Context Graph" linking machine health signals with operational, process and environmental data — [Manufacturing Dive press release, 2026-05-18](https://www.manufacturingdive.com/press-release/20260518-augury-shaping-the-future-of-production-with-the-industrial-ai-workforce-2/)
- Augury raised $75 million while maintaining a $1 billion valuation, and launched Machine Health Ultra Low for low-RPM machinery (hundreds of additional asset types) — [Augury press release](https://www.augury.com/media-center/press/augury-announces-75-million-of-funding-and-maintains-1b-valuation/); [Augury press release, Ultra Low](https://www.augury.com/media-center/press/machine-health-category-leader-augury-releases-first-ai-powered-predictive-maintenance-solution-for-ultra-low-rpm-machinery/)
- Augury requires its own sensors, and certified reliability engineers review alerts before they reach maintenance teams (secondary roundup) — [Techsy 2026 roundup](https://techsy.io/en/blog/ai-tools-for-manufacturing)
- Landing AI: LandingLens is positioned as a low-code platform to label, train and deploy custom vision models, with a data-centric approach for small datasets, scaling "from a single production line to worldwide operations" — [Landing AI, LandingLens page](https://landing.ai/landinglens)
- Landing AI's homepage emphasis has shifted since 2024 toward Agentic Document Extraction for financial services and insurance (secondary interpretation, not a company statement) — [KI-Syndikat review](https://www.ki-syndikat.de/tools/landing-ai/)
- Instrumental: AI inspection and root-cause platform purpose-built for electronics manufacturing; over $80 million raised (secondary roundup) — [Viewpoint Analysis 2026](https://www.viewpointanalysis.com/post/manufacturing-ai-software-options-2026)
- Uptake: Bosch announced on 2026-03-19 plans to acquire Uptake Technologies (Chicago), described as specializing in AI predictive analytics for commercial fleets; terms undisclosed — [Bosch Media Service US](https://us.bosch-press.com/pressportal/us/en/press-release-30080.html)
- Skild AI: with NVIDIA and Foxconn, began using the Skild Brain foundation model on dual-arm robots assembling hardware at an NVIDIA factory in Houston; claims a $100 million annual revenue run rate and learning unseen multistep tasks from one video demonstration (company claims via press, 2026) — [AI Business](https://aibusiness.com/robotics/nvidia-backed-skild-ai-teaches-robots-tasks-from-video)
- Stanford/NVIDIA paper (July 2026) on ROSA, a robotics foundation model serving system for "robot factories", states such models are making general-purpose robots increasingly practical for factory deployment — [NVIDIA Research](https://research.nvidia.com/publication/2026-07_rosa-robotics-foundation-model-serving-system-robot-factories.md)

### Inferences
- Supporting H: the fastest-growing US player (Palantir, US commercial +148% YoY in Q3 2026) sells a reusable platform but delivers it through embedded engineers who model each customer's data into a site-specific ontology; the value is in customer-specific data integration, not in a cross-industry pretrained model. C3 AI, which sells more packaged generic applications, shrank sharply in FY2026. This is correlation only; C3's decline also has company-specific causes (leadership change, restructuring) not examined here.
- Supporting H: process-industry incumbents (Emerson/AspenTech, Honeywell) explicitly keep first-principles and physics-based models and site OT data at the core and use LLMs as an interface or reasoning layer, not as the predictive model.
- Contradicting H: Augury's approach is the opposite of per-site modelling: one model family trained across 450M+ machine hours and 100+ machine types, reused at every new site. Rotating equipment is similar across plants, so pooled pretraining works. Skild AI and NVIDIA's Omniverse/Mega stack likewise bet on general robot foundation models plus simulation to reduce on-site data collection.
- Synthesis: reuse works where the physical asset is standard across sites (pumps, motors, robots, common defect types); purpose-built work dominates where the process, product or data schema is unique to the plant (ERP/MES integration, process control, scheduling). The US market is moving toward both at once: pretrained layer plus heavy site-specific integration.
- Even "generic model" vendors retain field or expert labor: Augury keeps human reliability engineers in the loop and its own sensors, which is a form of vendor-controlled data collection.

### Gaps
- GE Vernova: no usable source found on its 2026 industrial AI software (GridOS, APM) architecture.
- Rockwell Automation: no primary source found on FactoryTalk AI products, model training approach or its NVIDIA integration details.
- Microsoft and AWS industrial offerings (Fabric for manufacturing, factory operations agents, AWS IoT SiteWise and similar): search returned nothing citable.
- Physical Intelligence: only a funding figure surfaced ($600 million at $5.6 billion valuation, secondary, unverified); no factory deployment or data-collection detail. Figure's BMW Spartanburg claim (95%+ success over 10,000+ trials) came only from an aggregator and is unverified.
- How site data is labeled (who labels, tooling, cost per site) is not documented in any source found, beyond Landing AI's label-train-deploy description and Augury's use of repair feedback.
- Palantir bootcamp counts, manufacturing-specific customer counts and FDE headcount for 2026 not found; the 10-Q/10-K text was not opened.
- Share of Palantir or C3 revenue from manufacturing specifically: not found.

## 2. FDE trend: hiring data, adopters, growth figures, criticisms

### Takeaway
FDE job postings grew by roughly an order of magnitude from 2025 to 2026 according to several labor-data vendors, and OpenAI, Anthropic and AWS moved from small in-house teams to large deployment organizations and partner training programs. The main criticisms are services-level margins, poor scalability, and loose use of the title.

### Cited Findings
- Lightcast data cited by Fortune: "forward-deployed" engineer postings rose more than 1,000% between January and August 2026 versus the same period in 2025, and more than 4,600% versus 2023; broader tech postings grew 13% YoY (page not opened directly; from search excerpt) — [Fortune, 2026-09-03](https://fortune.com/2026/09/03/forward-deployed-engineers-fast-growing-six-figure-silicon-valley-job-integrate-ai-with-customers-tech-careers-palantir/)
- Indeed data via Business Insider: FDE postings grew 729% between April 2025 and April 2026 (secondary relay) — [Paraform, April 2026](https://www.paraform.com/insights/forward-deployed-engineer-demand-quadrupled)
- LinkUp: listings rose more than 15x, from about 300 to over 5,000 (period not confirmed in excerpt) — [LinkUp](https://www.linkup.com/insights/blog/inside-the-ai-revolution-linkup-job-data-shows-steady-hiring)
- The three sources disagree on the growth rate (729%, 1,000%+, 15x) because baselines and title definitions differ; postings use the label loosely, so title counts may overstate the role — [Fortune, 2026-09-03](https://fortune.com/2026/09/03/forward-deployed-engineers-fast-growing-six-figure-silicon-valley-job-integrate-ai-with-customers-tech-careers-palantir/)
- OpenAI set up its FDE team in early 2024 and aimed for about 50 engineers in 2025; Anthropic said it would grow its applied AI team fivefold in 2025 (FT reporting relayed; 2025 figures, now dated) — [eWeek](https://www.eweek.com/news/openai-anthropic-cohere-ai-hiring/)
- OpenAI launched a separate "OpenAI Deployment Company" and agreed to acquire Tomoro, bringing about 150 FDEs and deployment specialists from day one (2026; exact date not captured) — [OpenAI](https://openai.com/index/openai-launches-the-deployment-company/)
- Anthropic is putting $100 million into a program to train 10,000 forward-deployed engineers by end of 2027, aimed at engineers working for customers and partners rather than internal staff; AWS is in the same race — [CNBC, 2026-10-15](https://www.cnbc.com/2026/10/15/aws-anthropic-racing-to-deploy-army-of-specialized-ai-engineers.html)
- Unverified claim: four AI companies committed about $9 billion combined to FDE functions, including OpenAI $4 billion and Anthropic about $1.5 billion; could not be corroborated — [Paraform, April 2026](https://www.paraform.com/insights/forward-deployed-engineer-demand-quadrupled)
- The FDE model is spreading into healthcare (2026) — [Forbes, 2026-09-02](https://www.forbes.com/sites/spencerdorn/2026/09/02/why-forward-deployed-engineers-are-spreading-into-healthcare/)
- a16z argues services-led growth "trades margin for moat": customization lowers gross margin and raises burn early; it acknowledges the objections that services limit scalability and should be left to partners (page not opened directly; from search excerpt) — [a16z, "Trading Margin for Moat"](https://a16z.com/services-led-growth/)
- Criticism: traditional services run 30 to 40% gross margin versus 70 to 80%+ for software; Bob McGrew (ex-Palantir) is quoted: "The FDE model is doing things that don't scale at scale" (secondary) — [N47, "The FDE dilemma"](https://www.n47.com/insights/the-forward-deployed-engineer-dilemma)
- Counterpoint: Palantir keeps 80%+ gross margins despite field deployment; individual deployments can have poor margins because the work is effectively R&D feeding the platform, not COGS (blog, opinion) — [Barry's blog](https://www.barry.ooo/posts/fde-culture)
- Criticism from the buyer side: a CIO.com piece titled "Stop sending me engineers: what OpenAI, Anthropic and Microsoft misread about enterprise AI" (2026; content not read, title only) — [CIO.com](https://www.cio.com/article/4233864/stop-sending-me-engineers-what-openai-anthropic-and-microsoft-misread-about-enterprise-ai.html)
- Criticism: most of what companies call FDE is relabeled solutions engineering or consulting (self-published opinion) — [Medium](https://medium.com/@jision/forward-deployed-engineering-is-real-most-of-what-companies-are-building-is-not-d6a87e852a7c)

### Inferences
- The FDE boom is mostly a general enterprise-AI phenomenon (LLM labs, SaaS), not manufacturing-specific. In manufacturing the clearest instance is Palantir Warp Speed's dedicated FDSE role.
- The shift from in-house teams (OpenAI about 50 in 2025) to a separate deployment company and partner-training programs (Anthropic's 10,000 target) suggests the labs themselves concluded in-house FDEs do not scale and are pushing the embedded work out to partners. This supports "field people matter" while also confirming the scalability critique.
- Supports H in part: the party with the best models still needs people on the customer's premises to get value; the binding constraint is context and data access, not model quality.

### Gaps
- No verified current FDE headcount for OpenAI, Anthropic or Palantir as of late 2026.
- No data on what share of FDE postings are in manufacturing or industrial firms.
- Fortune and a16z pages could not be opened (hosts not reachable from this session); details beyond the excerpts are unconfirmed. Publication date of the a16z piece not confirmed.
- No McKinsey, BCG or Deloitte report on FDE surfaced.

## 3. Documented failures or retreats of the "generic platform" approach

### Takeaway
GE Predix is the best-documented failure, and the commonly stated cause is that a do-all horizontal platform still required expensive per-customer customization while lacking packaged applications. IBM shut its Watson IoT Platform in December 2023 without stating a reason. Current survey evidence points to site data infrastructure, not model quality, as the reason pilots stall.

### Cited Findings
- Predix was marketed as a broad edge-to-cloud platform but in practice was a generic platform needing a lot of expensive customization and developer time per customer; packaged applications solving concrete problems came late (analyst commentary, older) — [Medium, World of IoT](https://medium.com/world-of-iot/73-lessons-to-learn-from-the-failure-of-ges-iot-platform-predix-3b3d20eccd42)
- Lesson drawn: "industrial IoT doesn't scale horizontally" and a platform provider cannot compete at every layer (older, circa 2018) — [Stacey on IoT](https://staceyoniot.com/?p=1429)
- GE's decision to build its own Predix cloud data centers put it in competition with Amazon, Microsoft and Google (commentary, older) — [Medium, World of IoT](https://medium.com/world-of-iot/73-lessons-to-learn-from-the-failure-of-ges-iot-platform-predix-3b3d20eccd42)
- Predix messaging got mired in technical features rather than outcomes; GE sought a new owner for the unit (older) — [TBR](https://tbri.com/?p=3596)
- Organizational causes: platform treated as a siloed entity; conflict between platform practices and GE's Lean manufacturing culture. Headline cost figures vary by source: "$7 billion" in one title, "$4 billion" in another (both secondary, unverified) — [platformengineering.org](https://platformengineering.org/blog/how-general-electric-burned-7-billion-on-their-platform); [Panorama Consulting](https://panorama-consulting.com/ge-digital-transformation-failure)
- IBM retired the Watson IoT Platform on IBM Cloud effective 2023-12-01 with no direct replacement and gave no reason when asked; Google shut IoT Core around the same time — [The Register forum thread on the 2022-11-15 article](https://forums.theregister.com/forum/all/2022/11/15/ibm_set_to_retire_watson/); [We Speak IoT](https://www.wespeakiot.com/watsoniot/)
- Uptake (once a horizontal industrial AI platform) cut headcount by nearly half over two years (circa 2019, old) and by 2026 was described as a fleet predictive-maintenance specialist acquired by Bosch — [Crain's Chicago Business](https://www.chicagobusiness.com/john-pletz-technology/uptake-cuts-more-jobs-headcount-down-about-half-peak); [Bosch Media Service US, 2026-03-19](https://us.bosch-press.com/pressportal/us/en/press-release-30080.html)
- C3 AI revenue fell from $389.1 million (FY2025) to about $247 to $251 million (FY2026) (secondary) — [SiliconANGLE, 2026-02-25](https://siliconangle.com/2026/02/25/c3-ai-shares-plunge-earnings-miss-shrinking-sales-weak-outlook-rattle-investors/)
- Kaufman Rossin survey (2026, US mid-market): 73% of manufacturers stuck in AI pilot phase; only 27% have a data warehouse or data lake versus 60% across the broader mid-market; legacy integration is the top barrier for 55% (41% average) — [MarketScale](https://www.marketscale.com/industries/industrial-iot/most-mid-market-manufacturers-are-stuck-in-ai-pilot-mode-and-their-data-infrastructure-is-why)
- Parsec Automation survey (2026, 1,200 leaders, vendor-sponsored): 72% adopted AI in some form, 10% deployed at scale — [Let's Data Science](https://letsdatascience.com/news/parsec-survey-finds-a-wide-gap-between-manufacturing-ai-pilo-12112f67)
- Augury State of Production Health 2026 (501 leaders, vendor survey): poor data quality is now the top roadblock to AI adoption, up 20 points from the prior year; 42% say over half of pilots reach scale across sites versus 14% in 2025 — [Augury](https://www.augury.com/collateral/the-state-of-production-health-2026/)
- TCS and Google Cloud (August 2026): 9% of manufacturers have scaled AI pilots into full operational deployment (secondary) — [Manufacturing Digital](https://manufacturingdigital.com/news/the-industrial-ai-barriers-manufacturers-are-facing)

### Inferences
- Supports H: the stated Predix lesson is precisely that a generic horizontal layer does not remove per-site work; the vendors that survived narrowed to a vertical (Uptake to fleets) or kept domain models (AspenTech, Honeywell).
- Supports H: 2026 surveys name data infrastructure, data quality and legacy integration as the blockers, which are site-level problems that pretrained models from other industries do not solve.
- Contradicts or qualifies H: Augury's own survey shows the share of firms scaling most pilots tripled in one year (14% to 42%), which suggests packaged, pretrained products are getting easier to roll out across sites. The survey is vendor-run, so treat with caution.
- The Predix failure was also about cloud strategy and organization, so it is not clean evidence about model reuse versus purpose-built models.

### Gaps
- No primary GE statement of causes found; all Predix causes are third-party interpretation, mostly from 2018 to 2020 era commentary.
- IBM gave no reason for the Watson IoT shutdown; any causal claim would be speculation.
- The widely repeated "95% of corporate AI projects fail to deliver ROI" (attributed to MIT) and "87% of industrial AI pilots never reach deployment" could not be traced to a primary source in this search; do not cite without verification.
- No McKinsey or Deloitte 2026 manufacturing scale figure found. A McKinsey 2025 global survey figure (91% of respondents not using AI agents in manufacturing) appeared only second-hand.

## 4. US government programs touching manufacturing AI and workforce

### Takeaway
Federal action in 2025 to 2026 is modest in dollars and centered on NIST: an AI-focused Manufacturing USA institute (up to $70 million over five years) and a $20 million MITRE-run pair of AI centers, both linked to the July 2025 AI Action Plan. Workforce elements focus on skilled trades and employer-led training, not on AI model builders.

### Cited Findings
- NIST plans to award up to $70 million over five years, with at least equal non-federal matching, for an "AI for Resilient Manufacturing" Manufacturing USA institute bringing together AI, manufacturing and supply chain expertise; tied to Pillars I and II of the July 2025 AI Action Plan (award status as of Nov 2026 not confirmed) — [ExecutiveGov](https://www.executivegov.com/articles/nist-issues-notice-of-intent-for-ai-focused-manufacturing-usa-institute)
- The institute is planned to run R&D, set up employer-led sectoral partnerships for training resources and create pathways for skilled workers (earlier planning-stage description) — [Assembly Magazine](https://www.assemblymag.com/articles/98586-nist-to-launch-ai-focused-manufacturing-institute)
- NIST announced in December 2025 a $20 million award to MITRE for two AI centers: one for manufacturing productivity, one for critical infrastructure cybersecurity — [King & Spalding](https://www.kslaw.com/insights/articles/nist-establishes-ai-centers-to-advance-us-manufacturing-productivity-and-critical-infrastructure-cybersecurity); [Manufacturing Dive](https://www.manufacturingdive.com/news/nist-20m-investment-strengthen-ai-cybersecurity/808614/)
- The AI Action Plan (July 2025) is described as mirroring manufacturing industry demands and including support for technical trades, electrical work and systems integration roles (secondary analysis) — [Manufacturing Today](https://manufacturing-today.com/news/white-house-ai-plan-mirrors-manufacturing-industry-demands/)

### Inferences
- Federal manufacturing-AI funding found here ($70M over five years plus $20M) is small relative to private activity (Palantir alone booked $984M US commercial revenue in one quarter). US industrial AI is being driven by vendors and customers, not by government programs.
- The workforce emphasis on trades and systems integration is consistent with the view that deployment and integration labor, not model development, is the bottleneck.

### Gaps
- NIST MEP: no source found linking MEP to AI programs or giving its 2026 funding status.
- CHIPS-related AI or workforce items: nothing found.
- DOE manufacturing AI programs: nothing found.
- Whether the AI Manufacturing USA institute award was made by Nov 2026, and to whom: not confirmed.
- The AI Action Plan text itself was not opened; its manufacturing and workforce items are from secondary summaries.

## 5. Market size figures for industrial AI

### Takeaway
Estimates range from about $3 billion to about $44 billion for the base year depending on scope, with forecast growth of 20 to 35% a year. All figures found are global; no US-only figure was found.

### Cited Findings
- IoT Analytics: global industrial AI market $43.6 billion in 2024, forecast $153.9 billion by 2030, 23% CAGR (report "Industrial AI Market Report 2025-2030"; paywalled, USD 5,000) — [IoT Analytics](https://iot-analytics.com/industrial-ai-market-insights-how-ai-is-transforming-manufacturing/); [IoT Analytics report page](https://iot-analytics.com/product/industrial-ai-market-report-2025-2030/)
- Verdantix: industrial AI analytics software only, $3.2 billion in 2025 to nearly $9.3 billion in 2031, 20% CAGR (global) — [Verdantix](https://research.verdantix.com/insights/report/market-size-and-forecast--industrial-ai-analytics-2025-2031-global)
- MarketsandMarkets: AI in manufacturing $34.18 billion in 2025 to $155.04 billion by 2030, about 35.3% CAGR (global) — [MarketsandMarkets](https://www.marketsandmarkets.com/Market-Reports/industrial-artificial-intelligence-market-72679105.html)

### Inferences
- The more than tenfold gap between Verdantix ($3.2B) and IoT Analytics ($43.6B) is a scope difference: Verdantix counts analytics software only, while the broader figures include hardware, services and infrastructure. If services and integration make up much of the broader figure, that fits the finding that deployment labor is a large part of industrial AI spending; the breakdown is behind paywalls and unconfirmed.

### Gaps
- No US-only market size found.
- No split of spending between software licences and services or integration found.
- No 2026 base-year update from IoT Analytics found; the 2024 base figure is the latest located.
