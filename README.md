# devcontainer_template

This repository is a template to use as a base when starting new projects that make use of [devcontainers](https://code.visualstudio.com/docs/devcontainers/containers). It contains a [Dockerfile](./Dockerfile.base) which can be modified (comment/ comment out, etc) to enable different Python development environments: using MATLAB exported libraries with an official [MATLAB base image](https://www.mathworks.com/help/cloudcenter/ug/matlab-container-on-docker-hub.html), setting up [uv](https://github.com/astral-sh/uv) for managing dependencies or [miniconda](https://docs.anaconda.com/miniconda/).

## Getting started

Open (clone) the repository with VSCode and `CTRL+SHIFT+P` to open the command palette and select `devcontainers: Reopen in Container`.

### Setting up the development environment from within the container

#### Using uv

Once inside the container, set up a new conda environment with the necessary dependencies:

```bash
uv sync
```

#### Using conda

Once inside the container, set up a new conda environment with the necessary dependencies:

```bash
conda init zsh
```

Create and install dependencies using the `environment.yml` file:

```bash
conda env create -f environment.yml
```

And then activate it using the name specified in the `environment.yml` file:

```bash
conda activate conda-env
```
