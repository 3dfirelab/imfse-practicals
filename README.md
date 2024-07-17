<img style="float: left;" src="./imfse-practical1-Emission/images/logo.png" width="400"/> <br/><br/><br/>

# IMFSE-practical UNIT 5 - WildFire Behavior Modelling 

## General Objectives
Using a fire that occured in el pont de Vilomara in on the 17 of July 2022, we are going to look at 
- fire emission estimate like the one provided in Copernicus.
- fire propagation as modeled with fire spread model like Farsite
- and finally fire-atmosphere couple model like the FDS-Level set model.
  

## Technical Requirement:
Several excercises of the practical are proposed via jupyter notebook, a python interactive environment.
I advice to run them on andromeda server where data and python encvironement are already available. 
On your windows machine I assume you have wsl installed.
then you need to connect to andromeda form a powershell.
at this stage you need to have a user and a port number
use the list below making sure each of you have a different username.
list of user,port
- student1, 8889
- student2, 8890
- student3, 8891
- student4, 8892
- student5, 8893
- student6, 8894

in the following I use USERNAME for you user and XXXX for the port
```
ssh -L 8888:localhost:XXXX USERNAME@andromeda.cdb.upc.edu
```
while on the sever move to `data` disc
```
cd /datat/USERNAME
```
clone here the material of the practicals here:
```
git clone https://github.com/3dfirelab/imfse-practicals.git
```
then activate a python environement that was already set
```
source /opt/imfse/bin/activate
```
launch the jupiter notebook server.
```
jupyter lab  -no-browser --port=XXXX
```
and finally in the browser of your windows machine goes to the address provided by the last command that shoudl looks like something like this:
http://localhost:8888/tree?token=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

Within the jupyter interface you should be able to navigate to the first practical imfse-practical1-Emission and sub directories where wyou will find the notebook.

**Note**:   
to open .md file, right click and select  `open with` and get `markdown preview`