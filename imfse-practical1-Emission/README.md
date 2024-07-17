# imfse-practical UNIT 5 - WildFire Behavior Modelling - Fire Emission

this is the material for the first practical on fire emission at atmospheric scale.

### Objectives:
- load and plot GFAS data
- load and plot GFED4 data
- obervation of fire Season Emission
- accessing active fire data


### Requirement:
The excercise are proposed via jupyter notebook.
I advice to tun them on andromeda server where data and python encvironement are already available. 
On your windows machine I assume you have wsl installed.
then you need to connect to andromeda form a powershell.
at this stage you need to have a user and a port number
use the list below making sure each of you have a different username.
list of user,port
student1, 8889
student2, 8890
student3, 8891
student4, 8892
student5, 8893
student6, 8894
in the following I use USERNAME for you user and XXXX for the port
```
ssh -L 8888:localhost:XXXX USERNAME@andromeda.cdb.upc.edu
```
while on the sever move to `data` disc
```
cd /datat/USERNAME
```
then activate a python environement that was already set
```
source /opt/imfse/bin/activate
```
launch the jupiter notebook server.
```
jupyter notebook  --port=XXXX
```
and finally in the browser of you windows machine goes to the address provided by the last command.

