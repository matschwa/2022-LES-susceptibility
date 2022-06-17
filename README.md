# 2022-LES-susceptibility
## Download data

### Ackermann 2009 Data
available at https://www.giss.nasa.gov/staff/aackerman/gcss_rf02/index.html

in `/{PWD}/data/` download the data from Ackerman, et al. (2009) intercomparison e.g. using wget:
```
wget https://www.giss.nasa.gov/staff/aackerman/gcss_rf02/dime/BLCWG_DYCOMS-II_RF02.scalars.nc
wget https://www.giss.nasa.gov/staff/aackerman/gcss_rf02/dime/BLCWG_DYCOMS-II_RF02.profiles.nc
```

### MIMICA Large-eddy simulation data 
**_NOTE:_**  Upload to bolinc and provide link here!

## Clone/download code form github
**_NOTE:_**  Upload to bolinc and provide link here!

# Run juypter notebook in docker
Install docker (<href>https://www.docker.com/</href>) and download and run jupyter/scipy-notebook:3.9.10 (<href>https://hub.docker.com/r/jupyter/scipy-notebook</href>) image.

Lunch a jupyter notebook using

```docker run -p 8888:8888 --user $(id -u):$(id -g) --group-add users -v  "${PWD}":/home/jovyan/work --name misu-jupyterlab -e GRANT_SUDO=yes -e JUPYTER_ENABLE_LAB=yes jupyter/scipy-notebook:3.9.10```

Inside the container the file tree should look like this:
```
.
└── work
    ├── 2022-LES-susceptibility
    │   ├── calc_susceptibility_3d.ipynb
    │   ├── functions.ipynb
    │   ├── LICENSE
    │   ├── LWP_validation_Ackermann2009.ipynb
    │   ├── maxSupersaturation.ipynb
    │   ├── namelist.ipynb
    │   ├── Profiles_validation_Ackermann2009.ipynb
    │   ├── README.md
    │   └── set_up_case_dict.ipynb
    └── data
        ├── BLCWG_DYCOMS-II_RF02.profiles.nc
        ├── BLCWG_DYCOMS-II_RF02.scalars.nc
        ├── DYCOMS_limDQC_AO_LTS
        └── DYCOMS_limDQC_AO_LTS.zip
```


To Install the required packages lunch a new terminal in the jupyter-lab, navigate to code directory (`/home/jovyan/work/2022-LES-susceptibility`) and install packages using `conda install --file requirements.txt`.

Finally, execute the notebooks to reproduce all figures. 


## Pyrcel simulations

Download and install pyrcel following the official instructions https://pyrcel.readthedocs.io/en/latest/

