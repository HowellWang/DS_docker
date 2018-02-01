## Data-Science-Analysis-with-Python
This repository is the Docker container for Python data science packages to support multi-platform development. It's the tool I use to support for "Data Science Analysis with Python" to MSBA, MSIS, MSSC and MBA students at the Leavey School of Business at Santa Clara University. 

## How to use it?

* `git clone https://github.com/dataquestio/ds-containers.git DS_docker` to the local machine. 
* `sh build_container.sh python2` (switch `python2` for another container to build that one`).
    * You can also pull the container by running `docker pull dataquestio/python2-starter`.  
* Run `docker run -d -p 8888:8888 -v ORIGIN_FOLDER:/home/ds/notebooks dataquestio/python2-starter`
    * Replace `python2-starter` with the container you want.
    * Replace `ORIGIN_FOLDER` with a folder on your local machine that you want to persist notebooks in.
* Open your browser and start working with IPython notebook.
    * On Linux, the url will be `localhost:8888`.
    * On Windows/OSX, run `docker-machine ip default` (replace `default` with the name of your machine).  Then, you'll be able to access IPython notebook at `CONTAINER_IP:8888`.
* Run `docker ps` to check the docker container id like e3f285fe4a3d, then Run `docker exec -it e3f285fe4a3d /bin/bash` to open a shell prompt in the container with id e3f285fe4a3d. After running docker exec, you'll be put into a shell prompt inside the container. The container is running python in a virtual environment called ds, which should already be activated.To install packages, just type `pip install PACKAGE_NAME`. For our class requirement, you could use it install "fix_yahoo_fiance" and "pydotplus". For "fix_yahoo_finance", you just need to input "pip install fix-yahoo-finance --upgrade --no-cache-dir". For "pydotplus", you need to input "sudo apt-get update", then input "sudo apt-get install graphviz".When you want to exit the container shell prompt, just type exit.



