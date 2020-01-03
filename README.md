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

<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Project](#about-the-project)
  * [Built With](#built-with)
* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
   * [Prerequisites](#prerequisties)
   * [Docker](#docker)
   * [Pip](#pip)
   * [Virtualenvwrapper](#virtualenvwrapper)
* [Run This Show](#Run-This-Show)
* [Usage](#usage)
* [Roadmap](#roadmap)
* [Contributing](#contributing)
* [License](#license)
* [Contact](#contact)


<!-- ABOUT THE PROJECT -->
## About The Project

This is a out-of-the-box Django project that can be downloaded and spun up relatively quickly. The app is designed to be a 
production grade Django application complete with:
    * Prod grade WSGI Server
    * Reverse Proxy Server
    * Prod grad database
    * Virtualisation

Simply clone the repo, build the images and run associated containers. This way, your time can be spent writing code and decreasing 
project turnaround time, rather than repeating processes over and over to configure web servers and the like.

If I have added you as a contributor to this project, then I hope this saves you some time (and pain)!


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


<!-- Spinning up Docker -->
## Run This Show

* Clone the repo (Make sure that the DockerFile and docker-compose.yml are with the repo clone!)
* Then cd to the project directory and follow the below commands to build the (production) Docker image and run the 
(production) container.
```
$ docker-compose -f docker-compose.prod.yml up -d --build
$ docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput
$ docker-compose -f docker-compose.prod.yml exec web python manage.py collectstatic --no-input --clear
```

* To execute any Terminal and/or Shell commands within the docker container, such as setting up a super user, run the following:
```
$ docker-compose -it exec django-admin createsuperuser
```

<!-- ROADMAP -->
## Roadmap

* Add a testing suite
* Consider CI/CD piplines with Kubenetes functionality from the get-go
* Add Redis for caching
* Add Celery for smooth automation of processes etc.


<!-- CONTRIBUTING -->
## Contributing

If I have added you as a contributor, then any additions, comments and feedback will be greatly appreciated. I can't always keep up with the latest
Dev Ops practices, vulnerabilities or business needs so, any contributions you make are **greatly appreciated**.

To contribute to the project, fork the project and create a pull request.
Check out these CLI commands below to copypasta:

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information. 
Feel free to take this project and do what you like with it. 


<!-- CONTACT -->
## Contact
If you would like to see something added to 
