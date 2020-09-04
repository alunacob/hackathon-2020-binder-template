# hackathon-2020-binder-template


## Run the notebook on Binder

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ec-better/hackathon-2020-binder-template/master?urlpath=lab)

## Using this template

This software repository contains a template for running a notebook on Binder.

To create your own repository:

- create a **public** repository on GitHub 
- copy the contents of this repo in that repository 
- update the `environment.yml` with the conda packages required to run the notebook(s)
- create one or more notebooks to support the BETTER Hackathon 2020 activities
- update the `README.md` file to update the Binder badge repository URL:

`https://mybinder.org/v2/gh/ec-better/{your repository name}/master?urlpath=lab`

### Setting the conda environment and the Jupyter kernel to run the notebook

The conda environment and associated kernel is defined in the file `environment.yml` under the `.binder` folder.

The template provides an minimum set of python modules to run the template notebook example.

```yaml
name: env_better
channels:
  - conda-forge
  - terradue
dependencies:
  - ipykernel
```

Add any additional conda dependency with a new line after ` - ipykernel`, e.g.:

```yaml
name: env_better
channels:
  - conda-forge
  - terradue
dependencies:
  - ipykernel
  - gdal
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

## Understanding the contents of the `.binder` folder

The `.binder` folder contains a docker file that sets the conda environment and associated kernel.

If you need additional steps, you can create a bash script named `postBuild`. There's an example here: https://github.com/binder-examples/jupyterlab/blob/master/binder/postBuild

More info here: https://mybinder.readthedocs.io/en/latest/using.html#share-computational-work-or-papers

**Don'ts**

- Don't change docker file

## Computing resources

Binder runs the experiments for free with computing resources provided by Google Cloud, OVH, GESIS Notebooks and the Turing Institute.
The notebook must target a computing environment with 2 GB of RAM

After some inactivity, the docker container is culled. 

## Additional guidelines

There are a few knowledge base entries here https://knowledge.terradue.com/display/ELLIP/Ellip+Notebooks+user+guides showing how to common tasks with a Notebook 
