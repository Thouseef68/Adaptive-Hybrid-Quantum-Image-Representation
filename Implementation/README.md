# Implementation

Implementation
Platform and Tools

Platform: IBM Quantum

Quantum Framework: Qiskit

Programming Language: Python

Simulation Type: Statevector and QASM simulators

Simulation-based implementation is used due to current quantum hardware limitations, which is standard practice in quantum image processing research.

Implementation Strategy
Step 1: Classical Preprocessing

Load medical or SAR image

Convert to grayscale

Normalize pixel values

Resize image to 2×2 or 4×4

Step 2: Implementation of Existing Methods
FRQI (Baseline Method)

Encode pixel positions using quantum superposition

Encode pixel intensity using rotation gates

Simulate quantum circuit

Record qubit count and circuit complexity

NEQR (Reduced Implementation)

Encode pixel values in binary form

Use fewer intensity qubits for reduced complexity

Simulate and record resource usage

Other methods (NAQSS, QUALPI, SQR) are studied theoretically and compared using literature-based metrics.

Step 3: Implementation of Proposed AHQIR

Analyze image regions classically

Apply FRQI encoding to low-detail regions

Apply reduced NEQR encoding to high-detail regions

Combine encodings into a single hybrid quantum image state

Simulate the hybrid circuit

Step 4: Evaluation

All methods are evaluated using the same input images and simulation environment.

Evaluation Metrics:

Number of qubits

Gate complexity

Circuit depth

Reconstruction accuracy

Output

Quantum image state representation

Comparative performance analysis between existing methods and AHQIR

Demonstration of improved balance between accuracy and resource usage

Summary

The implementation follows a fair, simulation-based comparison framework, ensuring that improvements observed in AHQIR are due to the adaptive hybrid strategy rather than differences in input or platform.
