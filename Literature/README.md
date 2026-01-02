# Literature

This folder contains research papers collected from IEEE, Springer, Elsevier, and MDPI related to quantum image representation and quantum image processing.

Literature Review (2020–Present)

Quantum Image Processing (QIP) is an emerging research area that studies how image information can be represented and processed using quantum computing principles. A fundamental requirement in QIP is an efficient Quantum Image Representation (QIR), which determines how pixel positions and intensity values are encoded into quantum states. Over the last few years, several QIR techniques have been proposed and analyzed in IEEE, Springer, MDPI, and ACM publications.

One of the earliest and widely used models is the Flexible Representation of Quantum Images (FRQI). FRQI encodes pixel positions using quantum superposition and represents pixel intensity using a rotation angle. Literature reports that FRQI is simple and requires fewer qubits, but it suffers from limited accuracy and measurement complexity. To address these limitations, Novel Enhanced Quantum Representation (NEQR) was introduced, which encodes pixel values directly in binary form. While NEQR improves accuracy, it significantly increases qubit usage and circuit complexity.

More advanced representations such as NAQSS, QSMC/QSNC, and SQR extend support to multi-channel or specialized images. However, recent studies highlight that these methods increase computational overhead and are difficult to scale. Similarly, Quantum Log-Polar Image Representation (QUALPI) enables rotation-invariant encoding and supports geometric transformations, but it requires complex encoding and higher quantum resources.

Recent application-based studies in medical imaging, image encryption, and SAR image analysis demonstrate the usefulness of quantum image representations in real-world scenarios. At the same time, these works continue to rely on existing QIR models and inherit their limitations. Research on quantum image operations such as geometric transformation, image flipping, and filtering further emphasizes that the efficiency of these operations strongly depends on the underlying image representation.

Due to current hardware limitations, most recent research adopts simulation-based implementation, with platforms such as IBM Quantum and Qiskit being widely used. These simulators enable fair comparison of different QIR techniques using metrics such as qubit count, gate complexity, and encoding efficiency.

From the literature, a clear research gap is identified: existing quantum image representation techniques apply a single fixed encoding strategy to the entire image, leading to inefficient use of quantum resources. To address this limitation, this project proposes a novel Adaptive Hybrid Quantum Image Representation (AHQIR) that combines the strengths of multiple QIR techniques. By adaptively selecting encoding strategies based on image characteristics, the proposed approach aims to achieve better balance between accuracy and quantum resource utilization while supporting quantum image operations.
