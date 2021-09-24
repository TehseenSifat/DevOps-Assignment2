# DevOps-Assignment2

- Explain Docker Containers vs VMs
------------------------------------
  Each VM includes a separate operating system image, which adds overhead in memory and storage footprint. ... Containers sit on top of a physical server and its host OS—for example, Linux or Windows. Each container shares the host OS kernel and, usually, the binaries and libraries

- Explain Docker Architecture
------------------------------
Docker follows Client-Server architecture, which includes the three main components that are Docker Client, Docker Host, and Docker Registry.

- Write command to create an nginx container in detached mode with name assignment-2 running on host port 9090 on a custom network named assignment-2
------------------------------------------------------------------------------------------------------------------------------------------------------

docker container run -publish 9090:80 --name assignment-2 nginx
docker container run -p 9090:80 --name assignment-2 nginx

- Write command to see logs of the above container
---------------------------------------------------

docker container logs assignment-2

- Write commands to Exec into the container and cat the output of the default nginx file at /usr/share/nginx/html/index.html
-----------------------------------------------------------------------------------------------------------------------------

docker container exex -it assignment-2 /usr/share/nginx/html/index.html

- Exit the above container, and now recreate the container by Volume using bind mounting
-----------------------------------------------------------------------------------------

docker container stop
 

- Command to exec into the above container and replace the default index.html to a custom one, which says that â€œI am becoming a Docker Expertâ€‌ and it should be persisted for the next times.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

