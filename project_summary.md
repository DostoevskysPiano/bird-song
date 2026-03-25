# Project: Spatiotemporal Acoustic Manifold
**Objective:** To develop a web-based, real-time audio visualization system inspired by the "Visual Birds" and "Seeing Birdsong" series by [Lucio Arese](https://www.lucioarese.net/seeing-birdsong/).

## 1. Vision & Inspiration
The project aims to move beyond standard "volume-based" visualizers toward a **Generative Sculpture** model. Following Arese's philosophy, the goal is to transform audio—specifically complex signals like bird songs and music—into **spatial structures**. By treating time as a third dimension (the Z-axis), the system reveals the "hidden architecture" and "mathematical fingerprints" of sound.

## 2. Technical Evolution
Over the course of development, the system has evolved through several architectural phases:

*   **Phase 1: 2D FFT Manifold:** Initial experiments using 2D Canvas.
*   **Phase 2: 3D Grid & Cubic Lattice:** Transitioned to Three.js volumetric manifolds.
*   **Phase 3: Circular Neural Bundle:** Organic "nerve bundle" topology.
*   **Phase 4: Feature-Driven Vector Space:** Move to Feature Extraction (Entropy, Spread, Flux).
*   **Phase 5: Perceptual Cepstral Manifold:** Implementation of **MFCCs**.
*   **Phase 6: Calibrated Perceptual Manifold:** Refined mathematical model with **Exponentially Smoothed Auto-Scaling** and a **Noise Gate (Threshold: 0.1)**.

## 3. The Analytical Coordinate System (Full Reference)

| Dimension | Positive (+) Direction | Negative (-) Direction | Analysis |
| :--- | :--- | :--- | :--- |
| **X-Axis (Red)** | **Bright / High-Tilt** (Right) | **Dark / Bassy** (Left) | **Spectral Tilt:** Tracks global energy balance. |
| **Y-Axis (Green)** | **Stable / Pure** (Top) | **Impact / Strike** (Bottom) | **Rhythm/Flux:** Tracks note onsets and percussion. |
| **Z-Axis (Blue)** | **Sharp Curve / Vowel** (Front) | **Soft Curve / Wide** (Back) | **Texture Curvature:** Tracks the "identity" of the sound. |

## 4. Viewing Guide (Best Angles)
*   **To See "Timbre vs. Rhythm":** View the manifold from the **Side** (looking along the Blue Z-axis). This highlights how different textures strike the floor.
*   **To See "Timbre vs. Texture":** View the manifold from the **Top** (looking down the Green Y-axis). This reveals the 2D "fingerprint" map of the instrument's identity.
*   **To See "Rhythm vs. Texture":** View the manifold from the **Front** (looking down the Red X-axis). This shows how different vowel/texture types respond to rhythmic hits.

## 5. Key Mathematical Features
*   **MFCC Analysis:** Perceptual fingerprinting via Mel-scale filtering and Discrete Cosine Transform.
*   **Adaptive Auto-Zoom:** Uses Exponential Smoothing (Lerp) to ensure the manifold always fills the screen without jittering.
*   **Noise Gating:** RMS-based signal detection to keep the visualization clean during silence.

## 6. Simplified Concept Glossary
*   **Texture (Timbre + Envelope):** The core of the visualization. **Timbre** is the 'identity' of the sound (Piano vs. Violin), and **Envelope** is how that sound changes over time (Attack/Decay). The manifold shows 'Texture' by mapping how the identity of the sound morphs as it plays.
*   **MFCCs (Vocal Fingerprint):** If sound were a person, **Pitch** is their height, and **MFCC** is their face. It captures the unique "texture" that lets you identify a specific voice or instrument.
*   **Mel Scale (The Human Ruler):** A "zoomed-in" ruler. It stretches out the low notes (where we hear detail) and squishes the high notes (where we don't), so the math matches our ears.
*   **Spectral Entropy (Messiness Meter):** Measures how "tidy" a sound is. A pure whistle is tidy (Low Entropy); a cymbal crash is a mess (High Entropy).
*   **Manifolds (Uncrumpling the Paper):** Sound data is like a crumpled ball of paper. **Manifold Learning** is the math used to "uncrumple" it so we can see the logical map hidden inside.
*   **Spectral Leakage (Blurry Photos):** When a computer takes a "snapshot" of a sound, if the frequency is "between pixels," it bleeds into the ones next to it. This makes sharp sounds look "blurry" or "wide."
*   **Formants (The Mouth Shape):** The physical shape of the "container" the sound is in. It's what makes an "Oooo" sound different from an "Aaaa" even on the same note.
*   **Windowing (Fading the Edges):** A "Fade-In / Fade-Out" that happens 60 times a second to make the edges of sound chunks soft so the computer doesn't get distracted by the "chops."

## 7. Research & Learning Backlog

### Core Topics for Deep-Dive Research
*   **Manifold Learning:** Understand the theory of "embedding" high-dimensional data (like 1024 FFT bins) into lower-dimensional 3D spaces.
*   **Principal Component Analysis (PCA):** Arese uses this to collapse 13 MFCC dimensions into 3. How does the math determine which dimensions are "most important" in real-time?
*   **Psychoacoustics:** Study the **Mel Scale** and **Bark Scale** to understand why mapping frequencies non-linearly matches human hearing better than linear Hertz.
*   **Information Theory:** Research **Spectral Entropy**—the mathematical measure of "surprise" or "chaos" in a sound signal.
*   **Cepstral Analysis:** What is a "Quefrency"? Understand why the "Spectrum of a Spectrum" (the Cepstrum) is the gold standard for speech and bird-song recognition.

### Critical Investigation Questions
1.  **The Sine Wave Paradox:** Why does a "pure" sine wave often look "wide" or "noisy" to a Mel Filterbank? (Keywords: Spectral Leakage, Filter Overlap).
2.  **Windowing Functions:** How would applying a **Hamming** or **Hann** window to our raw audio buffer improve the sharpness of our manifold?
3.  **Dimensionality Reduction:** Can we replace our hard-coded MFCC selection with a real-time **PCA** algorithm to automatically find the best "Texture" axis for any given song?
4.  **Temporal Topology:** How does the speed of our history-shifting affect our ability to see "clusters" vs "arcs"?
5.  **Formant Extraction:** How can we better isolate the "vocal tract" shape of a bird song from its pitch?

---
*Updated: Tuesday, February 10, 2026*