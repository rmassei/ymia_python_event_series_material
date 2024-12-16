## Requirements for the workshop
Please follow these instructions before participating in the workshop.
*	Install miniforge for example by following these instructions: https://biapol.github.io/blog/mara_lampert/getting_started_with_mambaforge_and_python/readme.html (just the first part about Installation of miniforge) 
*	Start miniforge
*	Set up a python environment with some basic libraries
```
conda create -n omero -c conda-forge omero-py ipykernel matplotlib numpy pip
```
*	Activate the omero environment
```
conda activate omero
```
*	Install ezomero and juypter labs (more information about installing jupyterLab can be found here https://jupyterlab.readthedocs.io/en/4.2.x/getting_started/installation.html)
```
pip install ezomero
pip install jupyterlab
python -m ipykernel install --user --name=omero
```
*	Optional (to upload data) 
  *	Prepare sample data to upload to OMERO
  *	Install OMERO.insight: https://www.openmicroscopy.org/omero/downloads/

## Use this repository
Clone to your local computer and open the notebooks in `nbs` with jupyter lab:

Open Miniforge prompt
```
conda activate omero
jupyter lab
```
