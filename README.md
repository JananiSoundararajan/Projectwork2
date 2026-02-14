## ARCTICOS – AI-Native GPU-Centric Runtime for Compute-Centric Operating Systems

ARCTICOS is a GPU-centric runtime architecture designed to optimize AI and high-performance computing workloads by minimizing CPU–GPU synchronization overhead and enabling accelerator-aware execution above an unmodified Linux operating system.

### About

ARCTICOS (AI-Native Runtime for Compute-Centric Operating Systems) is a research-oriented runtime framework that redefines how operating systems interact with GPUs. Traditional operating systems are CPU-centric, where GPUs are treated as peripheral devices controlled via drivers. This design creates bottlenecks for modern AI and HPC workloads that rely heavily on parallel accelerator execution.

ARCTICOS introduces a layered runtime model that operates above an unmodified Linux OS. It separates responsibilities into:

CPU Control Plane – Responsible for coordination, safety, initialization, and interaction with the Linux kernel.

GPU Data Plane – Responsible for execution scheduling, GPU-owned memory management, and runtime simulation.

By reducing repetitive CPU intervention and keeping data resident within accelerator memory, ARCTICOS improves execution locality, scalability, and runtime efficiency for heterogeneous systems.

### Features

GPU-centric runtime execution model

CPU–GPU control plane separation

Scheduler simulation inside GPU runtime

GPU-owned memory management strategy

Reduced CPU–GPU synchronization overhead

Compatibility with unmodified Linux systems

Designed for AI and HPC workloads

Scalable runtime architecture for heterogeneous systems

### Requirements

Operating System: Ubuntu 20.04 / 22.04 (Linux-based system required)

Hardware: NVIDIA GPU (RTX 3050 or higher recommended)

Programming Language: Rust (for runtime implementation), C/C++ (optional integration)

System Interfaces: Linux system calls, POSIX APIs

GPU Support: CUDA Toolkit / NVIDIA Drivers

Version Control: Git

IDE / Editor: VSCode / CLion / Neovim


### Additional Dependencies:

CUDA Runtime

Linux Kernel headers

Cargo (Rust package manager)

Make / GCC toolchain

### System Architecture

The ARCTICOS architecture follows a layered runtime approach:

<img width="400" height="500" alt="image" src="https://github.com/user-attachments/assets/0170ad04-f500-408b-b978-459842ae705c" />


### Output
#### Output 1 – Runtime Initialization

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/be6c0c4c-1586-4577-a940-f6d5713bf26b" />


### Output 2 – Task Execution Monitoring

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/9acf9a8d-a4ac-4db2-b3cb-ce985c52fb30" />


### Performance Metrics (Prototype Evaluation)

<img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/580bdef5-7055-448b-b054-b1caf489b78b" />


Note: Metrics depend on workload characteristics and hardware configuration.

### Results and Impact

ARCTICOS demonstrates that GPUs can be treated as first-class execution platforms at the runtime level without modifying the Linux kernel.

#### Impact:

Reduces CPU bottlenecks in AI/HPC workloads

Improves execution locality and scalability

Enables compute-centric operating system research

Provides foundation for accelerator-native OS architectures

Supports future research in AI-assisted scheduling

ARCTICOS serves as a stepping stone toward accelerator-centric computing environments where GPUs actively participate in runtime decision-making rather than being passively controlled by CPUs.

### Future Enhancements

Multi-GPU runtime coordination

Distributed GPU-aware cluster runtime

AI-driven adaptive scheduling policies

Kernel-level integration (future research direction)

NUMA-aware GPU memory optimization

Integration with containerized AI platforms

### Articles Published / References

S. Kato, M. McThrow, C. Maltzahn, and S. Brandt, “Gdev: First-Class GPU Resource Management in the Operating System,” USENIX ATC, 2012.

L. Zhang et al., “Persistent Kernels for Iterative Memory-Bound GPU Applications,” IEEE/ACM SC, 2018.

J. Veselý et al., “GPU System Calls and System Service Requests,” IEEE ISPASS, 2018.

NVIDIA Corporation, “GPUDirect Technology Overview,” 2019.

O. Kayiran et al., “Managing GPU Concurrency in Heterogeneous Architectures,” MICRO, 2015.

S. Novakovic et al., “Scale-Out NUMA,” ACM SIGARCH CAN, 2014.

J. Zhong and B. He, “Kernelet: High-Throughput GPU Kernel Executions,” IEEE TPDS, 2014.

J. Power et al., “Heterogeneous System Coherence for Integrated CPU–GPU Systems,” MICRO, 2013.
