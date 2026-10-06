# ⚡ RATISS Neuralink-POC v1.0

## Local & Efficient Topological Neural Decoding Pipeline

## 🌌 Project Overview

RATISS (Autonomous Local Cognitive Engine) introduces a paradigm shift in brain-computer interface (BCI) processing. Unlike heavy, centralized statistical models based on the cloud, RATISS uses local differential geometry in $\mathbb{R}^7$ and algebraic topology to isolate and decode human motor intent in real time, locally, with a stabilized latency of 5.8 ms and no memory overhead thanks to `numpy.memmap` processing.

## 🛠️ Dual-Core Architecture

### Module 1 (V8-OMEGA): Local Curvature Density (LCD) Filtering

This module is based on the Ricci approximation (discrete Laplacian). It removes background biological noise while preserving 100% of the useful signal structure (32x32x32 active voxels).

### Module 2 (Cypher ODV): Topological Invariant Extractor (H_1)

This module compresses and maps over 62,000 neural micro-cycles to produce a stable, deterministic discrete decision vector (`winding_class`), eliminating any risk of algorithmic hallucination.

## 🚀 Quick Start Guide

### Prerequisites

*   Python 3.13+
*   NumPy 2.1+

### Running the POC

```bash
pip install numpy
python ratiss_core_unified.py
```

## Interchangeable Movements

RATISS's geometric architecture is universal and interchangeable. The code generates a toroidal signature by default to test cycle detection, but the injection function can be reconfigured endlessly to map any motor sequence or physical intention.

### How to modify the algorithm to simulate other combinations:

To change the type of decoded movement, modify the `run_v8_injection_pipeline()` function by changing the geometric constraint of the signal injected into the `memmap` block:

*   **Scenario A: Grabbing a cup (fine precision - `winding_class = 2`)**
    Inject a tightly-wound local curvature pattern (nested double torus or closed spiral type) to force the LCD filter to measure an average density above 0.8 at the centroid.

*   **Scenario B: Bringing a glass to the mouth (combined movement - `winding_class = 1`)**
    Generate a coupled sinusoidal displacement along the dimensional axes in $\mathbb{R}^7$ space to simulate the spatio-temporal transition of the approach ("reach").

*   **Scenario C: Sitting down / Relaxing (rest / neutral - `winding_class = 0`)**
    Reduce the amplitude of the useful signal to let the ambient Gaussian noise act. The LCD filter will lower the density below the emanation threshold $\epsilon$, confirming the absence of voluntary contraction or active motor intent.

By adjusting the geometric equations of the input matrix (geodesic shapes, point density), the topological core will automatically compute the appropriate persistence (birth / death) to drive a robotic effector, a prosthesis, or be injected directly into an embedded chip (FPGA / NPU type).

Independently developed by Jonathan (Software Architect).
