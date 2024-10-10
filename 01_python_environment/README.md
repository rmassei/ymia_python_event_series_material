# Python environments for image analysis
### Speaker: Dr Riccardo Massei

### What do I need to run this training?

A Conda package and environment manager such as miniconda or miniforge.
To install miniforge, follow the instructions [here](https://github.com/conda-forge/miniforge).

**IMPORTANT** - Please, give a look to the Anaconda’s terms of service and read [**"Is Conda Free?"**](https://www.anaconda.com/blog/is-conda-free) to understand if the conda-compatible packages in the <code>default</code> channel and Anaconda Distribution are free to use in your specific case.


### Which image data can I use?
Examplary images can be downloaded at this [link](https://hub.knime.com/knime/spaces/Life%20Sciences/Image_Processing/KNIME%20Executors%20on%20HPC/cell%20segmentation%20usecase/hcs-data~RRjAB-IH5X_gCloD/).


## Step-by-step guide to CUDR (create, use, delete and re-create) an environment

**Before Starting**: Download the JN "2024_ymia_basic_data_processing" in 02_JN and part of the data!
Move in that folder using the terminal (which is always cool and make you look professional)-> [CLI cheat sheet](https://www.git-tower.com/blog/command-line-cheat-sheet/)

---
1) Open your terminal and check if conda is correctly installed. You can do this by typing:

<code>
conda --version
</code>

A version number should appear if this was done correctly. Otherwise, you can check again 
using the miniconda/miniforge terminal (search "miniconda" or "miniforge" in your search bar, a terminal bar should appear)

 ---
2) Create a new environment with the necessary packages by typing:

<code>
conda create -n py_imana python=3.8 scikit-image
matplotlib
microfilm
notebook
</code>

Wait for conda to create the environment

---
3) Activate your environment. Type in your terminal.

<code>
conda env list

conda activate py_imana
</code>

The CLI should change from  <code>(base)</code> to <code>(py_imana)</code>

---
4) Start the Jupyter notebook in your browser by typing in the terminal:

<code>
jupyter notebook
</code>

Navigate in the browser and open the JN "2024_ymia_basic_data_processing".

---
5) Run the analysis and save the result. Close the JN and go back to the terminal.

---
6) Export the environment in an .yml file by typing:

<code>
conda env export > py_imana_env.yml
</code>

save this file in the folder

---
7) Move back to the base environment by typing:

<code>
conda activate base
</code>

delete the othet environment by typing:

<code>
conda env remove --name py_imana_env.yml
</code>

---
8) Now you can try to recreate the old environment by typing:

<code>
conda env create -f py_imana_env.yml
</code>

---
9) **Start again from point 4 and check if the analysis is the same!**

---
We thank Dr Robert Haase for this exercise inspired from his [Bio-image Analysis Notebooks](https://haesleinhuepf.github.io/BioImageAnalysisNotebooks/intro.html)

## Useful Links
- [Conda Cheatsheet 1](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf)
- [Conda Cheatsheet 2](https://docs.conda.io/projects/conda/en/latest/user-guide/cheatsheet.html)
