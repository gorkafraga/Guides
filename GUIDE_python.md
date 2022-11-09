# Quick Guide for Python 

## Main issues 

We are likely to have several instances of python in our PC. We need to ensure we know in which one we are working. A light IDE like Spyder (like Rstudio) seems to work best. We can download Anaconda 3 containing a version of Python (as well as the package manager conda among other software). From there we can create environments in which we will install packages. Then launch the Spyder from a given environment. Issues during installation included problems with spyder recognizing the right python version or not recognizing the 'conda' command (e.g., because Anaconda folders were not added in the OS path). PIP is another package manager. Recommended to stick to conda for installing packages whenever possible.  

## Local windows installation 
Main documentation: https://docs.spyder-ide.org/current/installation.html  

* Download Anaconda3 for windows and installed  

* Set environment variables. Add to PATH: Anaconda3, Anaconda3/Scripts and Anaconda3/Library/bin folder 

* Check installation : Open Anaconda prompt and type: conda info --envs 

* Create a environment with modules.In Anaconda prompt type:   
 conda create –n spyder-env –y   or 
  conda create -n spyder-env spyder numpy scipy pandas matplotlib sympy cython


* Activate environment in the prompt  
conda activate spyder-env 

* Install packages and spyder kernle 
(Notice the prompt will change now indicating you are within the creted environment ). Type 'Spyder' to launch spyder from wihin this environment.You can also install  packages like scikit-learn by typing this either in the console or in Spyder (but must be within the enviornment): 
    
     conda install spyder-kernels scikit-learn seaborn   

Alternatively, for launching Spyder you can open the Spyder stand alone from the windows menu, and then go to preferences and set up the Python environment from the newly created env (located in Anaconda3/env folder) 
 
## Exporting environment across platforms (e.g., from windows to Linux)
Imagine you created an environment in one computer and you want now to run those analysis in a remote desktop in another computer (which may have a different operating system). You can export the environment and import it in the other computer. But if the OS are different the dependencies might change (but you still want to have the same version of python and packages if possible). 
https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#sharing-an-environment 
* Create an environment: specify python version 
* Export your environment:  e.g., conda env export > spyder-env.yml --from-history
* Import: 



## Tips

* Install MAMBA: a more efficient solver than Conda.. 
* STATSMODELS package with similar stuff as R , more complete than scipy 
* https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#sharing-an-environment  ---- Check exporting an environment file across platform. We need to –from-history flag when exporting environment (conda env export  –from-history) so that in when installing the environment in a new system Conda will solve the required dependencies (e.g., if we have an environment in windows and we want to use the same packages in Linux,  dependencies might differ between the two OS)  


## keywords:  
pip = package manager works from any environment  
Conda = package and environment  
Spyder = IDE for python (like Rstudio) 
Anaconda =  Python distributor with multiple programs 
https://medium.datadriveninvestor.com/what-is-pip-conda-anaconda-spyder-jupyter-notebook-pycharm-pandas-tensorflow-and-django-36d54778d85c 

 
## Additional Resources 
https://google.github.io/styleguide/pyguide.html  

## Troubleshooting  
Spyder is not showing plotly plots? Set up the default renderer:  
   import plotly.io as io 
   io.renderers.default='browser' 

 

 
