# Docker Privilege Escalation
This project helps to evaluate how docker group access could exploited to gain unrestricted file access of the host machine.

As per Docker, to use docker command either a user needs to be a sudo group member or should have access to docker group.

When a system trusts a user with sudo membership, it assumes the fact that the user has administrative privileges.
However, the same notion is not been yet shared with most developers that the user within a docker group could access the unrestricted paths and files on the host machine from the container spawned by his privileges.

```
git clone https://github.com/jigerjain/Docker_Privesc.git
cd Docker_Privesc/
docker build -t application .
./exploit.sh

Running docker
You could access the root folder of the system machine under /Hostroot folder

```





