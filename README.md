# Awesome NVIDIA Agentic Skills & MCP Servers

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](http://creativecommons.org/publicdomain/zero/1.0/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](./CONTRIBUTING.md)

A curated, product-line-organized registry of agentic skills, MCP servers, and coding-agent integrations for **all** NVIDIA products.

The goal is to be the definitive place to discover and install resources that let AI agents and coding assistants work with NVIDIA hardware, software, and cloud services.

**Inclusion criteria:** Resources must be agent-facing or coding-assistant oriented — MCP servers, agentic skills, provider extensions, or reference implementations with a clear agent interface. General SDK docs and tutorials are out of scope. See [CONTRIBUTING.md](./CONTRIBUTING.md) for the full quality bar.

---

## Contents

- [AI / LLM / Inference](#ai--llm--inference)
  - [NVIDIA NIM](#nvidia-nim)
  - [NVIDIA NeMo](#nvidia-nemo)
  - [TensorRT-LLM, vLLM & NVIDIA Dynamo](#tensorrt-llm-vllm--nvidia-dynamo)
- [Agent Runtimes & Sandboxes](#agent-runtimes--sandboxes)
- [Data Science / ML](#data-science--ml)
- [Scientific Computing](#scientific-computing)
- [HPC / Cluster / Workload Management](#hpc--cluster--workload-management)
- [Cloud / Orchestration / Kubernetes](#cloud--orchestration--kubernetes)
- [Networking](#networking)
- [Simulation / Physical AI / Robotics](#simulation--physical-ai--robotics)
- [Graphics / Gaming](#graphics--gaming)
- [Automotive](#automotive)
- [Healthcare / Life Sciences](#healthcare--life-sciences)
- [Edge / IoT](#edge--iot)
- [Security](#security)
- [UI / Design](#ui--design)
- [Agent / IDE Integrations](#agent--ide-integrations)
- [OpenCode Skills in this Workspace](#opencode-skills-in-this-workspace)
- [Contributing](#contributing)
- [License](#license)

---

## AI / LLM / Inference

### NVIDIA NIM

[NVIDIA NIM](https://www.nvidia.com/en-us/ai/nim/) provides optimized, containerized AI model inference microservices.

- **[NVIDIA NIM](https://github.com/nvidia/nim)** `Official` — Microservice inference for NVIDIA-optimized AI models.
- **[NIM API Catalog](https://build.nvidia.com/explore/discover)** `Official` — Browse hosted models and get API keys.
- **[NIM Documentation](https://docs.nvidia.com/nim/)** `Official` — Deployment guides and API reference.
- **[NVIDIA NIM Deploy](https://github.com/NVIDIA/nim-deploy)** `Official` — Reference YAML/Helm/Operator implementations for Kubernetes.
- **[NVIDIA NIM Anywhere](https://github.com/NVIDIA/nim-anywhere)** `Official` — Reference project for Gen AI development with NIM + AI Workbench.
- **[nvidia-nim-mcp](https://github.com/david-eve-za/nvidia-nim-mcp)** `Community` — TypeScript MCP server for NVIDIA NIM.
  - Install: clone, `npm install`, build, run.
- **[nvidia-nim-mcp](https://github.com/tungns84/nvidia-nim-mcp)** `Community` — Python MCP server for NVIDIA NIM.
- **[nim-mcp-server](https://github.com/Murchiz/nim-mcp-server)** `Community` — MCP server that indexes code with RAG over NIM.

### NVIDIA NeMo

[NVIDIA NeMo](https://www.nvidia.com/en-us/ai/neemo/) is an end-to-end framework for building and customizing generative AI models.

- **[NVIDIA NeMo](https://github.com/NVIDIA/NeMo)** `Official` — Framework for building, customizing, and deploying generative AI.
- **[NVIDIA NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails)** `Official` — Open-source toolkit for controllable and safe LLM conversational systems.
- **[nemo-guardrails-mcps](https://github.com/razashariff/nemo-guardrails-mcps)** `Community` — MCP plugin for NeMo Guardrails with message signing and audit logging.

### TensorRT-LLM, vLLM & NVIDIA Dynamo

- **[TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM)** `Official` — High-performance LLM inference on NVIDIA GPUs.
- **[vLLM](https://github.com/vllm-project/vllm)** `Community` — High-throughput LLM inference engine commonly paired with NIM.
- **[NVIDIA Dynamo](https://github.com/ai-dynamo/dynamo)** `Official` — Open-source inference serving platform for generative AI.

---

## Agent Runtimes & Sandboxes

Resources that provide agent frameworks, runtimes, or sandboxes built on NVIDIA technology.

- **[NVIDIA NeMo Agent Toolkit](https://github.com/NVIDIA/NeMo-Agent-Toolkit)** `Official` — Build agent workflows and expose them as MCP servers.
  - Install: `uv pip install nvidia-nat-mcp`
  - Run: `nat mcp serve --config_file config.yml`
- **[NVIDIA AI-Q Blueprint](https://github.com/NVIDIA-AI-Blueprints/aiq)** `Official` — Multi-agent deep-research blueprint using NeMo Agent Toolkit and MCP client groups.
  - Deploy with `uv sync`, add `mcp_client` function groups to the YAML workflow config.
- **[NVIDIA RAG Blueprint](https://github.com/NVIDIA-AI-Blueprints/rag)** `Official` — Enterprise RAG with an MCP server exposing ingestion and generation tools.
  - Run: `python mcp_server.py --transport sse|streamable_http|stdio` after blueprint deployment.
- **[NVIDIA NemoClaw](https://github.com/NVIDIA/NemoClaw)** `Official` — Reference stack for running OpenClaw / Hermes agents inside NVIDIA OpenShell sandboxes.
  - Install: single-command curl installer, then `nemoclaw` CLI.
- **[NVIDIA nv-ingest](https://github.com/NVIDIA/nv-ingest)** `Official` — Document extraction microservice consumed by the RAG Blueprint.
  - Install: `pip install nv-ingest`
- **[nemo-agent-mcp](https://github.com/bina165/nemo-agent-mcp)** `Community` — Design, validate, run, and serve NeMo Agent Toolkit workflows from Claude Code / Desktop.

---

## Data Science / ML

GPU-accelerated data science, machine learning, and optimization tools.

- **[RAPIDS](https://rapids.ai/)** `Official` — GPU-accelerated data science with cuDF, cuML, cuGraph, and cuSpatial.
- **[NVIDIA DALI](https://github.com/NVIDIA/DALI)** `Official` — GPU-accelerated data loading and augmentation.
- **[NVIDIA cuOpt](https://github.com/NVIDIA/cuOpt)** `Official` — GPU-accelerated combinatorial optimization.
- **[NVIDIA TAO Toolkit](https://github.com/NVIDIA/TAO)** `Official` — Low-code model training and adaptation toolkit.
- **[NVIDIA Morpheus](https://github.com/NVIDIA/morpheus)** `Official` — AI cybersecurity framework (also listed under Security).

---

## Scientific Computing

Physics-informed ML, simulation, weather/climate, and quantum-classical computing.

- **[NVIDIA Modulus](https://github.com/NVIDIA/modulus)** `Official` — Physics-ML model framework.
- **[NVIDIA Warp](https://github.com/NVIDIA/warp)** `Official` — Python framework for high-performance differentiable simulation.
- **[NVIDIA PhysicsNeMo](https://github.com/NVIDIA/physicsnemo)** `Official` — Physics-informed machine learning.
- **[NVIDIA Earth2Studio](https://github.com/NVIDIA/earth2studio)** `Official` — Weather and climate simulation workflows.
- **[NVIDIA CUDA-Q](https://github.com/NVIDIA/cuda-quantum)** `Official` — Quantum-classical computing platform.
- **[cudaq-mcp](https://github.com/Haadi-Khan/cudaq-mcp)** `Community` — MCP server for CUDA-Q workflows.

---

## HPC / Cluster / Workload Management

Cluster management, workload scheduling, and on-prem/HPC GPU platforms.

- **[NVIDIA Base Command Manager](https://www.nvidia.com/en-us/data-center/base-command-manager/)** `Official` — Cluster management, workload orchestration, and GPU configuration.
- **[NVIDIA Run:ai](https://www.run.ai/)** `Official` — GPU orchestration, fractional GPU allocation, and workload scheduling.
- **[NVIDIA DGX / DGX Cloud](https://www.nvidia.com/en-us/data-center/dgx/)** `Official` — Purpose-built AI infrastructure and cloud service.
- **[Slurm Workload Manager](https://slurm.schedmd.com/)** `Community` — Open-source HPC scheduler commonly used with NVIDIA DGX clusters.

---

## Cloud / Orchestration / Kubernetes

Kubernetes operators, cloud orchestration, and fleet management.

- **[NVIDIA GPU Operator](https://github.com/NVIDIA/gpu-operator)** `Official` — Manage NVIDIA GPU resources in Kubernetes.
- **[k8s-nim-operator](https://github.com/NVIDIA/k8s-nim-operator)** `Official` — Deploy and maintain NVIDIA NIM microservices on Kubernetes.
- **[NVIDIA Fleet Command](https://www.nvidia.com/en-us/data-center/fleet-command/)** `Official` — Secure edge AI orchestration and management.
- **[NVIDIA Network Operator](https://github.com/Mellanox/network-operator)** `Official` — Kubernetes networking for NVIDIA Spectrum and BlueField.

---

## Networking

AI networking, SmartNICs, and data-center interconnects.

- **[NVIDIA Spectrum-X](https://www.nvidia.com/en-us/networking/spectrum-x/)** `Official` — AI Ethernet networking fabric.
- **[NVIDIA BlueField / DOCA](https://github.com/NVIDIA/doca)** `Official` — Data-center infrastructure-on-a-chip software framework.

---

## Simulation / Physical AI / Robotics

Simulation, robotics, vision AI, and physical-AI platforms.

- **[NVIDIA Omniverse](https://www.nvidia.com/en-us/omniverse/)** `Official` — Real-time collaboration and simulation platform.
- **[NVIDIA Isaac Sim](https://github.com/NVIDIA-Omniverse/IsaacSim)** `Official` — Robotics simulation environment.
- **[NVIDIA Isaac Lab](https://github.com/isaac-sim/IsaacLab)** `Official` — Learning-based robot training framework.
- **[NVIDIA OSMO](https://www.nvidia.com/en-us/deep-learning-ai/solutions/osmo/)** `Official` — Cloud-native robotics AI platform.
- **[NVIDIA Cosmos](https://github.com/nvidia-cosmos)** `Official` — Physical AI world foundation models.
- **[NVIDIA Metropolis / DeepStream](https://github.com/NVIDIA-AI-IOT/deepstream)** `Official` — Vision AI and streaming analytics.
- **[NVIDIA RTX Remix](https://github.com/NVIDIAGameWorks/rtx-remix)** `Official` — AI-powered modding runtime.
- **[USDcodeNIM_MCP](https://github.com/jph2/USDcodeNIM_MCP)** `Community` — MCP for Cursor wrapping the NVIDIA USD Code NIM.
- **[isaacsim-mcp](https://github.com/mochan-b/isaacsim-mcp)** `Community` — MCP server for NVIDIA Isaac Sim.
- **[nvidia-isaac-mcp](https://github.com/nullbyte91/nvidia-isaac-mcp)** `Community` — LLM-to-fleet connection for Isaac Sim or real Nav2 robots.
- **[nvidia-omniverse-isaacsim-mcp-server](https://github.com/mateuszbestai/nvidia-omniverse-isaacsim-mcp-server)** `Community` — MCP bridge for Omniverse / Isaac Sim.
- **[omniverse-mcp](https://github.com/serionist/omniverse-mcp)** `Community` — MCP server for NVIDIA Omniverse.
- **[nayantra](https://github.com/shashankbr27/nayantra)** `Community` — LLM fleet control for Isaac Sim / Open-RMF robots.

---

## Graphics / Gaming

AI-powered graphics, upscaling, and game technologies.

- **[NVIDIA DLSS / RTX](https://www.nvidia.com/en-us/geforce/technologies/dlss/)** `Official` — AI-powered graphics upscaling and RTX technologies.

---

## Automotive

Autonomous vehicle development platforms.

- **[NVIDIA DRIVE / DRIVE AGX](https://www.nvidia.com/en-us/self-driving-cars/drive-platform/)** `Official` — End-to-end autonomous vehicle platform.

---

## Healthcare / Life Sciences

AI for healthcare, drug discovery, genomics, and medical imaging.

- **[NVIDIA BioNeMo](https://github.com/NVIDIA/bionemo-framework)** `Official` — Generative AI for drug discovery and biology.
- **[NVIDIA MONAI](https://github.com/Project-MONAI/MONAI)** `Official` — Open-source medical imaging AI framework.
- **[NVIDIA Parabricks](https://github.com/NVIDIA/parabricks)** `Official` — GPU-accelerated genomic analysis.
- **[NVIDIA Clara Holoscan](https://github.com/nvidia-holoscan)** `Official` — Real-time sensor processing for healthcare.
- **[evo2-nim-mcp](https://github.com/zzgael/evo2-nim-mcp)** `Community` — MCP server for the NVIDIA Evo2 NIM (DNA scoring, variant analysis).

---

## Edge / IoT

Edge AI computing and sensor processing.

- **[NVIDIA Jetson](https://www.nvidia.com/en-us/autonomous-machines/embedded-systems/)** `Official` — Edge AI and robotics computing platform.
- **[NVIDIA Holoscan](https://github.com/nvidia-holoscan)** `Official` — Real-time sensor processing at the edge.
- **[jetson-mcp-agent](https://github.com/beret21/jetson-mcp-agent)** `Community` — MCP server exposing Jetson Xavier CUDA/GPU resources to Claude Code.

---

## Security

AI-driven cybersecurity frameworks.

- **[NVIDIA Morpheus](https://github.com/NVIDIA/morpheus)** `Official` — AI cybersecurity framework for building applications that detect and mitigate threats.

---

## UI / Design

Agent-facing design systems and UI tooling.

- **[NVIDIA Elements](https://github.com/NVIDIA/elements)** `Official` — Design system with an official MCP server for AI coding assistants.
  - Install: `npm install -g @nvidia-elements/cli`
  - Run: `nve mcp`

---

## Agent / IDE Integrations

Coding agents and IDEs with native or community NVIDIA support.

- **[Continue.dev NVIDIA Provider](https://docs.continue.dev/customize/model-providers/more/nvidia)** `Official` — Native `provider: nvidia` for NIM endpoints.
  - Config: add `provider: nvidia`, `model: <MODEL_ID>`, `apiKey: <NVIDIA_API_KEY>` to `.continue/config.yaml`.
- **[OpenClaw NVIDIA Provider](https://docs.openclaw.ai/providers/nvidia)** `Official` — Built-in NVIDIA provider supporting 150+ NIM models.
  - Set `NVIDIA_API_KEY`, then `openclaw models set nvidia/nvidia/nemotron-3-ultra-550b-a55b`.
- **[OpenCode NVIDIA NIM](https://docs.opencode.ai)** `Official` — OpenCode supports NVIDIA as an OpenAI-compatible provider.
  - Config: set `provider.nvidia` in `~/.config/opencode/opencode.json` with `baseURL: https://integrate.api.nvidia.com/v1`.
- **[Claude Code + NIM](https://docs.nvidia.com/nim/large-language-models/latest/ai-assistant-integrations/claude-code.html)** `Official` — Use Claude Code with a NIM endpoint via Anthropic-compatible `/v1/messages`.
  - Set `ANTHROPIC_BASE_URL=http://<NIM_ENDPOINT>:<PORT>` and `ANTHROPIC_API_KEY=not-used`.
- **[pi-nvidia-nim](https://github.com/xRyul/pi-nvidia-nim)** `Community` — NVIDIA NIM provider extension for the pi coding agent.
  - Install: `pi install git:github.com/xRyul/pi-nvidia-nim`
- **[pi-nvidia-extension](https://github.com/lutfi-zain/pi-nvidia-extension)** `Community` — Another pi-coding-agent NVIDIA NIM provider with interactive `/login nvidia`.
  - Install: `pi install git:github.com/lutfi-zain/pi-nvidia-extension`
- **[Cline + NIM](https://github.com/VISHWAJ33T/local-nim-coding-stack/blob/main/configs/cline-config.md)** `Community` — Cline configuration for NIM free endpoints.
- **[local-nim-coding-stack](https://github.com/VISHWAJ33T/local-nim-coding-stack)** `Community` — VS Code setup combining Ollama, Continue, Cline, and NVIDIA NIM.
- **[nim-doctor](https://github.com/Gowrav-M/nim-doctor)** `Community` — Diagnostic CLI for NVIDIA NIM + agent-tool readiness.
  - Run: `npx nim-doctor`
- **[Continue-NIM-Proxy](https://github.com/FAI-Solutions/Continue-NIM-Proxy)** `Community` — Proxy fixing empty-response issues in Continue with NIM.
- **[NIMbus](https://github.com/cyberofficial/NIMbus)** `Community` — FastAPI proxy translating Anthropic requests to NIM's OpenAI endpoint.

---

## OpenCode Skills in this Workspace

The following OpenCode-compatible skills are available in the current workspace and target NVIDIA products. They follow the convention of one directory per skill containing a single `SKILL.md` with YAML frontmatter.

- **base-command-manager** `Official` — Expert NVIDIA Base Command Manager administration.
  - Install: copy/symlink `base-command-manager/` into `~/.config/opencode/skills/` or reference via the OpenCode plugin.
- **bcm-user** `Official` — Base Command Manager end-user workflows.
- **runai** `Official` — Run:ai GPU orchestration, CLI, REST API, and policies.
- **kubernetes-dev** `Official` — Kubernetes workflows including NVIDIA GPU Operator, MIG, and Triton.
- **mlops-engineer** `Official` — MLOps workflows with CUDA/GPU resource management and model serving.
- **train-deploy-ml** `Official` — Generic ML train/deploy lifecycle flow skill.

---

## Contributing

Read [CONTRIBUTING.md](./CONTRIBUTING.md) for the quality bar, entry format, and PR process.

---

## License

This list is released into the public domain under [CC0-1.0](./LICENSE).

## Need implementation help?

Enterprise AI Atlas is maintained by [Vibe Coding Agency](https://vibecodingagency.com). If your team needs support designing, building, or deploying production AI systems covered in this atlas, [get in touch](https://vibecodingagency.com).
