# CudaUdemy
CUDA Parallel Programming masterclass on Udemy.

## Section 1

### 1.2 - Introduction to Parallel Programming

- Task Level vs Data Level Parallelism
  - Task Level: Differrent task on same or different data.
  - Data Level: Same task on different data.
- Parallelism vs Concurrency
  - Parallelism: We have enough cores for multiple processes to run at the same time.
  - Concurrency: Time multiplexing allows "context" of each task to be changed and some incremental amount of work is completed for each task sequentially (this looks parallel to the human eye).

### 1.3 - Supercomputing

Performance of a supercomputer is measured using Floating Point Operations (FPU).

GPU (Graphics Processing Unit)

- Adresses demands of real time high resolution 3d graphics compute intensive tasks.
- CPU has a few cores with a large instruction set and has optimization hardware like branch predictors.
- GPU has thousands of light cores - "Throughput device"

GPU vs CPU

- Context switching: GPU - done by hardware, CPU - done by software.
- Thread schedulers / dispatch units - GPU implemented in hardware, CPU - work item created in software.

Heterogeneous computer

- Use more than one kind of processor or cores.
- Gain performance or energy efficiency by adding specialized / dissimilar coprocessors that can handle particular tasks.

### 1.4 - First Look at CUDA Programming

CUDA (Compute Unified Device Architecture) is a parallel computing platform and API model created by Nvidia. Enables us to use Nvidia GPU for general purpose computing (GPGPU - General Purpose Computing in Graphic Processing Unit).

On Windows, use Run > dxdiag. This brings up the DirectX Diagnostic Tool. What microarchitecture & compute capability is my GPU?

[Supported CUDA GPU Wiki](https://en.wikipedia.org/wiki/CUDA#GPUs_supported). Determine the latest CUDA SDK version you can use based on your GPU's microarchitecture and compute capability.

**Laptop GPU**

- NVIDIA GeForce 940MX
- Microarchitecture: Maxwell
- Compute Capability: 5.0

**Desktop GPU**

- GeForce 1070 GTX
- Microarchitecture: Pascal
- Compute Capability: 6.1

CUDA SDK 11.3 supports both of my GPUs.

The command prompt command to check if the toolkit installed properly is "nvcc --version"