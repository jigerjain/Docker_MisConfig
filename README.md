# Docker Privilege Escalation
This project helps to evaluate how docker group access should be appropriately mainted to prevent privilege escalation.

As per Docker, to use docker command either a user needs to be a sudo group member or should have access to docker group.

When a system trusts a user with sudo membership, it assumes the fact that the user has administrative privileges.
However, the same notion is not been yet shared with most developers that the user within a docker group could access the unrestricted paths and files on the host machine from the container spawned by his privileges



