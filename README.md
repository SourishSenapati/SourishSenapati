<!-- SOURISH SENAPATI | Chemical Engineering × AI × Industrial Robotics -->

<div align="center">
  <img src="https://github.com/SourishSenapati/SourishSenapati/blob/main/banner.png?raw=true" width="100%" alt="Sourish Senapati — Chemical Engineering, AI Systems, Industrial Robotics" />
</div>



<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=20&pause=1200&color=00D4FF&center=true&vCenter=true&width=750&lines=Chemical+Engineer+who+writes+production+code.;PINNs+%7C+OPC-UA+%7C+ROS2+%7C+Digital+Twins;IIT+Bombay+Techfest+AI+Finalist.;Siemens+Campus+Connect+Ambassador.;Building+systems+that+enforce+physics.)](https://github.com/SourishSenapati)

</div>

<div align="center">

[![LinkedIn](https://img.shields.io/badge/_%40sourishsenapati-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sourish-senapati-0aba921b1)
[![Email](https://img.shields.io/badge/_Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:sourishs.chem.ug@jadavpuruniversity.in)
[![Tinkercad](https://img.shields.io/badge/_Tinkercad-FF6D00?style=for-the-badge&logo=autodesk&logoColor=white)](https://www.tinkercad.com/users/SourishSenapati)
[![GitHub](https://img.shields.io/badge/_23_Repos-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/SourishSenapati?tab=repositories)

</div>

<div align="center">

![Profile Views](https://komarev.com/ghpvc/?username=SourishSenapati&style=flat-square&color=00D4FF&label=Profile+Views)
&nbsp;&nbsp;
**Chemical Engineering @ Jadavpur University (2027)**

</div>

---

## The Short Version

I am a third-year chemical engineering student at Jadavpur University. My academic record is not exceptional. What I do have is a pattern of building things — real things, not notebooks — that sit at the boundary between physical science and machine intelligence.

The distinction matters. A lot of ML applied to engineering treats the physics as context, not constraint. My work does the opposite. When I trained a PINN for gas plume detection, the network had to satisfy the Navier-Stokes residual on every forward pass. When I built a bioreactor control agent, it operated on actual Monod kinetics and Arrhenius penalty functions. The physics is not decoration. It is the architecture.

Seventeen repositories worth of evidence. A Techfest finalist medal from IIT Bombay. A live Siemens Ambassador credential. Here is what I have been building.

---

## Credentials

<div align="center">

| | |
| :---: | :--- |
| [![Techfest](https://img.shields.io/badge/IIT_Bombay_Techfest-AI_Finalist_2025-gold?style=flat-square&logo=trophy&logoColor=black)](https://github.com/SourishSenapati/neuroprep-ai) | **AI Interviewer Competition — Finalist** |
| [![Siemens](https://img.shields.io/badge/Siemens-Campus_Connect_Ambassador-009999?style=flat-square&logo=siemens&logoColor=white)](https://www.siemens.com) | **Confirmed active member — Industry 4.0 engagement** |
| [![AsianPaints](https://img.shields.io/badge/Asian_Paints-Alchemy_Campus_Ambassador-E63946?style=flat-square&logoColor=white)](https://www.asianpaints.com) | **Alchemy Campus Ambassador** |
| [![IIChE](https://img.shields.io/badge/IIChE-Student_Member-1D3461?style=flat-square&logoColor=white)](https://www.iiche.org.in) | **Indian Institute of Chemical Engineers** |
| [![SURE](https://img.shields.io/badge/SURE_Trust-Certified_Robotics_Prototyper-4CAF50?style=flat-square&logo=ros&logoColor=white)](https://github.com/SourishSenapati/ROS2Project2-SURETRUST) | **GS Robotics Programme** |

</div>

---

## Tech Stack

<div align="center">

[![Skills](https://skillicons.dev/icons?i=python,pytorch,cpp,typescript,react,nextjs,docker,postgres,neo4j,linux&perline=10)](https://skillicons.dev)
[![Skills](https://skillicons.dev/icons?i=nodejs,git,vscode,matlab,redis,html,js,css,flask,sqlite&perline=10)](https://skillicons.dev)

</div>



<div align="center">

| Scientific ML | Process Engineering | Industrial Systems | Robotics |
| :---: | :---: | :---: | :---: |
| PINNs · SINDy | Peng-Robinson EOS | OPC-UA · SCADA | ROS2 · MAVROS |
| LangGraph · GraphRAG | Rachford-Rice · Gibbs | ZeroMQ · SHA-256 WORM | ArduPilot · Gazebo SITL |
| TensorRT FP16/ONNX | Monod kinetics | Asyncua server | OpenCV CUDA · APF |

</div>

---

## Projects

### VectorSense — Autonomous Industrial Gas Leak Detection

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://github.com/SourishSenapati/VECTORSENSE)
[![ROS2](https://img.shields.io/badge/ROS2_Humble-22314E?style=flat-square&logo=ros&logoColor=white)](https://github.com/SourishSenapati/VECTORSENSE)
[![OPC--UA](https://img.shields.io/badge/OPC--UA_Gateway-009999?style=flat-square&logoColor=white)](https://github.com/SourishSenapati/VECTORSENSE)
[![Repo](https://img.shields.io/badge/Repo-VECTORSENSE-181717?style=flat-square&logo=github)](https://github.com/SourishSenapati/VECTORSENSE)

The starting point for this project was frustration. Industrial gas detectors produce so many false positives that operators stop trusting them. That is a well-documented problem with a poorly-documented solution. My answer was to replace the threshold with physics.

A Physics-Informed Neural Network trained against the Navier-Stokes advection-diffusion residual governs the plume model. The network learns from data but cannot produce a solution that violates the governing PDE. That constraint, on its own, eliminates most false positive classes before any secondary filtering. Combined with SINDy-based sensor drift separation, the validated false-positive reduction is **85%**.

The system is built around what I call the Brain-Stem Split. The Stem handles deterministic low-latency flight control over ROS2/MAVROS. The Brain — PINN inference, ZeroMQ message routing, OPC-UA node updates — runs asynchronously and feeds decisions back through a typed industrial interface that SCADA systems can consume directly. The OPC-UA gateway exposes a `Hazard_Mitigation` object that enables closed-loop Emergency Isolation Valve actuation from the plant control layer. Translation latency: under 5 ms per update.

Multi-drone coordination runs CUDA-accelerated Artificial Potential Fields on PyTorch tensors. Three-drone velocity resolution: under 2 ms on an RTX 4050. A SHA-256 Merkle-chain WORM ledger in SQLite records every telemetry event with cryptographic linkage to its predecessor — producing mathematical proof of data integrity for safety audits at under 0.1 ms write overhead per entry.

Seven ROS2 packages. Gazebo SITL environment. ONNX FP16 export for edge hardware. TensorRT for base station inference.

---

### ENTRODYN-AERIAL — Gas Leak Localisation via Entropy Gradients

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://github.com/SourishSenapati/ENTRODYN-AERIAL)
[![Repo](https://img.shields.io/badge/Repo-ENTRODYN--AERIAL-181717?style=flat-square&logo=github)](https://github.com/SourishSenapati/ENTRODYN-AERIAL)

The science underneath VectorSense. Thermodynamic entropy gradients drive PINN-constrained trajectory planning for source localisation in cluttered environments. Built as a focused research vehicle before the full system was assembled.

---

### RADORDENA / InnoSortRecycle — Battery Recycling Digital Twin

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://github.com/SourishSenapati/InnoSortRecycle)
[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)](https://github.com/SourishSenapati/InnoSortRecycle)
[![Repo](https://img.shields.io/badge/Repo-InnoSortRecycle-181717?style=flat-square&logo=github)](https://github.com/SourishSenapati/InnoSortRecycle)

India's EV battery waste problem arrives at 1.6 million tonnes by 2030. The incumbent solution — pyrometallurgical smelting — emits 4.2 tonnes of CO₂ per tonne of input and cannot selectively recover lithium from the mix. RADORDENA replaces it with a Sort-Bioleach-Recover pipeline.

Three agents in sequence. SORT-01 is a YOLOv8-Nano with a hyperspectral head trained on NMC, LFP, and LCO spectral signatures using the Kubelka-Munk framework. It achieves 94.2% Top-1 accuracy and routes feedstock before a gram of contaminant reaches the bioleaching reactor. BIO-01 is a PPO reinforcement learning agent that manages *Acidithiobacillus ferrooxidans* bacterial cultures — holding pH at 1.8 and temperature at 30°C with 50 ms feedback latency, because above 35°C the Arrhenius penalty collapses bacterial activity by 40%. The electro-recovery stage precipitates Li₂CO₃, Co(OH)₂, NiSO₄, and MnCO₃ sequentially.

Financial model confirms greater than 25% IRR. Carbon credit revenue: 2.5 tonnes CO₂ avoided per tonne processed, calculated against the pyrometallurgy baseline.

---

### NeuroPrep AI — Adaptive Interview Simulator

[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://github.com/SourishSenapati/neuroprep-ai)
[![Next.js](https://img.shields.io/badge/Next.js_14-000000?style=flat-square&logo=next.js&logoColor=white)](https://github.com/SourishSenapati/neuroprep-ai)
[![IIT Bombay Techfest Finalist](https://img.shields.io/badge/IIT_Bombay_Techfest-AI_Finalist-gold?style=flat-square&logo=star&logoColor=black)](https://github.com/SourishSenapati/neuroprep-ai)
[![Repo](https://img.shields.io/badge/Repo-neuroprep--ai-181717?style=flat-square&logo=github)](https://github.com/SourishSenapati/neuroprep-ai)

Finalist at IIT Bombay Techfest — one of Asia's largest engineering festivals. 224 million questions generated. The system reads a candidate's biometric stress signal from their webcam and adapts the interview in real time.

MediaPipe FaceMesh extracts micro-expression features from 478 facial landmarks — eyebrow displacement, jaw tension, pupil dilation — and a WebNN-accelerated CapsNet classifies anxiety state. Fitbit heart rate via Web Bluetooth augments the estimate with HRV data. High stress shifts the AI toward scaffolded Socratic questions. Low stress brings adversarial probing with explicit derivation requirements.

GPT-4o leads the provider cascade. Claude 3.5 Sonnet is secondary. Gemini Pro third. If all three fail, rule-based fallbacks keep the session running. Response analysis produces: EQ score, AI-text detection flag, technical accuracy score, and a Neural Resilience Index percentile.

Twelve engineering disciplines. Eight seniority levels. Four AI personas. PWA mobile support. Stack: Next.js 14, TypeScript, PostgreSQL, Docker, Vercel.

---

### Kinexica — Perishable Asset Market Intelligence

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://github.com/SourishSenapati/Kinexica)
[![Stars](https://img.shields.io/github/stars/SourishSenapati/Kinexica?style=flat-square&color=00D4FF)](https://github.com/SourishSenapati/Kinexica)
[![Repo](https://img.shields.io/badge/Repo-Kinexica-181717?style=flat-square&logo=github)](https://github.com/SourishSenapati/Kinexica)

The question that started this: if biological degradation follows predictable thermodynamic kinetics, why is the market price of a perishable good not updated continuously to reflect it? The answer is that measurement has always been too slow and too coarse. Kinexica uses edge-deployed sensors fused with spoilage models to compute real-time asset valuations before conventional quality inspection can detect any change. The gap between the market price and the model price is the trade signal.

---

### Team-Glass2Grid — Solar Windows from Agricultural Waste

[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://github.com/SourishSenapati/Team-Glass2Grid)
[![Repo](https://img.shields.io/badge/Repo-Team--Glass2Grid-181717?style=flat-square&logo=github)](https://github.com/SourishSenapati/Team-Glass2Grid)

Lignocellulosic agricultural waste converted to Carbon Quantum Dots via hydrothermal synthesis. The dots are embedded in a Luminescent Solar Concentrator glass matrix — absorbing UV, re-emitting as near-infrared at panel edges where photovoltaic strips convert it to power. Fully transparent to visible light. ESG tracking across the full supply chain closes the circular economy loop.

---

### GreenH2-ML-DT — ML for Green Hydrogen Catalyst Efficiency

[![HTML](https://img.shields.io/badge/Research-Apache_2.0-blue?style=flat-square&logo=bookstack&logoColor=white)](https://github.com/SourishSenapati/GreenH2-ML-DT-Revision)
[![Repo](https://img.shields.io/badge/Repo-GreenH2--ML--DT-181717?style=flat-square&logo=github)](https://github.com/SourishSenapati/GreenH2-ML-DT-Revision)

Formal academic research at Jadavpur University (Senapati and Biswash). Ensemble ML for PEM electrolyser catalyst efficiency prediction. The ALTFS framework detects thermal runaway, membrane fouling, and surface poisoning before they cause downtime. Directly relevant to Siemens Energy's hydrogen portfolio.

---

### Morphaeon — Unified PINNs + GNNs + MARL Framework

[![Repo](https://img.shields.io/badge/Repo-Morphaeon-181717?style=flat-square&logo=github)](https://github.com/SourishSenapati/Morphaeon)

An experimental architecture integrating Physics-Informed Neural Networks, Graph Neural Networks, and Multi-Agent Reinforcement Learning. GNNs encode relational structure between physical agents. PINNs enforce physical consistency on each forward model. MARL coordinates collective behaviour. The theoretical foundation from which production systems inherit their design.

---

### ORDINAR — Autonomous Gene Regulatory Network Discovery

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://github.com/SourishSenapati/ORDINAR)
[![Repo](https://img.shields.io/badge/Repo-ORDINAR-181717?style=flat-square&logo=github)](https://github.com/SourishSenapati/ORDINAR)

SINDy sparse inference extracts governing ODEs directly from gene expression time series. A LangGraph swarm — DataArchitect, Theorist, Critic — debates each proposed regulatory link against biological priors before it enters the network. The result is an interpretable, mechanistically grounded GRN rather than a correlation matrix. Tags: systems-biology, PINN, SINDy, spatial-transcriptomics.

---

### NexusQ — Academic Intelligence Engine

[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://github.com/SourishSenapati/nexusq-academic)
[![Repo](https://img.shields.io/badge/Repo-nexusq--academic-181717?style=flat-square&logo=github)](https://github.com/SourishSenapati/nexusq-academic)

Neo4j knowledge graph of engineering curriculum queried via GraphRAG. Three adversarial agents — Historian, Psychologist, Skeptic — produce weighted consensus exam probability scores. Topics above 60% consensus are flagged. The SwarmJudge computes: `P_final = Σ(P_i × w_i) / Σ(w_i)`.

---

### CODA-NS — Neuro-Symbolic Agent for Clinical Trials

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://github.com/SourishSenapati/NESTChemicalJU---CODA-NS)
[![Repo](https://img.shields.io/badge/Repo-CODA--NS-181717?style=flat-square&logo=github)](https://github.com/SourishSenapati/NESTChemicalJU---CODA-NS)

FDA-aligned safety rules enforced via a deterministic Python logic kernel. Pattern recognition across heterogeneous EDC and lab sources is learned. Safety-critical logic is auditable and explicit — never absorbed into weights.

---

### AlcheMeal-AI — Multi-Agent Food Science System

[![Repo](https://img.shields.io/badge/Repo-AlcheMeal--AI-181717?style=flat-square&logo=github)](https://github.com/SourishSenapati/AlcheMeal-AI)

Three agents: Culinary Chemist (Maillard thermodynamics, enzymatic kinetics), Process Engineer (logistics and scaling), Market Oracle (ingredient pricing and supply chain volatility). Chemical engineering applied to food production at scale.

---

### Integrated Foliar-Particulate Bioanalytics

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://github.com/SourishSenapati/Integrated-Foliar-Particulate-Bioanalytics)
[![Repo](https://img.shields.io/badge/Repo-Foliar--Bioanalytics-181717?style=flat-square&logo=github)](https://github.com/SourishSenapati/Integrated-Foliar-Particulate-Bioanalytics)

APTI field data paired with PINN-modelled atmospheric fluid dynamics for spatially resolved PM2.5/PM10 deposition mapping. The SylvaNode module converts leaf-tissue biomonitoring readings into Verified Carbon Credit profitability analysis — urban green infrastructure as a distributed, continuously-credited environmental asset. Tags: air-quality, biomonitoring, carbon-credits.

---

### PROJECT-ANCILE — MICE Economy Inventory Engine

[![Repo](https://img.shields.io/badge/Repo-PROJECT--ANCILE-181717?style=flat-square&logo=github)](https://github.com/SourishSenapati/PROJECT-ANCILE)

Autonomous inventory orchestration for the $900B Meetings, Incentives, Conferences, and Exhibitions economy. Per-event microsite generation with real-time management of accommodation, logistics, and venue components.

---

### Supporting Work

| Project | Description |
| --- | --- |
| [ForkFleet](https://github.com/SourishSenapati/ForkFleet) | 3D GitHub ecosystem navigator — live data, Three.js, TypeScript |
| [ROS2Project2-SURETRUST](https://github.com/SourishSenapati/ROS2Project2-SURETRUST) | SURE Trust GS Robotics certified — ROS2 foundations, Tinkercad circuit prototyping |

---

## Activity

<div align="center">

[![Trophies](https://github-profile-trophy.vercel.app/?username=SourishSenapati&theme=tokyonight&no-frame=true&no-bg=true&margin-w=6&row=1&column=7)](https://github.com/SourishSenapati)

</div>

<div align="center">

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=SourishSenapati&theme=tokyo-night&hide_border=true&area=true&area_color=00D4FF)](https://github.com/SourishSenapati)

</div>

<div align="center">

<img height="175em" src="https://github-readme-stats.vercel.app/api?username=SourishSenapati&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true&hide_border=true" alt="GitHub Stats" />
&nbsp;
<img height="175em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=SourishSenapati&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" alt="Top Languages" />

</div>

<div align="center">

<img src="https://github-readme-streak-stats.herokuapp.com/?user=SourishSenapati&theme=tokyonight&hide_border=true" alt="GitHub Streak" />

</div>

---

## What Is Being Built Right Now

**VectorSense — hardware-in-the-loop.** Running full ROS2 orchestration in Gazebo SITL to validate PINN inference latencies, APF swarm coordination, and OPC-UA round-trip times under realistic RF noise. The goal is physical deployment readiness, not simulation performance.

**Morphaeon — publishable framework.** Extending it toward a unified formalism where any multi-agent physical system — chemical plant, power grid, logistics network — can be modelled in the same architecture. PINNs for physical consistency, GNNs for relational structure, MARL for collective control.

**SylvaNode — carbon credit API.** Moving from profitability modelling to a live API that converts APTI sensor readings into automated VCC issuance. Urban trees as continuously-priced environmental assets.

**GreenH2 — publication track.** Tightening predictive maintenance model accuracy against real PEM electrolyser operational benchmarks. Target: peer-reviewed publication.

---

<div align="center">

The work here is not a portfolio. It is a track record.
Every project started with a problem that did not have a good solution and ended with something that runs.
If that is the kind of builder you are looking for — reach out.

</div>
