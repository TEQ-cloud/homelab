# Homelab

Homelab to simulate and play arround with all parts and stages of a production environment.

A lot of techniques used in this homelab are documentend op my blog and LinkedIn.
https://teqcloud.net
https://www.linkedin.com/in/quinten-de-haard-2b4900333/

## Introduction

This repository contains all configurations and scripts I use to compose and automate my homelab.

The purpose of my homelab is learning about and play with all sorts of things to explore, test and deploy different software and services. In my current function as a Cloud Engineer, I get to work with big and powerfull production VMware clusters, and this homelab is the place in witch I can learn and play around with new things. Since I have full control and responsibility over the whole system, it teaches me to do things while minimizing downtime and it helpes me get the right mindset of what exactly to document. And since I host services myself, I also have to think about testing and proof of concept phases, maintainance windows, security, backup, the best way of deployment, automation and more.

## Cluster Provisioning & Architecture
The main cluster is a VMware vSphere (ESXi) cluster consisting of two nodes, managed by VMware vCenter, running all my workloads in the form of virtual machines.


## Hardware

### Nodes

My homelab concists of 2 Dell servers that serve as hypervisors and a disk shelf to expand my storage needs.

Dell Poweredge R730xd
Dell Poweredge R720xd
Dell Powervault MD1200 

## Installed Apps and Infrastructure

### Apps

Everything I self host to make my own life easier.

| Logo | Name | Description |
| --- | --- | --- |
| <img width="45" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fuser-images.githubusercontent.com%2F88257202%2F194461324-cd562d2d-2a96-4fbc-8e93-80085c514f0d.png&f=1&nofb=1&ipt=32ab2bca591ee8c1d59784094379e74fc21a48c8a4971905e665851411a89ff9"> | [Homepage](https://gethomepage.dev/) | A portal with links to all mamangement pages of my infrastructure. |
| <img width="45" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fimmich.app%2Fimg%2Fimmich-logo-inline-light.png&f=1&nofb=1&ipt=18c8276b9b90e035189075e8325274c99ea7852ef2744e3ea37767fc88c99c20"> | [Immich](https://immich.app/) | My favorite backup solution for all media on my phone. |
| <img width="45" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.journaldugeek.com%2Fcontent%2Fuploads%2F2022%2F08%2Fplex-logo.jpg&f=1&nofb=1&ipt=98ddb987554b11886448890bdadecbd70cb32619e5efa8ec31df36017baace4e"> | [Plex](https://www.plex.tv/) | Movie streaming app to stream my own movies to all my devices. |

### Infrastructure

Everything needed to run my homelab and deploy appliactions.

| Logo | Name | Description |
| --- | --- | --- |
| <img width="45" src="https://www.stevenbright.com/2023/02/managing-esxi-local-user-accounts-from-vcenter-server/images/cover.png"> | [vCenter](https://www.vmware.com/products/cloud-infrastructure/vcenter) | A cluster manager for VMware vSphere (ESXi) |
| <img width="45" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fassets.stickpng.com%2Fimages%2F629a3d113e59ee069da94c78.png&f=1&nofb=1&ipt=3aaadaa4edd8ae5450dda44d9486e5340c3fb7238d4eb97629fd2984f71515d4&ipo=images"> | [Veeam Backup and Replication](https://www.veeam.com/products/veeam-data-platform/backup-recovery.html?ad=packaging-foundation-backup-recovery) | Manages the backup infrastructure that backs up the VMware cluster |
| <img width="45" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.ixsystems.com%2Fwp-content%2Fuploads%2F2021%2F02%2Ftruenas_scale-logo-full-color-rgb.png&f=1&nofb=1&ipt=9de4481f0ef626ee7fd21716e24d34b9e77a7225b7d7bfb9120c9fcfec61b235"> | [TrueNAS Scale](https://www.truenas.com/) | Operating system for main storage solutions. |
| <img width="45" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fivorontita.com%2Fwp-content%2Fuploads%2F2020%2F06%2Fkisspng-active-directory-federation-services-microsoft-off-5b1e5b080fff82.7771912715287160400655.png&f=1&nofb=1&ipt=b48c88bbff0d36793e70b8097154fe3089889d5916bb6acda662be7a4768b8cb"> | [Active Directory](https://www.microsoft.com/) | Identity management for users and groups. |
| <img width="45" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.returngis.net%2Fwp-content%2Fuploads%2F2018%2F07%2FAzure-DNS-logo.png&f=1&nofb=1&ipt=0c17fddc9717293b81fd59e8a35e4ebc4620db4ecd67039883dab7f8de69ac08"> | [DNS](https://www.microsoft.com/) | DNS server on a Windows Server 2022 domain controller for name resolution. |
| <img width="45" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.pngkey.com%2Fpng%2Ffull%2F325-3250930_opnsenselogo-opnsense-logo.png&f=1&nofb=1&ipt=72aecf0d674bd7f75047edff196aaee75ccf38dc23c5b7866f74cd11184285e9"> | [OpnSense](https://opnsense.org/) | Statefull firewall for controlling access and traffic between networks. |
| <img width="45" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftailscale.gallerycdn.vsassets.io%2Fextensions%2Ftailscale%2Fvscode-tailscale%2F0.4.4%2F1688077014639%2FMicrosoft.VisualStudio.Services.Icons.Default&f=1&nofb=1&ipt=e42260e52b82c6557796543b5ad828c4e9d98eb937d53ff1073dd18548d7d36c"> | [Tailscale](https://tailscale.com/) | My VPN of choice to controll network access to remote devices and users. |
| <img width="45" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Flogos-world.net%2Fwp-content%2Fuploads%2F2021%2F02%2FDocker-Symbol.png&f=1&nofb=1&ipt=ff94a5d7aef91dc3c6e215d41e674974b66ce79862f7ae57c0bc682bbff89812"> | [Docker](https://www.docker.com/) | Containerized infrastructure spread over multiple VM's. |
| <img width="45" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcdn.thenewstack.io%2Fmedia%2F2023%2F03%2Fd417d139-portainer-logo-black-stacked%403x-1-300x201.png&f=1&nofb=1&ipt=1a2bb61aee9af5cd04c26d833c33c66690f6ed6532a676323109d630d96ef0e7"> | [Portainer](https://www.portainer.io/) | Manager for all stacks and containers running on the docker infrastructure. |
| <img width="45" src="https://dashboard.snapcraft.io/site_media/appmedia/2020/11/Screenshot_2020-11-21_at_02.05.22.png"> | [Semaphore UI](https://semaphoreui.com/) | User friendly web interface for executing Ansible playbooks, Terraform, OpenTofu code and Bash scripts. |
