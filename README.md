exo-core
=======

A set of ansible playbooks to deploy a cluster of CoreOS machine on Exoscale.

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
- Test the cloustack dynamic inventory, issuing the inventory as a json inventory to the commandline

```./setup.sh```

Test the dynamic inventory with ansible.

```ansible -i cloudstack.py all -m ping```

This will ping all your exoscale instances and report if they are up.




Authors
=======


Licence
=======
GNU
Click on the [Link](COPYING) to see the full text.
