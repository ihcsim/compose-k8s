# compose-k8s

Docker Compose file to set up Kubernetes.

## Getting Started

1. Install the Kubernetes command-line tool, [`kubectl`](http://kubernetes.io/v1.1/docs/user-guide/prereqs.html).
1. Source the environmental variables file: `$ source env.sh`
1. Run the services: `$ docker-compose up`
1. On OS/X with Docker Machine, set up port forwarding via SSH: `$ docker-machine ssh <machine> -L8080:localhost:8080`
1. Test your cluster: `$ kubectl get nodes`

```sh
NAME        LABELS                             STATUS
127.0.0.1   kubernetes.io/hostname=127.0.0.1   Ready
```

## Other Commands

1. To stop the services: `docker-compose stop`
1. To remove the services and volumes: `docker-compose rm -v`

## Supported Environmental Variables

The supported enviromental variables are found in the `env.sh` script file.

Variable     | Description
------------ | -----------
K8S_VERSION  | Kubernetes version. Default to v1.1.3.
ETCD_VERSION | etcd version. Default to 2.0.12.
