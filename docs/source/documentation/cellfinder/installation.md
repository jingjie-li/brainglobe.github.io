# Requirements

`cellfinder` should run on most machines, but for routine use on large datasets, you will need a fairly high-powered computer (see the guide to [Speeding up cellfinder](/documentation/cellfinder/troubleshooting/speed-up) for details).

Using an NVIDIA GPU will speed up cell classification considerably.
See [setting up your GPU](/documentation/setting-up/gpu) for details.

`cellfinder` uses `brainreg` for atlas registration, and the hardware requirements for `brainreg` depend on the atlas (and in particular, the resolution) you want to use.
Most machines (including laptops) will be able to use most of the atlases, but some atlases (such as the 10&mu;m mouse atlases) may need up to 50GB of RAM.

## Installation

To use cellfinder, you will need to have Python on your machine.
Your machine may already have Python installed, but we recommend installing miniconda.
See [Using conda](/documentation/setting-up/conda) for details.

### Installing the `cellfinder` package

You can use `pip` from inside your activated Python environment to install the `cellfinder` package directly.
Make sure to install version `1.0.0` or later!

```bash
pip install cellfinder>=1.0.0 # Run this if you only want the Python API (for use in scripts)
pip install cellfinder[napari]>=1.0.0 # Run this if you want to install the API and the napari plugin
```

### Installing BrainGlobe Atlases

To install download BrainGlobe atlases in advance, please see the guide to [the BrainGlobe Atlas API command-line interface](/documentation/bg-atlasapi/usage/command-line-interface).

### Installing `brainmapper`

The `brainmapper` workflow combines the `cellfinder` and `brainreg` packages into a single workflow, providing full-brain registration and cell detection in one command.
You can read more about it [on this page](../brainglobe-workflows/brainmapper/index.md).
