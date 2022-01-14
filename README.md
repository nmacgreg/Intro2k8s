## ACG "Introduction to Kubernetes", Chapter 2.5

* For this course, the Playground created 3 hosts running Ubuntu 18 LTS, and gave me their public IP addresses, and credentials
* Also, read my documentation over at https://github.com/ualbertalib/Cloud_Study_Notes/blob/main/docs/k8s/Intro2k8s/index.md
* Note: this installs kubernetes packages at version 1.22.0-00 (kublet, kubeadm, kubectl) 

## Using 

* Call this playbook:

```ansible-playbook -i inventory k8sUbuntu.yml -e "ansible_become_password=<redacted>"```
```ansible-playbook -i inventory k8sUbuntu.yml -e "ansible_become_password=<redacted>" --tags initialize```

## Status: 

* This is incomplete - I documented some steps that I don't know how to make idempotent.
* This is incomplete - the final step in "initialize.yml" tasklist is failing to get the worker nodes to join the cluster
* I suggest, maybe
    * https://github.com/dcj/ansible-kubeadm-cluster/blob/develop/cluster-create.yml
    * https://buildvirtual.net/deploy-a-kubernetes-cluster-using-ansible/
    * maybe https://www.linkedin.com/pulse/multi-node-kubernetes-cluster-using-ansibleautomation-ankita-jamdade
    * explore: https://itnext.io/getting-started-with-kubernetes-using-ansible-and-terraform-741e6bb6ad7a
