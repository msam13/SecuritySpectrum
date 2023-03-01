# Setting up docker with WSL2 Backend

installed Windows Subsystem Linux (WSL) with Ubuntu distro

> wsl install -d ubuntu

Download and run wsl_update_x64.msi

# setting up virtual python environment

Virtual environment the libraries, scripts installed are separated from other Virtual environment.
(no conflicts in versions among different projects)

## installing Virtual Environment
Installation
> pip install virtualenv

creating a new venv
> python -m venv <venv-name>

Activating a new venv
>cd <venv-name>
>Script\Activate  
> mitre\Scripts\activate<br>
> source mitre/lib/activate (on mac) <br>
  
update pip to latest version
> python.exe -m pip install --upgrade pip

Fork and clone the repo
> git clone https://github.com/msam13/2023-ectf-tools.git

install the tools
> python -m pip install -e 2023-ectf-tools

clone the repo for insecur_ example

building docker image
> python -m ectf_tools build.env --design 2023-ectf-insecure-example --name ectf-insecure
***
INFO 2023-02-10 12:51:36,497 Building image ectf:ectf-insecure

INFO 2023-02-10 13:00:23,034 Built image ectf:ectf-insecure
***

### build the tools

>  python -m ectf_tools build.tools --design 2023-ectf-insecure-example --name ectf-insecure

***
INFO 2023-02-10 13:15:11,207 ectf:ectf-insecure: Building tools <br>
INFO 2023-02-10 13:15:16,549 ectf:ectf-insecure: Built tools
***

### Build deployment

>  python -m ectf_tools build.depl --design 2023-ectf-insecure-example --name ectf-insecure --deployment d1

***
(mitre) PS D:\MITRE\mitre> python -m ectf_tools build.depl --design 2023-ectf-insecure-example --name ectf-insecure --deployment d1 <br> 
INFO 2023-02-10 13:30:23,839 ectf:ectf-insecure: Building deployment d1 <br>
INFO 2023-02-10 13:30:25,028 ectf:ectf-insecure: Built deployment d1 <br>
***


## build car_fob
> python3 -m ectf_tools build.car_fob_pair --design 2023-ectf-insecure-example --name ectf-insecure --deployment d1 --car-out ./bin --fob-out ./bin --car-name insec_car --fob-name insec_fob --car-id 1 --pair-pin 123456

```
INFO 2023-02-24 20:53:15,338 ectf:ectf-insecure:d1: Building car insec_car
INFO 2023-02-24 20:53:15,338 ectf:ectf-insecure:d1: Making output directory /Users/sam/mitre_ectf/bin
INFO 2023-02-24 20:53:17,310 ectf:ectf-insecure:d1: Built device insec_car
INFO 2023-02-24 20:53:17,310 ectf:ectf-insecure:d1: Packaging image for device insec_car
INFO 2023-02-24 20:53:17,311 ectf:ectf-insecure:d1: Packaged device insec_car image
INFO 2023-02-24 20:53:19,131 ectf:ectf-insecure:d1: Built device insec_fob
INFO 2023-02-24 20:53:19,131 ectf:ectf-insecure:d1: Packaging image for device insec_fob
INFO 2023-02-24 20:53:19,132 ectf:ectf-insecure:d1: Packaged device insec_fob image
```

## build fob 

> python3 -m ectf_tools build.fob --design 2023-ectf-insecure-example --name ectf-insecure --deployment d1 --fob-out ./bin --fob-name insec_fob_unpair

```
INFO 2023-02-24 20:57:20,388 ectf:ectf-insecure:d1: Building unpaired fob insec_fob_unpair
INFO 2023-02-24 20:57:22,241 ectf:ectf-insecure:d1: Built device insec_fob_unpair
INFO 2023-02-24 20:57:22,242 ectf:ectf-insecure:d1: Packaging image for device insec_fob_unpair
INFO 2023-02-24 20:57:22,243 ectf:ectf-insecure:d1: Packaged device insec_fob_unpair image
```