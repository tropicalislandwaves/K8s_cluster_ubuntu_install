#### Create two Ubuntu VMs in VirtualBox

**Create two Ubuntu VMs in VirtualBox. Remember the folloing points when creating the VMs**
- Master node should have minimum 2 CPU cores and 2 GB RAM
- Worker node should have minimum 2 CPU cores and 1 GB RAM
- Select *bidirectional* for *clipboard* setting
- Select *Bridged network adapter*

**Make the following changes once VMs are up and running**
- Change IP address allocation from Automatic to Manual (IPV4) along with DNS.
- Run the command ```swapoff -a``` in both the VMs
- Edit */etc/fstab* and comment swap line
- Create *kubernetes.list* file in */etc/apt/sources.list.d/* and add ```deb https://apt.kubernetes.io/ kubernetes-xenial main```
- Run ```sudo apt-get update && apt-get upgrade -y```
- Run ```sudo apt-get install -y vim open-ssh server```
