## Data-Science-Analysis-with-Python
This repository is the Docker container for Python data science packages to support multi-platform development. It's the tool I use to support for "Data Science Analysis with Python" to MSBA, MSIS, MSSC and MBA students at the Leavey School of Business at Santa Clara University. 

## Getting started

* Run `sh build_container.sh python2` (switch `python2` for another container to build that one`).
    * You can also pull the container by running `docker pull dataquestio/python2-starter`.  
* Run `docker run -d -p 8888:8888 -v ORIGIN_FOLDER:/home/ds/notebooks dataquestio/python2-starter`
    * Replace `python2-starter` with the container you want.
    * Replace `ORIGIN_FOLDER` with a folder on your local machine that you want to persist notebooks in.
* Open your browser and start working with IPython notebook.
    * On Linux, the url will be `localhost:8888`.
    * On Windows/OSX, run `docker-machine ip default` (replace `default` with the name of your machine).  Then, you'll be able to access IPython notebook at `CONTAINER_IP:8888`.

