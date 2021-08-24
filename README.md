# sf-pract-11

This repo contains example terraform script that creates 2 virtual machines on Yandex Public Cloud service and shell scripts for creating a Kubernetes cluster via kubectl and configuring this vms as a master and a worker node of the cluster.

Requirements: Yandex Cloud account, OAUTH token for this account, Terraform and Git, ssh key pair.

It is necessary to change ssh public key and username in meta.yml file. Cloud and folder ids in variables.tf also need to be changed to your values.

Usage:

```
git clone https://github.com/jkL-snk/sf-pract-11-k8s-in-yc-via-tf-bash.git
cd ./sf-pract-11-k8s-in-yc-via-tf-bash
terraform apply
```

Input your Yandex Cloud OAUTH token value.

Terraform outputs IP addresses of virtual machines. Then you can connect via SSH to these machines using your private key for public key in meta.yml. To create master node run export EXTIP=<this vms external ip> and then run master.sh. The script will output the join command. On the worker node you need to run worker.sh and then run this join command.
