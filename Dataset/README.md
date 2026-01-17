# Dataset

6.Dataset Description
To comprehensively evaluate the effectiveness, robustness, and generalizability of the proposed Adaptive Hybrid Quantum Image Representation (AHQIR), three heterogeneous and application-relevant datasets are selected. These datasets are deliberately chosen to represent distinct imaging modalities with fundamentally different characteristics, thereby validating the adaptability of the proposed framework across diverse real-world scenarios. The selected datasets include medical imaging data and synthetic aperture radar (SAR) imagery, each posing unique challenges for quantum image representation.
6.1Brain Tumor MRI Dataset
Dataset Overview
The first dataset consists of brain tumor magnetic resonance imaging (MRI) scans, which are widely used in medical diagnosis and treatment planning. MRI images are grayscale images characterized by smooth intensity variations, high spatial correlation, and subtle contrast differences between healthy tissue and pathological regions. Preserving these intensity variations is crucial, as even minor information loss can significantly affect diagnostic accuracy.
Motivation for Selection
Brain tumor MRI images are selected due to their high sensitivity to information loss. Unlike generic natural images, medical images demand precise intensity preservation and low reconstruction error. This makes them an ideal benchmark for evaluating how well a quantum image representation method preserves critical image information under quantum encoding and measurement constraints.
Image Characteristics
	•	Modality: Grayscale MRI
	•	Bit depth: 8-bit intensity resolution
	•	Texture: Smooth regions with localized high-contrast tumor areas
	•	Noise: Low to moderate acquisition noise
	•	Image size: Original images vary in resolution and are resized for quantum feasibility
Preprocessing for Quantum Encoding
Prior to quantum encoding, the MRI images undergo the following preprocessing steps:
	1.	Conversion to grayscale (if necessary)
	2.	Intensity normalization to the range [0,1]
	3.	Resizing to quantum-compatible dimensions 2 \times 2, 4 \times 4, and 8 \times 8
	4.	Adaptive thresholding for saliency detection (used by AHQIR)
These preprocessing steps ensure compatibility with position qubit encoding while preserving diagnostically relevant regions.
6.2 NASA Synthetic Aperture Radar (SAR) Dataset
Dataset Overview
The second dataset comprises NASA SAR images, which are widely used in earth observation, environmental monitoring, oceanography, and terrain analysis. SAR images are fundamentally different from optical images, as they are generated using microwave signals and contain complex backscatter information.
Motivation for Selection
NASA SAR imagery is selected to evaluate the performance of AHQIR on high-frequency, noise-dominated images. SAR images are particularly challenging for quantum image representation due to:
	•	Speckle noise
	•	High dynamic range
	•	Nonlinear backscatter intensity distribution
These characteristics make SAR images a rigorous test case for assessing scalability, robustness, and information preservation.
Image Characteristics
	•	Modality: Grayscale SAR
	•	Texture: Highly textured with speckle noise
	•	Contrast: High local intensity variations
	•	Noise: Multiplicative speckle noise
	•	Spatial patterns: Complex geometric and terrain-dependent features
Preprocessing for Quantum Encoding
The NASA SAR images are preprocessed as follows:
	1.	Logarithmic intensity normalization to compress dynamic range
	2.	Noise smoothing using light filtering (classical preprocessing)
	3.	Resizing to 2^n \times 2^n resolutions
	4.	Adaptive thresholding to isolate strong backscatter regions

These steps reduce redundancy and enhance the effectiveness of adaptive quantum encoding.
6.3.ICEYE SAR Dataset
Dataset Overview
The third dataset consists of ICEYE SAR images, obtained from a commercial small-satellite SAR constellation. ICEYE imagery represents a modern, high-resolution SAR dataset, offering finer spatial resolution and more complex scattering patterns compared to traditional SAR datasets.
Motivation for Selection
ICEYE SAR data is selected to demonstrate the practical relevance and novelty of the proposed AHQIR framework. Unlike legacy SAR datasets, ICEYE images capture detailed urban, maritime, and infrastructure features, making them particularly suitable for evaluating scalability and real-world applicability of quantum image representation methods.
Image Characteristics
	•	Modality: High-resolution SAR
	•	Spatial resolution: Sub-meter to meter-level
	•	Texture: Dense high-frequency structures
	•	Noise: Speckle and sensor-induced artifacts
	•	Application domains: Urban mapping, maritime surveillance, disaster monitoring
Preprocessing for Quantum Encoding
ICEYE SAR images undergo the following preprocessing steps:
	1.	Radiometric normalization
	2.	Contrast enhancement
	3.	Spatial downsampling for quantum feasibility
	4.	Adaptive thresholding to identify dominant scattering regions
These preprocessing steps ensure that only information-rich regions are encoded into quantum states, significantly reducing encoding overhead.

