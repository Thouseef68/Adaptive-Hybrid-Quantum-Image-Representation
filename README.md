# Adaptive Hybrid Quantum Image Representation (AHQIR)

Adaptive Hybrid Quantum Image Representation (AHQIR) uses classical intensity thresholding to select pixels, then applies controlled intensity rotations only at the selected positions. It is evaluated in Qiskit simulation on brain MRI and SAR images.

## Status

- **Manuscript:** under review.
- **Preprint (Research Square):** https://doi.org/10.21203/rs.3.rs-9250112/v1
- **Archived version (Zenodo):** https://doi.org/10.5281/zenodo.24100831

## Method

AHQIR keeps the position register in a full uniform superposition. It reduces the number of controlled-rotation instructions, not the position-qubit count or the support of the position state.

## Results (simulation, 4×4 images)

Experiments used 800 sampled brain MRI images and 1,160 SAR images, downsampled to 4×4. All results are from Qiskit simulation.

| Metric (vs. FRQI) | MRI | SAR |
|---|---|---|
| Logical gate-count reduction | 63.7% | 80.3% |
| Physical CX reduction (after transpilation) | 63.8% | 80.7% |

Physical CX counts (mean ± std): FRQI 384 for both; NEQR 1030.0 ± 187.3 (MRI) and 916.6 ± 248.5 (SAR); AHQIR 138.9 ± 32.6 (MRI) and 74.2 ± 39.8 (SAR).

These savings come with higher full-image reconstruction error, because non-selected pixels are reconstructed as zero.

## Limitations

- Results are for 4×4 images in simulation only. A supplementary scaling check used one representative image per modality at 4×4, 8×8, and 16×16.
- The per-selected-pixel gate cost grows with the number of position-qubit controls because no ancilla qubits are used. AHQIR reduces the prefactor, not the underlying exponential dependence on resolution.
- No physical-hardware or noise experiments were run.
- The intensity threshold is not a validated tumour or ship detector. Task relevance has not been assessed.

## Future Work

- Test larger images and ancilla-assisted multi-controlled gate synthesis.
- Evaluate on physical or noisy hardware.
- Assess task relevance (for example, downstream classification) on the selected regions.

## Citation

If you use this work, please cite the preprint or the Zenodo record above while the manuscript is under review.
