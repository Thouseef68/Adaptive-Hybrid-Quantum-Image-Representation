# Existing Methods

This folder documents existing quantum image representation techniques such as FRQI, NEQR, NAQSS, and QUALPI used for comparison.
Existing Quantum Image Representation Methods

Quantum Image Representation (QIR) methods define how classical image information such as pixel position and intensity is encoded into quantum states. Several techniques have been proposed in the literature, each with specific advantages and limitations. This project studies the following existing methods as baselines for comparison.

1. Flexible Representation of Quantum Images (FRQI)

FRQI is one of the earliest quantum image representation models. It encodes pixel positions using quantum superposition and represents pixel intensity using the rotation angle of a single qubit.

Advantages:

Requires fewer qubits

Simple and intuitive encoding

Suitable for small-scale simulation

Limitations:

Limited accuracy in pixel representation

Complex measurement and reconstruction

FRQI is efficient but not suitable for high-detail images.

2. Novel Enhanced Quantum Representation (NEQR)

NEQR improves upon FRQI by encoding pixel intensity values directly in binary form using multiple qubits.

Advantages:

Exact pixel value representation

Higher reconstruction accuracy

Limitations:

High qubit requirement

Increased circuit depth and gate complexity

NEQR provides accuracy at the cost of quantum resources.

3. Normal Arbitrary Quantum Superposition State (NAQSS)

NAQSS supports flexible image representation using arbitrary quantum superposition states.

Advantages:

Supports complex image structures

Flexible encoding

Limitations:

High computational complexity

Difficult to scale for practical implementation

4. QSMC / QSNC Models

Quantum States for M Colors and N Coordinates (QSMC/QSNC) extend quantum image representation to multi-color images.

Advantages:

Supports multi-channel and color images

Limitations:

Requires a large number of qubits

High encoding and decoding complexity

5. Quantum Log-Polar Image Representation (QUALPI)

QUALPI represents images using log-polar coordinates, making it suitable for rotation-invariant processing.

Advantages:

Effective for geometric transformations

Rotation-invariant representation

Limitations:

Complex encoding process

High quantum resource usage

Summary of Limitations

Although existing quantum image representation techniques are effective in specific scenarios, they all rely on a single fixed encoding strategy for the entire image. This leads to inefficient use of quantum resources, especially for images containing both low-detail and high-detail regions.

These limitations motivate the need for a novel adaptive and hybrid quantum image representation, which is addressed by the proposed AHQIR method.
