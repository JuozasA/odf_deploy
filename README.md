# Summary
- [Introduction](#Introduction)
- [Deploy ODF v4.8 Cluster](#Deploy_ODF_v4.8_Cluster)

## Introduction 
Ansible role to deploy ODF cluster with attached devices

## Requirements
- OpenShift Container Platform v4.8+ 
- OpenShift Container Storage v4.8+ (AKA OCS and now ODF)
- OpenShift authentication through kubeconfig file, modifify the following variable accordingly:
```bash
roles/odf-deploy/defaults/main.yml
# kubeconfig path
kubeconfig: '$HOME/.kube/config'
```

- Supported infrastructures: AWS IPI, VMware UPI (Other platforms have not been tested yet but the tool should work)
- `git` client
- Ansible at least v2.8 
- k8s ansible module

## OpenShift Data Foundation v4.7
The OpenShift Data Foundation deployment is based on version 4.8

### Deploy ODF v4.8 Cluster  
  
Please make sure you have 3 worker nodes delegated to ODF.

Run the ansible role:
```
ansible-playbook use_playbook.yml
```