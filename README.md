[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Rohithocean/Sea_Level_Data_Analysis/main)

# Sea_Level_Data_Analysis  

* [Installation](#installation)
  * [Try it right now on the cloud for free](#try-it-right-now-on-the-cloud-for-free)
  
# Installation
## Try it right now on the cloud for free
[Click here](https://mybinder.org/v2/gh/Rohithocean/Sea_Level_Data_Analysis/main) to launch a pre-configured notebook environment on the cloud platform provided freely by the  [binder project](https://mybinder.org). Use the Chrome browser if you have trouble loading that page. Refresh the page if loading fails.

If the page is loaded successfully, you should see a [Jupyter notebook](https://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/What%20is%20the%20Jupyter%20Notebook.html) interface. Then, click on the first notebook to get started. Jupyter combines Python code, execution results, plots, custom texts, and even Latex formulas in a single page. Besides using the Jupyter program, you can also view the static notebook on GitHub (e.g the first notebook).

Please follow [Jupyter official doc](https://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/Notebook%20Basics.html) to learn basic operations. The most important command is Shift+Enter to execute the current code block.

## Pyferret
The PyFerret program and Python module from NOAA/PMEL.
See https://ferret.pmel.noaa.gov/Ferret/ for more information about Ferret and PyFerret.

### Ferret/PyFerret Documentation
For more information on using PyFerret, see the Ferret and PyFerret documentation under https://ferret.pmel.noaa.gov/Ferret/

Information about the Ferret email users group, and archives of past discussions from the group (which should be searched prior to sending a question to the email users group) can be found at https://ferret.pmel.noaa.gov/Ferret/email-users-group/

### Jupyter/iPython notebook
The latest ferretmagic module from Patrick Brockmann for using PyFerret with the iPython notebook can be obtained using pip install ferretmagic, or see https://pypi.org/project/ferretmagic/. Note that this only installs the ferretmagic module for PyFerret; it does not install PyFerret.

### Anaconda Installation - Linux, OS X, and Windows 10/bash
Note: If you are updating an existing conda installation of PyFerret, you should only need to update the existing installation using conda update -n FERRET pyferret (assuming FERRET is the name of the environment used). Or you can install under a new environment name if you wish to keep multiple versions of PyFerret.
You may first need to update conda itself conda update conda; conda update --all before updating PyFerret. If you are using a Python 2.x version of miniconda, you will need to install the Python 3.x version of miniconda and then install PyFerret in that version of miniconda in order to get the latest version of PyFerret.

Download and install minicoda for your system from https://docs.conda.io/en/latest/miniconda.html Note that Windows 10 bash must use the Linux version! Install the Python 3.x version of minicoda to get the latest versions of PyFerret. (Although PyFerret works with ether Python 2.x or Python 3.x, Python 2.x itself will no longer be supported after 2019.) Allow miniconda to add its initialization code to your start-up scripts (e.g., $HOME/.bashrc) and open a new login window when the installation is complete. One thing with will do is add the conda bin directory to your path of directories to search for executables.

Execute the following command on the terminal to install pyferret as well as ferret_datasets (the default Ferret/PyFerret datasets) into conda:

conda create -n FERRET -c conda-forge pyferret ferret_datasets --yes
