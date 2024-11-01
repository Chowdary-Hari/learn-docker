FROM almalinux:9
ENV name="hari" \
    course="devops" \
    version="1.0"
CMD [ "sleep","100" ]
# you  can access the env variables in the container
# env variables location --> :: docker exec -it <container id> bash :: :: env ::
# available env variables that location --> :: docker exec -it <container id> env ::

#   only env variables in the runing container
# [ ec2-user@ip-172-31-62-57 ~/learn-docker/docker/ENV ]$ docker exec -it 24515 env
# PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# HOSTNAME=24515c393ae0
# TERM=xterm
# name=hari
# course=devops
# version=1.0
# HOME=/root
