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
Get familiar with docker (<href>https://www.docker.com/</href>) and download and run jupyter/scipy-notebook:3.9.10 (<href>https://hub.docker.com/r/jupyter/scipy-notebook</href>) image.

Lunch a jupyter notebook using

`
docker run -p 8888:8888 --user $(id -u):$(id -g) --group-add users -v  "${PWD}":/home/jovyan/work --name misu-jupyterlab -e GRANT_SUDO=yes -e JUPYTER_ENABLE_LAB=yes jupyter/scipy-notebook:3.9.10
`

