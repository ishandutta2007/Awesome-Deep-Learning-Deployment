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



- **OctoAI**

  Managed inference platform for optimized model serving. **Note**: Proprietary and cloud-hosted—no self-hosting option. Offers optimized inference for open-weight models with automatic scaling and pay-per-token pricing. **Best for**: teams wanting managed inference without infrastructure management.



- **NVIDIA TensorRT (Commercial Support)**

  **SDK for high-performance deep learning inference on NVIDIA GPUs**. The repository contains the **open-source components**—the core builder and runtime are distributed as pre-built binaries with commercial support available. **The reference for NVIDIA GPU inference**—takes an ONNX model, compiles it into a hardware-specific engine, and picks the fastest available GPU kernel for each layer.



- **Apple Core ML**

  **Apple's framework for on-device inference on iPhone, iPad, and Mac**. **Note**: The compiler and runtime are **closed-source**—you convert models using `coremltools` (open-source Python package) and deploy through Xcode. **The on-device choice** for Apple platforms—optimizes for the Neural Engine (ANE) and GPU.



- **Qualcomm SNPE (Snapdragon Neural Processing Engine)**

  **Qualcomm's SDK for inference on Snapdragon mobile and edge platforms**. **Note**: Proprietary—requires Qualcomm developer account. **The Snapdragon choice** for Android and IoT deployments.



- **AWS Neuron**

  **SDK for inference on AWS Inferentia and Trainium chips**. **Note**: Compiler and runtime are **closed-source**—you use the Neuron SDK to compile models for AWS silicon. **The AWS-specific choice** for cost-optimized inference on Inferentia instances.



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
