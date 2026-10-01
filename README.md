Hi, I'm Laalini 👋
ML Research Engineer · LLM agents, evaluation, RL and formally verified systems

I build ML systems that hold up outside the notebook: pretraining under tight compute, RL environments, agentic pipelines with evals and guardrails, and models whose key guarantees are proved, not just tested. By day I build agentic AI, evals and guardrails at Commonwealth Bank of Australia.

📄 Research
Non-Isobaric Is Not Enough: Gap-Merge Safety for Unambiguous Peptide Readout

Preprint (ChemRxiv) · Code and Lean proofs · under review at the Journal of Proteome Research

Focus: Formal verification (Lean 4), molecular data storage, tandem mass spectrometry.
Shows that the standard safeguard for peptide data storage (non-isobaric residues) is insufficient: one missing fragment ion can merge two residues into a gap that reads as a third, producing a silent error.
Defines gap-merge safety, a decidable condition with a machine-checked Lean 4 proof (zero sorry), and finds exactly two such collisions in the standard alphabet beyond Leu/Ile: Gly+Gly=Asn and Gly+Ala=Gln.
Safe alphabets gave zero silent errors at every simulated dropout rate; the guarantee held after calibration on 5,112 cleavage sites from public spectra.
PLM v2: a Perceptive Language Model for Neuromorphic Drone Control

Code

Focus: Vision-language-action models, spiking neural networks, speculative control, edge deployment.
Maps camera + LiDAR/4D-radar + IMU + a natural-language command ("fly to the red beacon") to smooth chunks of flight commands, using leaky integrate-and-fire spiking attention and closed-form liquid time-constant recurrence.
Four-stage curriculum: BEV modality alignment, self-supervised JEPA dynamics, language-conditioned imitation with DAgger, and speculative co-training with GRPO.
Verify-behind runtime: a ~0.1M-parameter edge drafter flies the drone while the full model verifies its actions in batches off the critical path, behind a control-barrier-function safety filter. In the CPU-scale run it matched the full model's success with zero collisions at about 6× lower critical-path latency (4.1 ms vs 24.2 ms).
Documents two instructive failures, kept in the repo: a "copycat" policy that looked great offline but never left hover, and a colour-blind policy caused by geometry-only perception training.
🚀 Projects
🏗️ Pretraining & Optimization
Parameter Golf submission
Focus: Model pretraining, compute efficiency, transformer scaling constraints.
Transformer pretraining under fixed parameter and compute budgets, tuning architecture and learning-rate schedule for throughput and stable convergence.
Protogrok: telecom small language model
Focus: Domain-specific pretraining, custom tokenization, JAX.
A 300M-parameter language model pretrained from scratch on raw packet-level network data, with a custom structural tokenizer.
🕹️ Reinforcement Learning
CRM Env (rlenv)
Focus: RL environments, reward design, conversational agents.
A gym-style environment that scores conversations with a rubric, used to train customer-facing agents toward a business metric (Net Promoter Score). Paper under review at ACM ICAIF 2026.
🤖 Agents & Orchestration
Anvyon Agentic
Focus: Deterministic orchestration, intent-driven routing, evaluation-as-judge.
Open-source agent framework implementing the validation-first loops from my book, Build Your Own Optimised AI Agents Using CrewAI & LangChain: schema grounding and state machines to catch production failure modes.
🌾 Open-Source Contributions
KrishiLekha
Focus: Multilingual NLP, speech and OCR pipelines.
A multilingual assistant delivering policy and agricultural advice across Indian languages through a speech → OCR → NLP → recommendation pipeline.
🛠️ Technical Toolkit
Languages: Python, SQL
ML: PyTorch, JAX/Flax, Hugging Face, LoRA, OpenAI Gym
Agents & evals: Google ADK, LangGraph, LangChain, LLM-as-judge, RAGAS
Formal methods: Lean 4
Core domains: Transformer pretraining, reinforcement learning, multimodal and spiking models, agent evaluation and guardrails
📬 Connect With Me
👔 LinkedIn: laalini-bhogadi
🆔 ORCID: 0009-0007-3275-5650
📙 My Books:
Build Your Own Optimised AI Agents Using CrewAI & LangChain
The Enterprise LLM Blueprint: A Complete Technical Guide to Architecting, Deploying, and Scaling Large Language Models in the Enterprise
