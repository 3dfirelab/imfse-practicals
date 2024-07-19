<img style="float: left;" src="./images/logo.png" width="400"/> <br/><br/><br/>

# IMFSE-practical UNIT 5 - WildFire Behavior Modelling 

## General Objectives
In this practicals on fire behavior modeling, using a fire that occured in el pont de Vilomara on the 17 of July 2022, we are going to look at 
- fire emission estimates like the one provided by [Copernicus](https://atmosphere.copernicus.eu/emissions-and-surface-fluxes).
- fire propagation as modeled with fire spread model like Farsite ([Finney et al 1994](https://doi.org/10.2737/RMRS-RP-4))
- and finally plume simulation from fire-atmosphere coupled system like the FDS-Level set model ([bova et al 206](https://www.fs.usda.gov/pnw/pubs/journals/pnw_2016_bova001.pdf)).
![pdvoverview](./images/pdv_overview.webp)

This will makes 3+1 practicals. The `+1` is on GIS, introducing the very basic skills you will need to process Flammap model outputs. The program is the following: 
1. practical1-Emission
2. practical2-GIS
3. practical3-FlamMap
4. practical4-FDSLS


## Technical Requirement to run juyterLab on andromeda UPC server:
Several excercises of the practical are proposed via jupyter notebook, a python interactive environment.
I advice to run them on andromeda server where data and python environment are already available. 

### 1. create or log to a virtual python environment on you windows machine
On your UPC windows machine I assume you have wsl installed.
In a windows powershell run 
```
wsl --install
```
This will installed a virtual pyhton environment in the machine that will be save in you local directory, so it would be accessible lateron when you reconnect.
During install you are asked to create an account and give a password. Take any, this username is not used in the following.  

If wsl is already installed just enter 
```
wsl 
```
to start the virtual python environment. 

### 2. connect to andromeda
Then you need to connect to andromeda form the virtual python environemnt.
At this stage you need to have a user/password and a port number to connect to andromeda, if not ask me.  

Use the list below assigne user to  different andromeda port.  
list of user,port  
- student1, 8889
- student2, 8890
- student3, 8891
- student4, 8892
- student5, 8893
- student6, 8894

in the following I use USERNAME for you user and XXXX for the port.  

all command line starting with a `$` should be enter in a terminal once you are connected to andromeda
```
$ ssh -L 8888:localhost:XXXX USERNAME@andromeda.cdb.upc.edu
```
while on the sever move to `data` disc
```
$ cd /data/USERNAME
```
clone here the material of the practicals:
```
$ git clone https://github.com/3dfirelab/imfse-practicals.git
```
then activate a python environement that was already set
```
$ source /opt/imfse/bin/activate
```
launch the jupiter notebook server.
```
$ jupyter lab  -no-browser --port=XXXX
```
and finally in the browser of your windows machine (edges, firefox, ...) goes to the address provided in the last command output that shoudl looks like something like this:
localhost:**XXXX**/tree?token=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

Here, you need to change **XXXX** to **8888** in you brower url. your token number should remain unchanged.

Within the jupyter interface you should be able to navigate to the first practical imfse-practical1-Emission and sub directories where wyou will find the first notebook.

## Note on using jupyterlab:    
- to open .md file, right click and select  `open with` and get `markdown preview`
- to kill the jupyter server enter `Ctrl-c` in the terminal where it runs and answer yes to the `[Y/n]` question.
