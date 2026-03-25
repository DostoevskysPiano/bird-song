# Bird Song: Spatiotemporal Acoustic Manifold

A real-time, web-based generative sculpture that transforms complex audio signals into 3D spatial structures. This project is a technical implementation of the **Spatiotemporal Acoustic Manifold** concept, inspired by the work of [Lucio Arese](https://www.lucioarese.net/) and his "Seeing Birdsong" (Visual Birds) series.

## 🎨 Inspiration: The Arese Methodology

This tool adopts Lucio Arese’s philosophy of **"Synesthesia by Design."** It moves beyond simple frequency-to-height mapping used in traditional spectrograms. Instead, it treats sound as a high-dimensional data source that can be "unfolded" into a geometric sculpture.

Bird songs contain dense mathematical fingerprints that define their species and individual identity. By mapping these features to a 3D manifold, we can see the **vocal trajectories** and **structural architecture** hidden within the sound.

## 🧬 Advanced Timbral Analysis

While pitch (frequency) and volume (amplitude) are easily visualized, **Timbre** is difficult to see. This tool uses **Mel-Frequency Cepstral Coefficients (MFCCs)** to extract and analyze the specific parts of timbre:

| Dimension | Analysis Target | Acoustic Property |
| :--- | :--- | :--- |
| **X-Axis (Red)** | **Spectral Tilt** | The "brightness" or "darkness" (energy balance) across the spectrum. |
| **Y-Axis (Green)** | **Spectral Flux** | The rate of change in the spectrum, highlighting rhythmic "strikes" and note onsets. |
| **Z-Axis (Blue)** | **Texture Identity** | The "fingerprint" of the sound. This uses MFCCs to distinguish between an "Oooo" vs. an "Aaaa" or a violin vs. a bird call. |

### The Manifold Learning Approach
Sound data is high-dimensional. Every snapshot of audio contains hundreds of frequency bins. This tool performs a form of **Dimensionality Reduction**. Similar to the Principal Component Analysis (PCA) used by Arese, this collapses complex descriptors into a 3D coordinate system where:
- **Closer points** share similar timbral textures.
- **Arcs and curves** represent the evolution of a sound's "identity" over time.

## 🛠 Technical Stack
- **Three.js**: WebGL rendering for the volumetric manifold.
- **Web Audio API**: Real-time FFT and MFCC extraction.
- **Mel Filterbank**: Non-linear frequency scaling that mimics human/avian hearing.

## 🚀 Quick Start
1. Open `index.html` in a modern browser.
2. Click **"Initiate Restored Manifold"** to start the analysis.
3. Observe how different sound sources (voice, music, or nature recordings) create unique 3D "fingerprints."
