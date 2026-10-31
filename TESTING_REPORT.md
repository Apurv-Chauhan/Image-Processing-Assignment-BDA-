# Execution and Quality Assurance Report

| Deliverable | Code execution | Visual outputs | Status |
|---|---|---|---|
| Practical File 1 | All 11 code cells executed; no exceptions | Inline images rendered and captured; `output_gray.jpg` saved | **PASS** |
| Practical File 2 | All 7 code cells executed; no exceptions | Edge, noise, compression, JPEG, GLCM and plant segmentation plots generated | **PASS** |
| Google Maps workflow | Not a notebook; Graphviz generated PNG and PDF | PNG inspected; one-page PDF rendered and inspected | **PASS** |

## Key verification results

- Practical File 1: `scene.jpg` reported height 480, width 640, 3 channels, `uint8`; the central crop is exactly 200 × 200; MSE was finite (35.2086) for equal-sized 256 × 256 grayscale inputs.
- Practical File 1: the OpenCV desktop-window branch is included for Windows/GUI use. The execution environment for this test was headless, so the inline Matplotlib image was displayed instead; the native desktop window itself was not exercised here.
- Practical File 2: RLE reconstruction matched the source pixels exactly. Original size was 786,432 bits; RLE was 35,257 bits (95.52% reduction); Huffman payload plus stated header was 138,368 bits (82.41% reduction). These are theoretical bit counts under the assumptions in the notebook, not actual output-file sizes.
- Practical File 2: JPEG-style results were finite and showed expected quality degradation as quantisation became more aggressive: low PSNR/SSIM 35.757 dB / 0.95092; medium 33.420 dB / 0.93130; high 30.248 dB / 0.88963.
- Practical File 2: per-pixel GLCM feature array shape was (76,800, 3); texture segmentation returned exactly 3 clusters. Multi-feature K-means also returned exactly 3 clusters. The synthetic leaf example transparently reports overlap between spot-like and healthy pixels rather than claiming diagnostic accuracy.
- Diagram: high-resolution PNG dimensions are recorded in the build check; PDF is one page and was rendered for visual verification.

All code cells in both final notebooks were executed in order using the Python 3 kernel with no notebook exceptions. The bundled notebooks include captured outputs from those runs.
