[![DOC](https://shields.mitmproxy.org/badge/docs-pdoc.dev-brightgreen.svg)](https://computational-cell-analytics.github.io/micro-sam/)
[![Conda](https://anaconda.org/conda-forge/micro_sam/badges/version.svg)](https://anaconda.org/conda-forge/micro_sam)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.7919746.svg)](https://doi.org/10.5281/zenodo.7919746)

# SegmentAnything for Microscopy

Tools for segmentation and tracking in microscopy build on top of [SegmentAnything](https://segment-anything.com/).
Segment and track objects in microscopy images interactively with a few clicks!

We implement napari applications for:
- interactive 2d segmentation (Left: interactive cell segmentation)
- interactive 3d segmentation (Middle: interactive mitochondria segmentation in EM)
- interactive tracking of 2d image data (Right: interactive cell tracking)

<img src="https://github.com/computational-cell-analytics/micro-sam/assets/4263537/d04cb158-9f5b-4460-98cd-023c4f19cccd" width="256">
<img src="https://github.com/computational-cell-analytics/micro-sam/assets/4263537/dfca3d9b-dba5-440b-b0f9-72a0683ac410" width="256">
<img src="https://github.com/computational-cell-analytics/micro-sam/assets/4263537/aefbf99f-e73a-4125-bb49-2e6592367a64" width="256">

If you run into any problems or have questions regarding our tool please open an issue on Github or reach out via [image.sc](https://forum.image.sc/) using the tag `micro-sam` and tagging @constantinpape.


## Installation and Usage

You can install `micro_sam` via conda:
```
conda install -c conda-forge micro_sam napari pyqt
```
You can then start the `micro_sam` tools by running `$ micro_sam.annotator` in the command line.

For an introduction in how to use the napari based annotation tools check out [the video tutorials](https://www.youtube.com/watch?v=ket7bDUP9tI&list=PLwYZXQJ3f36GQPpKCrSbHjGiH39X4XjSO&pp=gAQBiAQB).
Please check out [the documentation](https://computational-cell-analytics.github.io/micro-sam/) for more details on the installation and usage of `micro_sam`.


## Citation

If you are using this repository in your research please cite
- Our [preprint](https://doi.org/10.1101/2023.08.21.554208)
- and the original [Segment Anything publication](https://arxiv.org/abs/2304.02643)


## Related Projects

There are a few other napari plugins build around Segment Anything:
- https://github.com/MIC-DKFZ/napari-sam (2d and 3d support)
- https://github.com/JoOkuma/napari-segment-anything (only 2d support)
- https://github.com/hiroalchem/napari-SAM4IS

Compared to these we support more applications (2d, 3d and tracking), and provide finetuning methods and finetuned models for microscopy data.
[WebKnossos](https://webknossos.org/) also offers integration of SegmentAnything for interactive segmentation.


## Release Overview

**New in version 0.2.1 and 0.2.2**

- Several bugfixes for the newly introduced functionality in 0.2.0.

**New in version 0.2.0**

- Functionality for training / finetuning and evaluation of Segment Anything Models
- Full support for our finetuned segment anything models
- Improvements of the automated instance segmentation functionality in the 2d annotator
- And several other small improvements

**New in version 0.1.1**

- Fine-tuned segment anything models for microscopy (experimental)
- Simplified instance segmentation menu
- Menu for clearing annotations

**New in version 0.1.0**

- We support tiling in all annotators to enable processing large images.
- Implement new automatic instance segmentation functionality:
    - That is faster.
    - Enables interactive update of parameters.
    - And also works for large images by making use of tiled embeddings.
- Implement the `image_series_annotator` for processing many images in a row.
- Use the data hash in pre-computed embeddings to warn if the input data changes.
- Create a simple GUI to select which annotator to start.
- And made many other small improvements and fixed bugs.

**New in version 0.0.2**

- We have added support for bounding box prompts, which provide better segmentation results than points in many cases.
- Interactive tracking now uses a better heuristic to propagate masks across time, leading to better automatic tracking results.
- And have fixed several small bugs.


<!---
## Contributing

```
micro_sam <- library with utility functionality for using SAM for microscopy data
    /sam_annotator <- the napari plugins for annotation
```
-->
