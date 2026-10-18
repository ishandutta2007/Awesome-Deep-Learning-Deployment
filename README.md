# Awesome-Deep-Learning-Deployment

## Top Deep Learning Deployment Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Model Compilation, Runtime Optimization & Production Serving*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Deep Learning Deployment**. These tools enable developers to transform trained models into optimized, production-ready artifacts—from graph compilers that fuse operators and quantize weights to serving frameworks that handle batching, routing, and multi-model management.



**Examples** include Apache TVM, ONNX Runtime, OpenVINO, NVIDIA TensorRT, Apple Core ML, TensorFlow Lite, TorchScript, Qualcomm SNPE, Vitis AI, and OctoAI (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, cross-platform compilation, and open inference infrastructure—ideal for ML engineers, platform teams, and organizations seeking transparent, vendor-independent model deployment.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms

| Platform / Product | Company Size / Valuation / Revenue | Primary Focus / Deployment Scope | Starting Pricing | Free Tier / Trial Limits |
| :--- | :--- | :--- | :--- | :--- |
| **[NVIDIA NIM & AI Enterprise](https://www.nvidia.com/en-us/ai-data-science/products/nim/)** | ~$3.4 Trillion Market Cap ($120B+ ARR) | Optimized inference microservices and containerized deployment across NVIDIA GPUs | $1.00 per GPU-hour or $4,500 per GPU/year | 90-day free trial with 5,500 credits for NVIDIA AI Foundation Models; free local testing via NGC for research/individual use |
| **[Microsoft Azure AI Foundry & Azure ML](https://azure.microsoft.com/en-us/products/ai-foundry)** | ~$3.1 Trillion Market Cap ($140B+ Cloud ARR) | Managed enterprise model serving, ONNX Runtime integration, and Triton on AKS | $0.096/hour (`Standard_D2s_v5` CPU) or $0.38/hour (`Standard_NC4as_T4_v3` GPU) | 30-day free trial with $200 Azure credits, plus 12 months access to popular free services |
| **[Google Cloud Vertex AI](https://cloud.google.com/vertex-ai)** | ~$2.1 Trillion Market Cap ($40B+ Cloud ARR) | Managed serverless and dedicated endpoints for Gemma, PaLM, Gemini, and custom deep learning models | $0.0005 per 1k characters or $0.74/hour (`n1-standard-4` + NVIDIA T4 GPU) | 90-day free trial with $300 universal Google Cloud credits for new accounts |
| **[AWS SageMaker & Bedrock](https://aws.amazon.com/sagemaker/)** | ~$2.1 Trillion Market Cap ($105B+ AWS ARR) | Real-time, asynchronous, and serverless deep learning endpoints with AWS Neuron & GPU support | $0.05/hour (`ml.t3.medium` CPU) or $0.526/hour (`ml.g4dn.xlarge` GPU) | 2 months free trial with 250 hours/month of `ml.t3.medium` instances under AWS Free Tier |
| **[Fireworks AI](https://fireworks.ai/)** | $17.5 Billion Valuation ($1.5B Series D, $1B+ ARR) | Low-latency generative model serving, compound AI systems, and custom LoRA adapter hosting | $0.20 per 1M tokens (Llama 3 8B) or $0.00055/GPU-sec for on-demand dedicated deployments | $1 free starter credit upon account registration (approx. 5M tokens on 8B models); no expiry date |
| **[Modal](https://modal.com/)** | $15.75 Billion Valuation ($750M Series D, $1B+ ARR) | Serverless Python-defined container infrastructure with sub-second cold starts and scale-to-zero | $0.000163/core-sec CPU, $0.000588/sec for NVIDIA T4 (~$2.12/hr), $0.001097/sec for A10G | $30/month in free compute credits renewing forever; up to 10 concurrent GPUs and 3 workspace seats |
| **[Baseten](https://www.baseten.co/)** | $13.0 Billion Valuation ($1.5B Series F) | Production model serving backed by Truss packaging, Triton engine, and zero-idle cost scaling | $0.20 per 1M tokens or $0.033/min ($1.98/hour) for dedicated NVIDIA A10G instances | $30 free compute credits upon account creation for testing serverless deployments |
| **[Together AI](https://www.together.ai/)** | $8.3 Billion Valuation ($800M Series C) | Serverless open-source model inference endpoints and dedicated multi-GPU serving clusters | $0.18 per 1M tokens (Llama 3.1 8B), $0.88 per 1M tokens (70B), or $1.25/GPU-hour dedicated | $5 free credit upon account registration valid for 3 months to test serverless APIs |
| **[Hugging Face Inference Endpoints](https://huggingface.co/inference-endpoints)** | $4.5 Billion Valuation ($235M Series D) | Fully managed containerized model deployments directly from the Hugging Face Model Hub | $0.03/hour (CPU small) or $0.50/hour (NVIDIA T4 GPU 16GB) | Serverless Inference API is free forever up to 1,000 requests/day (rate limited to 30 requests/min) |
| **[Groq Cloud](https://groq.com/)** | $2.8 Billion Valuation (Series D) | Ultra-high throughput, deterministic low-latency inference powered by custom LPUs | $0.05 per 1M input tokens and $0.08 per 1M output tokens (Llama 3.1 8B) | Free forever plan with 30 requests/minute, 14,400 requests/day, and 30,000 tokens/minute (no credit card required) |
| **[Anyscale Endpoints](https://www.anyscale.com/)** | $1.0 Billion Valuation ($100M Series C) | Distributed Ray-based production model serving and high-performance inference clusters | $0.15 per 1M tokens (Llama 3 8B) or $0.40/GPU-hour on managed Anyscale Cloud clusters | 30-day free trial with $50 free credits upon sign-up |
| **[Replicate](https://replicate.com/)** | $350 Million Valuation (Acquired / Integrated into Cloudflare) | Pay-per-second API serving for open-source AI models packaged with Cog containers | $0.000100/sec ($0.36/hour) for CPU, $0.000550/sec ($1.98/hour) for NVIDIA A40 GPU | $5 free credit on initial signup (equivalent to ~45 minutes of T4 GPU compute) |
| **[OctoAI](https://octo.ai/)** | $165 Million Valuation (Acquired by NVIDIA in 2024) | TVM-backed automated compilation, runtime acceleration, and hosted endpoint serving | $0.10 per 1M tokens or $0.05/hour for containerized endpoint runtime | 30-day free trial with $10 free credits upon registration |



## Open-Source GitHub Projects



- **Apache TVM**

  **Open Machine Learning Compiler Framework** (Apache-2.0) — **the most comprehensive open-source DL compiler** . **13,500+ GitHub stars** and **1,020+ contributors** . **Python-first development** enables quick customization; **universal deployment** brings models into minimum deployable modules . **Cross-level design** with **TensorIR** for tensor-level representation and **Relax** for graph-level representation—jointly optimizing computational graphs, tensor programs, and libraries . **Targets CPUs, GPUs, and specialized accelerators**—Metal, Vulkan, OpenCL, ROCm, CUDA, and more . **The foundation for building domain-specific vertical compilers** (e.g., for LLMs) . **Best for**: teams wanting **a fully open, hackable compiler stack** that targets diverse hardware without vendor lock-in.



- **ONNX Runtime**

  **Cross-platform, high-performance scoring engine for Open Neural Network Exchange (ONNX) models** (MIT) — **the most widely deployed open-source inference runtime**. **Supports CPU, GPU, and specialized execution providers** including **OpenVINO, QNN (Qualcomm), DirectML, TensorRT, and CoreML**. **ONNX Runtime v1.22** introduced **Auto EP Selection** (automatic execution provider selection) and a **Compile API** for explicit model compilation . **KleidiAI integration** enhances Arm performance; **MatMulNBits** enables 8-bit quantized matrix multiplication . **The portability choice**—one model format runs across platforms and hardware. **Best for**: teams wanting **broad hardware support without rewriting models** per platform.



- **Intel OpenVINO**

  **Open Visual Inference and Neural Network Optimization toolkit** (Apache-2.0) — **the Intel hardware choice**. **Optimizes inference across Intel CPUs, integrated GPUs, and VPUs** (Neural Compute Stick). **OpenVINO 2026** removed the deprecated `openvino.runtime` namespace, requires **AVX2 as minimum CPU requirement**, and **discontinued the Model Optimizer** in favor of new conversion methods . **GenAI support** covers LLMs and diffusion models with reduced runtime footprint . **Best for**: teams deploying on **Intel hardware** who want **vendor-optimized inference without CUDA dependency**.



- **NVIDIA TensorRT (Open-Source Components)**

  **High-performance deep learning inference on NVIDIA GPUs** (Apache-2.0 for the open components) — **the open-source parsers, plugins, and samples** that accompany the proprietary TensorRT core . **The TensorRT ecosystem** includes **trtexec** for building and benchmarking engines, ONNX parsing, and runtime APIs for C++ and Python . **Best for**: teams already committed to NVIDIA GPUs who want **maximum inference performance** and can accept the proprietary core.



- **Triton Inference Server**

  **Cloud inferencing solution optimized for both CPUs and GPUs** (BSD-3-Clause) — **the serving layer** . **Provides an inference service via HTTP or gRPC endpoint**—remote clients request inference for any model managed by the server . **Edge deployment available as a shared library**—full server functionality embedded directly in an application . **Supports TensorRT, PyTorch, ONNX, vLLM, and Python backends** . **Best for**: teams needing **a production serving layer** that handles model management, batching, and multi-framework backends.



- **TensorFlow Lite (LiteRT)**

  **TensorFlow's lightweight solution for mobile and embedded devices** (Apache-2.0) — **the mobile deployment standard**. **Converts TensorFlow models to a compact FlatBuffer format** optimized for on-device inference. **Supports Android, iOS, and embedded Linux** with hardware acceleration via **GPU delegates, NNAPI, and Core ML delegates**. **Best for**: teams deploying **TensorFlow models to mobile and edge devices**.



- **TorchScript**

  **A way to create serializable and optimizable models from PyTorch code** (BSD-3-Clause) — **the PyTorch-native export path**. **Traces or scripts PyTorch models** into an intermediate representation that can run independently of Python. **The foundation for PyTorch deployment**—TorchScript models can be served via TorchServe, exported to ONNX, or compiled by TensorRT. **Best for**: teams committed to PyTorch who want **a standard export path** before choosing a runtime.



- **ExecuTorch**

  **Meta's on-device inference runtime for PyTorch** (BSD-3-Clause) — **the PyTorch mobile/edge choice** . **1.0 GA October 2025** with **50KB footprint** and **12+ hardware backends** . **Billions of users** across Meta's apps . **Best for**: teams deploying **PyTorch models to mobile and embedded devices** without leaving the PyTorch ecosystem.



### Additional Strong Open-Source Options



- **vLLM** — **High-throughput LLM inference engine** (Apache-2.0) — **the production default for LLM serving**. **PagedAttention** for KV cache management, **continuous batching**, and **OpenAI-compatible API**. **Best for**: serving LLMs at scale on GPU.

- **SGLang** — **Fast inference for LLMs and multimodal models** (Apache-2.0) — **the agentic workload specialist**. **RadixAttention** for prefix caching, **400,000+ GPUs in production** across xAI, LinkedIn, Cursor, Oracle, GCP, Azure, and AWS . **Best for**: multi-turn agent workloads and prefix-heavy serving.

- **llama.cpp** — **CPU, GPU, and Metal inference** (MIT) — **the reference for quantized CPU serving**. **Widest model support** and **full control over quantization and threading** . **Best for**: edge, embedded, and CPU-only deployments.

- **Ollama** — **Dev-laptop one-command install** (MIT) — **wraps llama.cpp with model-management UX**. **15-30% slower than llama.cpp** due to Go + CGo + HTTP serialization, but **the fastest path to a running model** . **Best for**: development and single-user inference.

- **AIKit (Kaito)** — **Fine-tune, build, and deploy open-source LLMs easily** (open-source) — **OCI packaging** for models, **OpenAI-compatible API**, **multi-modal support**, **Kubernetes-ready** with NVIDIA CUDA and AMD ROCm . **No GPU needed for local testing** (`docker run -d -p 8080:8080 ghcr.io/kaito-project/aikit/llama3.1:8b`) . **Best for**: teams wanting **containerized model deployment with supply-chain security** (SBOMs, signed images).

- **LiteRT-LM (Google AI Edge)** — **Production-ready orchestration layer to run LLMs with LiteRT** (Apache-2.0) — **cross-platform support** for Android, iOS, Web, Desktop, and IoT (Raspberry Pi) . **Hardware acceleration** via GPU and NPU, **multi-modality** (vision and audio), **tool use** for agentic workflows, and **broad model support** (Gemma, Llama, Phi-4, Qwen) . **Powers on-device GenAI in Chrome, Chromebook Plus, and Pixel Watch** . **Best for**: teams deploying **LLMs to edge devices** with Google's production-validated stack.

- **Seldon Core** — **Kubernetes-native model serving** (Apache-2.0) — **multi-step inference pipelines**, **drift detection**, **MLServer** for multi-model per GPU, and **Prometheus/ELK/Jaeger integrations** . **Best for**: teams running **complex inference graphs on Kubernetes** with observability built in.

- **ClearML** — **ML/DL development and production suite** (Apache-2.0) — **Model-Serving** module with **GPU serving backed by NVIDIA Triton**, **out-of-the-box model monitoring**, and **fractional GPUs** for container-level memory limits . **Best for**: teams wanting **experiment tracking, orchestration, and serving in one platform**.

- Community **n8n** workflows for model compilation pipeline automation and inference alerting.



**Frameworks for building custom systems**: Combine **Apache TVM** for cross-hardware compilation with **ONNX Runtime** for portability, **TensorRT** for NVIDIA GPU performance, **OpenVINO** for Intel optimization, **vLLM** or **SGLang** for LLM serving, and **Triton Inference Server** for production serving—creating a comprehensive deployment stack that spans development to production.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Deep learning deployment tools must be evaluated for **hardware target coverage**, **model format support**, **quantization capabilities**, and **licensing** (fully open vs. open components around proprietary cores).

- **The "compiler vs. runtime vs. server" distinction matters.** **Compilers** (TVM, TensorRT, OpenVINO) transform models into optimized executables for specific hardware. **Runtimes** (ONNX Runtime, vLLM, SGLang, llama.cpp) execute models. **Servers** (Triton, Seldon Core) provide HTTP/gRPC endpoints for production serving. **Most production stacks combine all three**—compile with TVM or TensorRT, serve with Triton or vLLM.

- **Engine selection is a function of hardware, scale, and ecosystem—not a leaderboard read.** **CPU-first → llama.cpp**. **AMD GPU → vLLM** (TRT-LLM is NVIDIA-locked). **NVIDIA Hopper → vLLM, SGLang, or TRT-LLM**. **Apple Silicon → llama.cpp (Metal)**. **1 user/dev → Ollama**. **10-100 users → vLLM single-GPU**. **100-10k users → vLLM production-stack or SGLang**. **10k+ users → vLLM production-stack + disaggregated + LMCache** .

- **TGI entered maintenance mode December 11, 2025.** Only bug fixes—**~10% slower raw throughput than vLLM** but historically top observability and HF-ecosystem integration . **That maintenance status makes it a risky long-term bet**—SGLang or vLLM are safer defaults for new projects .

- **Apache TVM is the most comprehensive fully open compiler option.** **13,500+ stars, 1,020+ contributors, Apache-2.0** . **TensorIR + Relax cross-level design** jointly optimizes graphs, tensor programs, and libraries . **The trade-off is complexity**—TVM has a steeper learning curve than vendor-specific toolchains. **Choose TVM when portability across diverse hardware matters more than turnkey simplicity.**

- **ONNX Runtime is the portability standard.** **Auto EP Selection** in v1.22 simplifies choosing the right execution provider per model . **The trade-off**: broad hardware coverage, but **not always the absolute peak performance** that a vendor-specific compiler tuned for one chip can deliver.

- **Vendor-specific compilers deliver peak performance at the cost of lock-in.** **TensorRT** picks the fastest GPU kernel per layer but only runs on NVIDIA GPUs . **OpenVINO** optimizes for Intel hardware but requires **AVX2 minimum** in 2026 and has **discontinued the Model Optimizer** . **Core ML** targets Apple silicon exclusively. **Choose vendor compilers when you've committed to that hardware**—use TVM or ONNX Runtime when you need to hedge.

- Self-hosted open-source solutions require proper GPU/hardware provisioning, model validation, and ongoing maintenance. **Compiler optimizations can introduce numerical differences**—validate outputs against the reference implementation before production deployment.



---



**Made for ML engineers, platform teams, and organizations building transparent inference solutions.**  

Let's make Deep Learning Deployment more open, data-driven, and hardware-aware.
