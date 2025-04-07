# Virtual Surround Sound (VSS) using Binaural Audio
This project simulates a 5.1 virtual surround sound field through **binaural audio processing**, allowing immersive playback over **headphones**. Using psychoacoustic cues like ITD (interaural time differences) and ILD (interaural level differences), the system creates spatial perception beyond typical stereo width.

## 🎧 Project Goal

To prototype a virtual surround experience using a stereo output format suitable for headphone listening, simulating surround speaker positions (L, R, C, LS, RS) with dry mono sources.

## 🛠️ Methodology

- A 5.1 multitrack input with mono stems representing five surround positions (L, R, C, LS, RS).
- Applied binaural spatialization using **measured HRIR data** from the SOFA-format dataset: `D2_HRIR_SOFA/D2_48K_24bit_256tap_FIR_SOFA.sofa`
- Used the HRIRs to **convolve** each virtual speaker source for accurate headphone-based spatial positioning.
- Combined the spatialized signals into a final stereo (binaural-style) mix for immersive playback.

## 🧪 Key Techniques

- SOFA HRIR convolution for direction-dependent filtering
- Interaural time and level difference simulation
- Pan law adjustments and center imaging
- Spatial summation for a natural-sounding surround image

## 📂 Dataset

- **HRIR Source**: `D2_48K_24bit_256tap_FIR_SOFA.sofa`
- **Format**: SOFA (Spatially Oriented Format for Acoustics)
- **Resolution**: 48 kHz, 24-bit, 256-tap FIR filters
- Used with np.convolve

## 🎯 Output

- A stereo (binaural-style) mix that mimics a surround speaker setup through headphones

🧠 **Designed for headphone playback.**  
Experience the best results using neutral headphones in a quiet listening environment.

## 📁 Files

- `VSS_clear_all_outputs.ipynb`: Cleaned notebook with full signal flow, spatial routing logic, and audio processing code.

> ⚠️ **Note:** Audio files are excluded due to GitHub's size limits. Please contact me for access or recreate using your own 5.1 sources with the code and mix instructions in the notebook.