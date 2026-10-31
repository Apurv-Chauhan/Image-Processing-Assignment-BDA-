# Image Processing Assignments — First Three Deliverables

This package contains the first three items in the supplied IPP assignment sheet.

## Package contents

- `Assignment_1_Practical_File_1/Practical_File_1.ipynb` — all 10 Lab 3 & Lab 4 assignment programs.
- `Assignment_1_Practical_File_1/images/` — the six bundled input images used by Practical File 1.
- `Assignment_2_Practical_File_2/Practical_File_2.ipynb` — all six detailed Lab 9 assignment problems (not 10 invented problems), including sliding-window GLCM features computed at every pixel.
- `Assignment_2_Practical_File_2/images/` — bundled real sample and synthetic input images plus generated visual results.
- `Assignment_3_Workflow_Diagram/Google_Maps_Workflow.png` — high-resolution workflow diagram.
- `Assignment_3_Workflow_Diagram/Google_Maps_Workflow.pdf` — printable diagram.
- `Assignment_3_Workflow_Diagram/Google_Maps_Workflow.dot` — editable Graphviz source.

## Run the notebooks

Use Python 3.10 or newer. Open each notebook from its own assignment folder and run **Kernel → Restart Kernel and Run All Cells**. Input assets are referenced using relative paths from the notebook folder; internet access is not required.

Install dependencies if they are not already available:

```bash
python -m pip install opencv-python pillow numpy matplotlib scikit-image scikit-learn scipy jupyter nbclient
```

## Image provenance and interpretation

Practical File 1 uses bundled, locally generated sample images for each required filename. Practical File 2 uses the local `scikit-image` sample `rocket` image for outdoor edge detection and `camera` sample for the noise experiment. The document scan, cityscape, texture mosaic and diseased-looking plant example are synthetic teaching images, generated specifically to make the required experiments repeatable without broken or unavailable downloads. The synthetic plant segmentation is not clinical or agricultural diagnosis and does not establish real-world detection accuracy.

## Compression accounting

The RLE and Huffman comparison reports theoretical payload plus stated compact headers. It does not report actual PNG/JPEG file sizes or Python in-memory object sizes. The exact assumptions are documented in the Practical File 2 notebook.

## Submission notes from the supplied Excel sheet

- Workflow diagram: upload the Google Maps flowchart.
- Practical File 1 and Practical File 2: the sheet requests notebook uploads and a **publicly visible GitHub link**. Create a public repository (or public repository folder) containing the notebooks and supporting `images/` folders, then submit the resulting URL in the institute's designated form / submission location.
- The Excel sheet does not show a populated deadline in the supplied cells.

This ZIP contains the files; it does not publish them to GitHub or submit them to the institute.
