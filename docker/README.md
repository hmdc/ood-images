# Docker OOD images

Launch the container:

    docker run -p 8080:80 -d --name ood ohiosupercomputer/ood

To set default SSH host for shell app:

    docker run -p 8080:80 -d --name ood -e DEFAULT_SSHHOST=login.my_center.edu ohiosupercomputer/ood

Add a cluster configuration file

    docker cp <cluster name>.yaml ood:/etc/ood/config/clusters.d/<cluster name>.yaml

Once the container is online, the Open OnDemand interface can be accessed at localhost:8080. Access to 
OpenOnDemand is via the `ood` user with password `ood`

## Development

    docker build -t ohiosupercomputer/ood:1.5.0 -t ohiosupercomputer/ood:latest .