# Learning Log

This file records the knowledge and hands-on work that existed when **Atom to Intelligence** began. It is not a claim that every topic has been mastered. It is the starting inventory from which the polished chapters will be built.

## Computer Foundations

- Explored atoms, electrons, electricity, switches, and the physical basis of computing.
- Developed a working model of transistors and logic gates as the foundation of digital computation.
- Studied binary, machine instructions, and common assembly operations.
- Learned the CPU fetch-decode-execute cycle.
- Explored registers, RAM, storage, buses, firmware, UEFI/BIOS, bootloaders, kernels, and operating systems.
- Reasoned through sleep, hibernation, saved state, and volatile versus persistent memory.
- Traced the memory hierarchy from feedback and SR latches through gated and D latches, edge-triggered flip-flops, multi-bit registers, shared buses, control signals, clock timing, and fetch-decode-execute.
- Current mental model: gates make decisions; latches and flip-flops retain state; registers hold groups of bits; buses move them; the control unit coordinates updates at clock edges.

## Programming and Development Tools

- Set up Python 3.12 on macOS.
- Created and used a Python virtual environment.
- Installed NumPy, pandas, matplotlib, Jupyter, and PyTorch.
- Learned core terminal, Git, and GitHub workflows.
- Created an evolving AI-Learning repository with code and written lessons.
- Practiced versioning, documentation, commits, pushes, README maintenance, and `.gitignore` rules.

## Machine Learning From Scratch

- Built a single-neuron predictor manually in Python.
- Added weights and bias.
- Calculated prediction error and squared loss.
- Used multiple training examples.
- Implemented gradient calculations and parameter updates.
- Implemented batch gradient descent.
- Expanded a neuron from one input to multiple inputs.
- Explored activation functions, hidden layers, multilayer perceptrons, and XOR.
- Used epochs, training loops, inference, confidence, and evaluation.
- Explored autograd-style value tracking and backpropagation concepts.
- Built early experiments involving curiosity, reinforcement learning, sequence learning, memory, and anomaly detection.

## Networking and Cybersecurity

- Reviewed IP addressing, subnet masks, default gateways, DNS, Wi-Fi interference, and basic troubleshooting.
- Studied virtualization, sandboxing, MAC addresses, DHCP, and public IP changes.
- Explored payloads, persistence, lateral movement, encryption, and quantum-safe cryptography.
- Began integrating Security+ concepts into a broader bottom-up technical foundation.

## Current Strengths

- Strong curiosity and willingness to reason from first principles.
- Comfortable connecting hardware, software, networking, cybersecurity, and AI concepts.
- Able to understand machine-learning code after building the mechanics manually.
- Increasing confidence explaining why systems work rather than merely repeating definitions.

## Current Gaps

- Electronics and semiconductor physics need a more rigorous foundation.
- Assembly and machine code are understood conceptually but need hands-on labs.
- Operating systems and networking need deeper structured study.
- Mathematical notation should be introduced gradually and tied to concrete behavior.
- Transformer architecture and modern language-model training remain future sections.
- Citations, diagrams, code tests, and chapter review standards must be established.

## Progress Update — July 31, 2026

- Reviewed visual explanations of semiconductor behavior, P-type and N-type doping, P-N junctions, diodes, and transistors.
- Strengthened the physical model of a transistor as an electrically controlled switch with no moving mechanical parts.
- Confirmed that physical **OFF/ON** language is easier to understand before translating circuit states into binary `0/1` labels.
- Built a working physical understanding of NOT, AND, OR, NAND, NOR, and XOR gate behavior.
- Connected series transistor paths with AND-style conditions and parallel paths with OR-style conditions.
- Understood a NAND gate as two series transistors that pull the output to ground only when both transistors are ON.
- Reinforced that circuit mechanisms should be understood before moving into arithmetic circuits or other applications.
- Identified animation and breadboard demonstrations as useful prerequisites when a concept depends on charge movement, voltage changes, feedback, or several interacting circuit paths.
- Stopped before SR latches and memory so feedback can be introduced visually and one mechanism at a time.

### Next Visual Prerequisite

Before continuing into memory, review an animation or breadboard demonstration of an **SR latch built from NAND gates**. Focus on how each gate's output feeds the other gate and allows the circuit to retain one of two stable states.

## Next Milestone

Continue from logic gates into feedback and memory, beginning with the SR latch. Teach the physical ON/OFF behavior first, then introduce state labels and binary abstractions only after the mechanism is clear.
