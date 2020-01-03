# A Plug-In-And-Play Production Grade Django App.
<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="">
    <img src="https://github.com/Kay-Wilkinson/blog_markdown/blob/master/Img_Assets/docker.png" alt="This would have shown a cool Docker/Python logo :/" width="200" height="120">
  </a>

  <h3 align="center">Dockerised, Production-Grade Django</h3>

  <p align="center">
    Combining the awesome full-stack framework with the most awesome virtualisation technology 
    <br/>
  </p>
</p>

### Built With
This section should list any major frameworks that you built your project using. Leave any add-ons/plugins for the acknowledgements section. Here are a few examples.
* [Docker](https://hub.docker.com)
* [Django](https://www.djangoproject.com/)
* [Nginx](https://www.nginx.com/)
* [Gunicorn](https://gunicorn.org/)
* [PostGres](https://www.postgresql.org/)

### Prerequisites

#### Docker:
Docker will need to be preinstalled in order to work with it:
https://docker.com 
Ensure that Docker is running whilst creating and running this project. I do so via the handy Desktop App.
Also ensure that docker-compose (the handy CLI tool) is also installed.
#### Pip:
It is likely that you already have pip installed if you already work with Python, but just in case...
Install:
```
$ curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
```
NB - You may need to run the below command with `sudo` prepended to the command.
```
$ python get-pip.py
```

#### Virtualenvwrapper:
Create a sandbox environment to keep installs at a project level, rather than installing them Globally.
Install:
```
$ pip install virtualenvwrapper
```
Configure:
```
$ export WORKON_HOME=~/Envs
$ mkdir -p $WORKON_HOME
$ source /usr/local/bin/virtualenvwrapper.sh
$ mkvirtualenv DOCKER_DJANGO
```
For more info (or debugging), checkout the official docs:
https://virtualenvwrapper.readthedocs.io/en/latest/
