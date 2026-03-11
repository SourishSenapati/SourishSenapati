<div align="center">
  <img src="https://github.com/SourishSenapati/SourishSenapati/blob/main/sourish_github_banner_1773235042701.png?raw=true" width="100%" alt="Sourish Senapati – Chemical Engineering, AI, Industrial Robotics, Digital Twins" />
</div>

# Sourish Senapati

<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=22&pause=1000&color=00D4FF&center=true&vCenter=true&width=700&lines=Chemical+Engineering+%40+Jadavpur+University;IIT+Bombay+Techfest+AI+Finalist;Siemens+Campus+Connect+Ambassador;PINNs+%7C+OPC-UA+%7C+ROS2+%7C+Digital+Twins;Building+Systems+That+Enforce+Physics)](https://github.com/SourishSenapati)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sourish-senapati-0aba921b1)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:sourishs.chem.ug@jadavpuruniversity.in)
[![Tinkercad](https://img.shields.io/badge/Tinkercad-FF6D00?style=flat-square&logo=autodesk&logoColor=white)](https://www.tinkercad.com/users/SourishSenapati)
[![Profile Views](https://komarev.com/ghpvc/?username=SourishSenapati&style=flat-square&color=6e40c9&label=Profile+Views)](https://github.com/SourishSenapati)
[![GitHub](https://img.shields.io/badge/23_Public_Repos-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/SourishSenapati?tab=repositories)

**Chemical Engineering Undergraduate — Jadavpur University (2027)**
**Siemens Campus Connect Ambassador | IIT Bombay Techfest Finalist**

</div>

---

## Who I Am

I build systems where chemical physics and machine intelligence are not separate layers — they are the same layer. My code does not approximate the physics. It enforces it.

In three years I have shipped: an autonomous industrial gas detection swarm with OPC-UA SCADA integration, an AI-driven battery recycling digital twin selected for national competition, an interview simulator that reached the finalist stage at IIT Bombay Techfest, a market-pricing engine for perishable assets using biological degradation thermodynamics, a solar window cleantech prototype using carbon quantum dots from agricultural waste, and a plant biomonitoring system that converts leaf tissue data into carbon credit valuations.

**277 GitHub contributions** in the last year. **23 public repositories**. Every serious one is Apache-2.0 licensed and documented.

---

## Credentials at a Glance

- **IIT Bombay Techfest — AI Interviewer Competition Finalist** (NeuroPrep AI, 2025)
- **Siemens Campus Connect Student Ambassador** — confirmed, active
- **Indian Institute of Chemical Engineers (IIChE)** — Student Member
- **SURE Trust GS Robotics** — Certified Prototyper
- **Asian Paints** — Campus Ambassador
- **277 GitHub contributions** in 2025–2026 across **23 repositories**

---

## Tech Arsenal

<div align="center">

[![My Skills](https://skillicons.dev/icons?i=python,pytorch,tensorflow,cpp,typescript,react,nextjs,docker,postgres,redis&perline=10)](https://skillicons.dev)

[![My Skills](https://skillicons.dev/icons?i=nodejs,git,linux,vscode,matlab,html,js,css,flask,sqlite&perline=10)](https://skillicons.dev)

</div>

| Domain | Capabilities |
| --- | --- |
| Scientific ML | PINNs, SINDy, LangGraph multi-agent, GraphRAG, TensorRT FP16/ONNX |
| Deep Learning | PyTorch, YOLOv8, Vision Transformers, GNNs, MARL, CapsNet, WebNN |
| Process Engineering | Peng-Robinson EOS, Rachford-Rice solver, Gibbs stability, Monod kinetics |
| Industrial Protocols | OPC-UA (asyncua server), ZeroMQ, SCADA integration, SHA-256 WORM ledger |
| Robotics | ROS2 Humble, MAVROS, ArduPilot, Gazebo SITL, OpenCV CUDA, CUDA-APF |

---

## Signature Projects

### VectorSense — Autonomous Industrial Gas Plume Detection Swarm

**Repository:** [github.com/SourishSenapati/VECTORSENSE](https://github.com/SourishSenapati/VECTORSENSE)

> "General purpose drone optimised for different sensing tasks in the chemical industry."

The problem with industrial gas detection is not sensitivity — it is specificity. Conventional sensors cannot distinguish a genuine leak from sensor drift, humidity, or background VOCs. The result is nuisance alarm rates so high that operators learn to ignore them. That is not a safety system. That is theatre.

VectorSense replaces threshold-based alerting with a **Physics-Informed Neural Network** trained simultaneously as a supervised regression model and as a residual-minimiser against the Navier-Stokes advection-diffusion PDE. The network cannot produce a physically inconsistent plume model. That constraint alone eliminates the majority of false positive classes.

**Architecture — Brain-Stem Split:** The Stem executes deterministic low-latency flight control via ROS2/MAVROS. The Brain runs PINN inference across three mission modes — gas tomography, thermal profiling, acoustic diagnostics — with mode-switching over ZeroMQ pub-sub. The trained model is exported to ONNX FP16 for edge hardware and TensorRT for base station GPU inference.

**SINDy Calibration:** Sparse identification of nonlinear dynamics separates genuine chemical transients from environmental noise at the sensor level. Validated result: **85% reduction in false-positive alarm rate** versus threshold baselines.

**OPC-UA Industrial Gateway:** Translates sub-20 ms ZeroMQ telemetry into typed OPC-UA node updates for DCS/SCADA integration. Target translation latency: under 5 ms. Exposes a `Hazard_Mitigation` object enabling closed-loop Emergency Isolation Valve actuation from the SCADA layer.

**CUDA-APF Swarm Coordinator:** Artificial Potential Fields on PyTorch GPU tensors. Full 3-drone velocity resolution: under 2 ms on RTX 4050.

**WORM Audit Ledger:** SHA-256 Merkle chain in SQLite. Mathematical proof of data integrity for industrial safety inspections. Write overhead per entry: sub-0.1 ms.

**Seven ROS2 packages:** `vectorsense_intelligence`, `vectorsense_safety`, `vectorsense_vision`, `vectorsense_bridge`, `vectorsense_description`, `vectorsense_bringup`, `vectorsense_gazebo`.

---

### ENTRODYN-AERIAL — Physics-Informed Autonomous Drones for Gas Leak Localisation

**Repository:** [github.com/SourishSenapati/ENTRODYN-AERIAL](https://github.com/SourishSenapati/ENTRODYN-AERIAL)

Focused research vehicle for the gas leak localisation problem using thermodynamic entropy gradients and PINN-constrained trajectory planning for precise source localisation in cluttered environments. The scientific core from which VectorSense's sensing architecture was derived.

---

### RADORDENA / InnoSortRecycle — AI-Integrated Bio-Hydrometallurgical Battery Recycling

**Repository:** [github.com/SourishSenapati/InnoSortRecycle](https://github.com/SourishSenapati/InnoSortRecycle)

> "India's First AI-Integrated Bio-Hydrometallurgical Battery Recycling Network."

Global battery recycling is stuck at 5%. Pyrometallurgy emits 4.2 tonnes of CO₂ per tonne treated. India absorbs 1.6 million tonnes of EV battery waste by 2030. This is not a sustainability problem. It is a strategic materials crisis.

RADORDENA replaces the smelter with a precision **Sort-Bioleach-Recover** pipeline.

**SORT-01 Vision Agent:** YOLOv8-Nano with a hyperspectral head, Kubelka-Munk reflectance framework. 94.2% Top-1, 99.1% Top-5 accuracy.

**BIO-01 Process Agent:** *Acidithiobacillus ferrooxidans* bio-oxidation. PPO RL agent holds pH at 1.8 and temperature at 30°C with 50 ms control latency.

**Electro-Selective Recovery:** Li₂CO₃, Co(OH)₂, NiSO₄, MnCO₃. Financial model confirms >25% IRR. 2.5 tonnes CO₂ avoided per tonne processed.

**Targets:** >95% critical mineral recovery. 30% lower operating cost than pyrometallurgy. 128 GWh Indian EV battery market by 2030.

---

### NeuroPrep AI — Adaptive AI Interview Simulator

**IIT Bombay Techfest AI Interviewer Competition — Finalist**

**Repository:** [github.com/SourishSenapati/neuroprep-ai](https://github.com/SourishSenapati/neuroprep-ai)

> "224M+ Questions — Advanced AI Interview Platform with PWA Mobile Support."

Selected as a **Finalist at IIT Bombay Techfest** — one of Asia's largest technical festivals.

**NeuroSync Biometric Engine:** MediaPipe FaceMesh extracts micro-expressions from 478 facial landmarks. WebNN-accelerated CapsNet classifies anxiety state. Closed-loop difficulty adaptation in real time.

**Scale:** 224M+ questions generated. 12 disciplines. 8 seniority levels. 4 AI personas. GPT-4o / Claude 3.5 / Gemini Pro cascade. PWA mobile. Stack: Next.js 14, TypeScript, PostgreSQL, Docker, Vercel.

---

### Kinexica — Predictive Market-Maker for Perishable Assets

**Repository:** [github.com/SourishSenapati/Kinexica](https://github.com/SourishSenapati/Kinexica)

> "Translates invisible biological degradation into actionable market intelligence."

Markets systematically misprice perishable goods because biological degradation is invisible until it is too late. Kinexica fuses edge-deployed sensors with thermodynamic spoilage models to compute real-time fair value before conventional quality inspection detects decline. The gap between perceived and actual quality is the signal. **2 stars, 1 fork.**

---

### Team-Glass2Grid — Transparent Solar Windows from Agricultural Waste

**Repository:** [github.com/SourishSenapati/Team-Glass2Grid](https://github.com/SourishSenapati/Team-Glass2Grid)

Agricultural waste converted into **Carbon Quantum Dots** via hydrothermal synthesis. Dots embedded in transparent glass as a Luminescent Solar Concentrator. Windows absorb UV, re-emit as near-infrared at panel edges where photovoltaic strips generate electricity — without blocking visible light. Zero-opacity commercial windows that generate power. Tags: cleantech, circular-economy, quantum-dots, renewable-energy.

---

### GreenH2-ML-DT — Machine Learning for Green Hydrogen Catalyst Optimisation

**Repository:** [github.com/SourishSenapati/GreenH2-ML-DT-Revision](https://github.com/SourishSenapati/GreenH2-ML-DT-Revision)

Ensemble ML for PEM electrolyser catalyst efficiency prediction, predictive maintenance, and stack-level fault detection. Academic research project at Jadavpur University (Senapati and Biswash). Directly relevant to Siemens Energy's hydrogen technology portfolio.

---

### Morphaeon — PINNs + Graph Neural Networks + Multi-Agent Reinforcement Learning

**Repository:** [github.com/SourishSenapati/Morphaeon](https://github.com/SourishSenapati/Morphaeon)

Unified research framework integrating Physics-Informed Neural Networks, Graph Neural Networks, and Multi-Agent Reinforcement Learning. GNNs encode relational structure between physical agents. PINNs enforce physical consistency on each agent's forward model. MARL coordinates emergent collective behaviour. The architectural test bench from which production systems inherit their theoretical foundations.

---

### ORDINAR — Autonomous GRN Discovery via SINDy and LangGraph

**Repository:** [github.com/SourishSenapati/ORDINAR](https://github.com/SourishSenapati/ORDINAR)

> "Autonomous 5-Sigma Agentic Engine for Mechanistic Inference in Spatial Transcriptomics."

SINDy sparse identification infers governing ODEs from gene expression time series. LangGraph swarm (`DataArchitect`, `Theorist`, `Critic`) debates each regulatory link for biological plausibility. Tags: systems-biology, PINN, SINDy, digital-twin, spatial-transcriptomics, GPU-acceleration.

---

### NexusQ — Academic Intelligence Engine

**Repository:** [github.com/SourishSenapati/nexusq-academic](https://github.com/SourishSenapati/nexusq-academic)

Neo4j knowledge graph of engineering curriculum, queried via GraphRAG. A `SwarmJudge` — `Historian`, `Psychologist`, `Skeptic` — produces weighted consensus exam probability scores: `P_final = Σ(P_i × w_i) / Σ(w_i)`. Topics above 60% consensus flagged as high-priority.

---

### CODA-NS — Neuro-Symbolic Clinical Trial Data Agent

**Repository:** [github.com/SourishSenapati/NESTChemicalJU---CODA-NS](https://github.com/SourishSenapati/NESTChemicalJU---CODA-NS)

FDA-aligned safety rules enforced deterministically by a Python logic kernel, fused with learned pattern recognition across heterogeneous EDC and laboratory data sources. In regulated domains, safety-critical logic must be auditable and explicit — not absorbed into a weight matrix.

---

### AlcheMeal-AI — Multi-Agent Food Science System

**Repository:** [github.com/SourishSenapati/AlcheMeal-AI](https://github.com/SourishSenapati/AlcheMeal-AI)

Three-agent system: **Culinary Chemist Agent** applies Maillard reaction thermodynamics and enzymatic kinetics; **Process Engineer Agent** handles production logistics and scaling; **Market Oracle Agent** tracks ingredient pricing and supply chain volatility.

---

### Integrated Foliar-Particulate Bioanalytics — Plant Biomonitoring Research

**Repository:** [github.com/SourishSenapati/Integrated-Foliar-Particulate-Bioanalytics](https://github.com/SourishSenapati/Integrated-Foliar-Particulate-Bioanalytics)

APTI field data paired with PINN-modelled atmospheric fluid dynamics for spatially resolved PM2.5/PM10 deposition maps. The **SylvaNode** module converts leaf tissue biomonitoring data into **Verified Carbon Credit (VCC) profitability analysis** — quantifying urban green infrastructure as a distributed biological monitoring and carbon accounting network. Tags: air-quality, biomonitoring, carbon-credits, particulate-matter.

---

### PROJECT-ANCILE — Autonomous Inventory Engine for Group Travel

**Repository:** [github.com/SourishSenapati/PROJECT-ANCILE](https://github.com/SourishSenapati/PROJECT-ANCILE)

Autonomous inventory orchestration for the $900B MICE (Meetings, Incentives, Conferences, Exhibitions) economy. Dynamic microsite generation per event with real-time inventory management across accommodation, logistics, and venue components.

---

### ForkFleet — 3D Open-Source Ecosystem Navigator

**Repository:** [github.com/SourishSenapati/ForkFleet](https://github.com/SourishSenapati/ForkFleet)

Live GitHub data rendered as interactive 3D graph with dynamic pan navigation. Stack: TypeScript, Three.js, Next.js.

---

### ROS2Project2-SURETRUST — Robotics Foundations

**Repository:** [github.com/SourishSenapati/ROS2Project2-SURETRUST](https://github.com/SourishSenapati/ROS2Project2-SURETRUST)

SURE Trust GS Robotics certified project. ROS2 nodes, topics, transforms, and services — foundational systems work underpinning the VectorSense architecture. Tinkercad circuit simulation for sensor interface prototyping.

---

## Activity

<div align="center">

[![GitHub Trophies](https://github-profile-trophy.vercel.app/?username=SourishSenapati&theme=tokyonight&no-frame=true&no-bg=true&margin-w=4&row=1)](https://github.com/SourishSenapati)

</div>

<div align="center">

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=SourishSenapati&theme=tokyo-night&hide_border=true&area=true)](https://github.com/SourishSenapati)

</div>

<div align="center">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=SourishSenapati&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true&hide_border=true" alt="GitHub Stats" />
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=SourishSenapati&layout=compact&theme=tokyonight&hide_border=true" alt="Top Languages" />
</div>

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=SourishSenapati&theme=tokyonight&hide_border=true" alt="GitHub Streak" />
</div>

---

## Recognition and Affiliations

| | |
| --- | --- |
| IIT Bombay Techfest | Finalist — AI Interviewer Competition (NeuroPrep AI) |
| Siemens Campus Connect | Confirmed Student Ambassador — active membership |
| Indian Institute of Chemical Engineers (IIChE) | Student Member |
| SURE Trust (GS Robotics) | Certified Robotics Prototyper |
| Asian Paints | Campus Ambassador |
| Tinkercad (Autodesk) | Active — [tinkercad.com/users/SourishSenapati](https://www.tinkercad.com/users/SourishSenapati) |
| Jadavpur University | Chemical Engineering Undergraduate (2027) |

---

## What I Am Building Right Now

**VectorSense — Hardware-in-the-Loop Validation:** Full ROS2 package orchestration in Gazebo SITL with MAVROS ArduPilot. Testing PINN inference, APF swarm coordination, and OPC-UA gateway latency under realistic electromagnetic noise. Goal: physical deployment readiness.

**Morphaeon — Unified Physics-Constrained MARL Framework:** Extending toward a published, reusable framework where any multi-agent physical problem — chemical plant, power grid, logistics network — fits the same formalism.

**PINN Surrogates as Real-Time Process Observers:** Investigating whether PINN surrogates can replace first-principles ODE solvers in the inner loop of model predictive control — preserving physical interpretability while cutting latency by two orders of magnitude.

**SylvaNode — Carbon Credit Commercialisation API:** Moving from profitability modelling to a deployable API that converts live APTI sensor feeds into automated carbon credit issuance. Urban green infrastructure as a continuously-credited environmental asset.

**GreenH2 Research — Publication Track:** Tightening predictive maintenance models against real PEM electrolyser operational datasets. Target: peer-reviewed publication.

---

<div align="center">

*The pattern across every project here is the same: domain knowledge converted into working software.*
*Not proof-of-concept notebooks. Not reproduced tutorials.*
*Systems that make decisions, enforce physical law, and are either deployed or competition-validated.*

**If you are reading this and thinking about whether to reach out — you should.**

</div>
