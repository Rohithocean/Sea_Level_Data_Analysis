[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Rohithocean/Sea_Level_Data_Analysis/main)

# Sea_Level_Data_Analysis  

* [Installation](#installation)
  * [Try it right now on the cloud for free](#try-it-right-now-on-the-cloud-for-free)

## Try it right now on the cloud for free
[Click here](https://mybinder.org/v2/gh/Rohithocean/Sea_Level_Data_Analysis/main) to launch a pre-configured notebook environment on the cloud platform provided freely by the  [binder project](https://mybinder.org). Use the Chrome browser if you have trouble loading that page. Refresh the page if loading fails.

If the page is loaded successfully, you should see a [Jupyter notebook](https://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/What%20is%20the%20Jupyter%20Notebook.html) interface. Then, click on the first notebook to get started. Jupyter combines Python code, execution results, plots, custom texts, and even Latex formulas in a single page. Besides using the Jupyter program, you can also view the static notebook on GitHub (e.g the first notebook).

Please follow [Jupyter official doc](https://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/Notebook%20Basics.html) to learn basic operations. The most important command is Shift+Enter to execute the current code block.

## Pyferret Installation 
The PyFerret program and Python module from NOAA/PMEL.
See https://ferret.pmel.noaa.gov/Ferret/ for more information about Ferret and PyFerret.

### Ferret/PyFerret Documentation
For more information on using PyFerret, see the Ferret and PyFerret documentation under https://ferret.pmel.noaa.gov/Ferret/

Information about the Ferret email users group, and archives of past discussions from the group (which should be searched prior to sending a question to the email users group) can be found at https://ferret.pmel.noaa.gov/Ferret/email-users-group/

### Jupyter/iPython notebook
The latest ferretmagic module from Patrick Brockmann for using PyFerret with the iPython notebook can be obtained using pip install ferretmagic, or see https://pypi.org/project/ferretmagic/. Note that this only installs the ferretmagic module for PyFerret; it does not install PyFerret.

## Anaconda Installation - Linux, OS X, and Windows 10/bash

*Note: If you are updating an existing conda installation of PyFerret, you should
only need to update the existing installation using `conda update -n FERRET pyferret`
(assuming `FERRET` is the name of the environment used).
Or you can install under a new environment name if you wish to keep multiple versions 
of PyFerret.  
You may first need to update conda itself `conda update conda; conda update --all` 
before updating PyFerret.
If you are using a Python 2.x version of miniconda, you will need to install the 
Python 3.x version of miniconda and then install PyFerret in that version of miniconda
in order to get the latest version of PyFerret.*

Download and install minicoda for your system from
[https://docs.conda.io/en/latest/miniconda.html](https://docs.conda.io/en/latest/miniconda.html)
Note that Windows 10 bash must use the Linux version!
Install the Python 3.x version of minicoda to get the latest versions of PyFerret.
(Although PyFerret works with ether Python 2.x or Python 3.x,
Python 2.x itself will no longer be supported after 2019.)
Allow miniconda to add its initialization code to your start-up scripts (e.g.,
`$HOME/.bashrc`) and open a new login window when the installation is complete.
One thing with will do is add the conda bin directory to your path of directories 
to search for executables.

Execute the following command on the terminal to install `pyferret` as well as
`ferret_datasets` (the default Ferret/PyFerret datasets) into conda:
```shell
conda create -n FERRET -c conda-forge pyferret ferret_datasets --yes
```
(`FERRET` is the environment name where `pyferret` is installed.
You can change that to any name you like, such as `PyFerret`.)

To start using PyFerret, execute the following command:
```shell
conda activate FERRET
```
(replacing `FERRET` with whatever environment name you used.)

Once you are done working with PyFerret you can leave this environment,
if you wish, with the command:
```shell
conda deactivate
```

As mention above `FERRET` is the environment name where `pyferret` is installed,
and can be any name you like (such as `PyFerret`).
We do not recommend installing `pyferret` in the root environment of miniconda.
The main reason is to take advantage of the `activate` and `deactivate` scripts that
will set up all the variables that PyFerret needs.
(You can test whether the PyFerret environment is activated by issuing the command
`echo $FER_DATA` and see if it returns a directory name.)

If you usually work under a C-shell (such as tcsh) or outside the conda environment,
you may want to create a Bourne shell script that activates and runs PyFerret within
the Bourne shell that is created for running the script.
Such a script would look something like the following (replacing `FERRET` with 
whatever environment name you used):
```shell
#! /bin/sh -l
## initialize the environment for running PyFerret
conda activate FERRET
## You may wish to add directories to FER_DATA and FER_GO
# export FER_DATA="$FER_DATA /my/path/to/big/data/dir"
# export FER_GO="$FER_GO /my/path/to/custom/ferret/scripts"
## Now execute PyFerret with all the command-line arguments given to this script
pyferret $*
```
If this script was called `pyferret.sh`, made executable (`chmod 755 pyferret.sh`),
and placed in a directory listed in your `$PATH` enviroment variable, you can just type
`pyferret.sh` (followed by any desired arguments) from the command line to run PyFerret.
