exo-deep-learing-gpu
=======

A set of ansible playbooks to deploy a GPU instance with common NN frameworks on Exoscale.

- Exoscale is a Switzerland cloud provider for the digital native based on the Apache Cloudstack API.
- Cloudstack is open source software designed to deploy and manage large networks of virtual machines.
- Ansible is the simplest way to automate apps and IT infrastructure, the DevOps way.


Getting Started
=======

First copy or create a cloudstack.ini with your exoscale credentials.

```
cat ./cloudstack.ini
[cloudstack]
endpoint = https://api.exoscale.ch/compute
key = cloudstack api key
secret = cloudstack api secret
```

Run the setup script to make sure the dependencies are met.
It will do the following for you:
- Install or update Ansible, module ansible
- Install or update your python cloudstack API, module cs
- Download the latest ansible cloudstack dynamic inventory, cloudstack.py

```./setup.sh```

Run the playbook to create the instance.
```
$ ansible-playbook create-instance.yaml
```

Feel free to adapt *group_vars/all.yaml* and the playbooks to modify the parameters to your liking.


Authors
=======
Marc Guillen (marc.guillen@datsci.farm)

Licence
=======
APACHE
Click on the [Link](LICENSE) to see the full text.
