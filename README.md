# Task A

In this task, we were tasked to deploy a simple web server using Nginx running in a Docker container.

Here, I've created 3 containers, all running NGINX.
2 of the containers run the main websites, while the `reverseproxy` container runs the reverse proxy server.

Visit http://localhost/clientA to visit the first site and http://localhost/clientA to visit the second site.

The Docker image is also accessible on https://hub.docker.com/repository/docker/ailanthustng/cs3219_taska.

---

# How to run

1. Clone this repository.
2. Go into the project directory by using `cd cs3219--taskA`
3. Firstly, navigate to clientA using `cd clientA`. Then run `docker-compose up -d --build`
4. Secondly, navigate to clientB using `cd ../clientB`. Then run `docker-compose up -d --build`
5. Lastly, navigate the the reverse proxy using `cd ../reverseProxy`. Then run `docker-compose up -d --build`
6. Now you can go to your browser to access both clientA and clientB using http://localhost/clientA and http://localhost/clientB respectively.
7. After accessing these pages, you can stop all running docker containers using the `docker stop $(docker ps -q)` command on Unix machines, or `docker ps -q | % { docker stop $_ }` on Windows.
