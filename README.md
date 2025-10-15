# HeteroSim

### Overview

**HeteroSim** is a GPU-accelerated simulation framework for high-fidelity, large-scale heterogeneous language model (LLM) training.  
It enables accurate, scalable, and data-driven emulation of distributed AI systems composed of diverse GPUs, interconnects, and communication backends.  

By integrating computation, communication, and scheduling into a unified simulation engine, HeteroSim achieves sub-percent simulation error and supports the exploration of new system architectures, parallel strategies, and network configurations under realistic heterogeneous environments.

---

### Core Innovations

- **IR-Based Workload Compiler**  
  Compiles model definitions, parallel strategies, and training schedules into a unified intermediate representation (IR), enabling precise mapping of computation and communication events.

- **Heterogeneity-Aware Computation Planner**  
  Dynamically allocates workloads based on GPU performance, topology bandwidth, and memory hierarchy, maximizing system efficiency in mixed-generation GPU clusters.

- **NCCL-Assisted Communication Planner**  
  Provides accurate modeling of hierarchical collective operations (e.g., all-reduce, broadcast) across NVLink, PCIe, and RoCE fabrics, ensuring consistency with real-world NCCL performance.

---

### System Architecture

![Architecture](./docs/heterosim_arch.jpg)

HeteroSim adopts a **three-layer data-oriented design** to couple model semantics with system dynamics efficiently:

1. **Workload Layer** — Parses model graphs, parallelization strategies, and batch configurations, then compiles them into IR.  
2. **Execution Plan Layer** — Generates optimized execution schedules considering device heterogeneity, interconnect topology, and communication strategies.  
3. **Simulation Engine Layer** — Executes the unified plan in a fully GPU-accelerated environment, jointly simulating computation, synchronization, and data movement.  





