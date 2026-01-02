# Implementation

This folder will contain Qiskit-based simulation notebooks for implementing existing and proposed methods.
Proposed Method: Adaptive Hybrid Quantum Image Representation (AHQIR)
Motivation

Existing quantum image representation techniques use a single fixed encoding strategy for the entire image. This leads to inefficient use of quantum resources because different regions of an image do not require the same level of precision. High-detail regions need accurate encoding, while background or low-detail regions can be represented using simpler encodings.

To address this limitation, this project proposes a novel Adaptive Hybrid Quantum Image Representation (AHQIR).

Core Idea of AHQIR

The key idea of AHQIR is to adaptively combine multiple quantum image representation techniques based on image characteristics.

Adaptive Strategy

Low-detail regions → encoded using FRQI

High-detail regions → encoded using reduced-bit NEQR

The encoded regions are combined into a single hybrid quantum image state

This adaptive hybrid strategy reduces quantum resource usage while maintaining image accuracy.

AHQIR Workflow (Aligned with Architecture)

Input classical grayscale image (medical or SAR)

Perform classical preprocessing and region analysis

Select appropriate encoding strategy for each region

Construct hybrid quantum image representation

Apply quantum image operations if required

Evaluate performance and compare with existing methods

Advantages of AHQIR

Optimized qubit usage compared to NEQR

Higher accuracy than FRQI

Flexible and scalable representation

Better support for quantum image operations

Suitable for simulation-based implementation

Novelty

The novelty of AHQIR lies in its adaptive and hybrid encoding mechanism, which dynamically selects quantum image representations instead of applying a single fixed method across the entire image.
