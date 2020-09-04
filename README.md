# hackathon-2020-binder-template


## Run the notebook on Binder

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ec-better/hackathon-2020-binder-template/master?urlpath=lab)

## Using this template

### Setting the conda environment and the Jupyter kernel to run the notebook

The conda environment and associated kernel is defined in the file `environment.yml`.

The template provides an minimum set of python modules to run the template notebook example.

```yaml
name: env_better
channels:
  - conda-forge
  - terradue
dependencies:
  - ipykernel
```

**Don'ts**

- Don't change the environment name, leave `env_better`
- Don't remove the `ipykernel` dependency

Below a real-life example:

```yaml
name: env_better
channels:
  - conda-forge
  - terradue
dependencies:
  - cioppy
  - gdal
  - geopandas
  - numpy
  - matplotlib
  - pillow
  - ipykernel
```
