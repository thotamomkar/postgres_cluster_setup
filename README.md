# postgres_cluster_setup
Test HA cluster, based on Postgres, Patroni & etcd.
For test purposes only!

## Third-party products list

### [Vagrant]
Vagrant is a tool for building and managing virtual machine environments in a single workflow. With an easy-to-use workflow and focus on automation, Vagrant lowers development environment setup time, increases production parity, and makes the "works on my machine" excuse a relic of the past.
[More](https://www.vagrantup.com/intro/index.html)

### [Patroni]
Patroni is a template for you to create your own customized, high-availability solution using Python and - for maximum accessibility - a distributed configuration store like ZooKeeper, etcd, Consul or Kubernetes. 
[More](https://patroni.readthedocs.io/en/latest/)

### [etcd]
Etcd is a distributed reliable key-value store for the most critical data of a distributed system
[More](https://coreos.com/etcd/docs/latest/)

## Usage
* install vagrant [vagrantup/installation](https://www.vagrantup.com/docs/installation/)
* install virtual box [virtualbox/installation](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=13&cad=rja&uact=8&ved=2ahUKEwj90-u-0ePhAhXwwcQBHWgmDl8QFjAMegQIBBAB&url=https%3A%2F%2Fwww.virtualbox.org%2Fmanual%2Fch02.html&usg=AOvVaw2MR27hIJR9ea15aOEfQIKg)
* Execute: ```vagrant up --provision```