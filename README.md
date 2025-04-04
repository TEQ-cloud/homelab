# Homelab

## Introduction

## Cluster Provisioning & Architecture
The main cluster consists of two node VMware vSphere (ESXi) cluster managed by VMware vCenter, running all my workloads in the form of virtual machines.


## Hardware

### Nodes

Dell Poweredge R730xd  
Dell EMC Poweredge R540  

## Installed Apps and Infrastructure

### Apps

| Name | Description |
| --- | --- |
| Homepage | A portal with links to all mamangement pages of my infrastructure |

### Infrastructure

| Logo | Name | Description |
| --- | --- | --- |
| <img width="45" src="https://www.stevenbright.com/2023/02/managing-esxi-local-user-accounts-from-vcenter-server/images/cover.png"> | [vCenter](https://www.vmware.com/products/cloud-infrastructure/vcenter) | A cluster manager for VMware vSphere (ESXi) |
| <img width="45" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fassets.stickpng.com%2Fimages%2F629a3d113e59ee069da94c78.png&f=1&nofb=1&ipt=3aaadaa4edd8ae5450dda44d9486e5340c3fb7238d4eb97629fd2984f71515d4&ipo=images"> | [Veeam Backup and Replication](https://www.veeam.com/products/veeam-data-platform/backup-recovery.html?ad=packaging-foundation-backup-recovery) | Manages the backup infrastructure that backs up the VMware cluster |
| <img width="45" src="https://dashboard.snapcraft.io/site_media/appmedia/2020/11/Screenshot_2020-11-21_at_02.05.22.png"> | [Semaphore UI](https://semaphoreui.com/) | User friendly web interface for executing Ansible playbooks, Terraform, OpenTofu code and Bash scripts. |
