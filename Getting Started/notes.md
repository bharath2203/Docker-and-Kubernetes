# DOCKER INTRO

>With the Dockerfile in the current directory use **docker build .** to create a image with **image_id**
The same image_id can be used to run in docker using **docker run image_id** command

>Use *-p local_port:docker_port* to tunnel from the local machine port to the docker container port

>List the docker process using *docker ps* command.
Stop the particular process using the *docker stop process_name* command

**Points to remember**
- Use *-it* option to open interactive terminal while running a docker container
- Use *-a* option to open all the containers even if there are stopped
- COPY and RUN executes relative to the working directory
- Set working directory using WORKDIR command
- *-p* command should be before the image_id in docker run command





**Additional lecture notes**

>As an additional quick side-note: For all docker commands where an ID can be used, you don't always have to copy / write out the full id.
You can also just use the first (few) character(s) - just enough to have a unique identifier.
So instead of
**docker run abcdefg**
you could also run
**docker run abc**
or, if there's no other image ID starting with "a", you could even run just:
**docker run a**
This applies to ALL Docker commands where IDs are needed.