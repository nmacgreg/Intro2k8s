# README for this ansible repo

## ACG Cloud Playground

* For this course, the Playground created 3 hosts running Ubuntu 18 LTS, and gave me their public IP addresses
* Also, read documentation in the directory above on initial patching, etc
* Note: this installs kubernetes packages at version 1.22.0-00 (kublet, kubeadm, kubectl) 

## Using 

* Call this playbook:

```ansible-playbook -i inventory k8sUbuntu.yml -e "ansible_become_password=<redacted>"```
