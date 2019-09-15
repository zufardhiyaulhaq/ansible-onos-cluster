# Ansible ONOS Cluster
Ansible template to create ONOS Cluster

### Testing in
* 3 Atomix node
* 3 ONOS node
* Ubuntu 16.04 & Ubuntu 18.04 (master branch)
* openSUSE Leap 15.1 (opensuse branch)

## Step
* Prepare deployer nodes (ansible is installed in here)
```
sudo apt-add-repository ppa:ansible/ansible
sudo apt update
sudo apt install ansible
```
* Make sure deployer have root access into all nodes (tips using ssh-copy-id)
```
ssh-copy-id root@atomix
ssh-copy-id root@onos
```
* Clone this repository
```
git clone https://github.com/zufardhiyaulhaq/ansible-onos-cluster.git
```
* Change some variable
```
group_vars/all.yml
hosts/hosts
```
* Run ansible
```
ansible-playbook main.yml -i hosts/hosts
```
