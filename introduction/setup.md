# Setup

### Running on EDC EOxHub Workspace

If you are using the EDC environment and have accessed this example through the Open Science Catalog, this example should have the correct kernel selected, and packages installed. You can directly use this example as is, with Dask Gateway. You can access this example on EDC during the week of LPS and the week after if you have registered for this workshop!

To request an account (only available during the workshop!) click on the following and use your github account to sign in: https://workspace.edc-lps25.hub-otc-sc.eox.at/


### Running on your own computer

Most parts of this tutorial were designed to run with limited computer resources, so it is possible to run on your laptop.
It is a bit more complicated as you will have to install the software environment yourself. Also you will not be able to test real cloud distributed processing with Dask gateway.

Steps to run this tutorial on your own computer are listed below and demonstrated _through Linux commands only_:

1. git clone the LPS-25 repository.
```bash
git clone https://github.com/sunnydean/LPS25_Pangeo_x_EarthCODE_Workshop.git
```
2. Install the required software environment with Conda. If you do not have Conda, install it by following these instructions (see [here](https://docs.conda.io/en/latest/miniconda.html)). Then create the environment, this can take a few minutes.
```bash
conda env create -n pangeo -f LPS25_Pangeo_x_EarthCODE_Workshop/environment.yml
```
3. Launch a Jupyterlab notebook server from this environment.
```bash
conda activate pangeo
jupyter lab
```
4. Open a web browser and connect to the Jupyterlab provided URL (you should see it in the jupyter lab command outputs), something like: http://localhost:8888/lab?token=42fac6733c6854578b981bca3abf5152.
5. Navigate to pangeo_on_EarthCODE using the file browser on the left side of the Jupyterlab screen.

