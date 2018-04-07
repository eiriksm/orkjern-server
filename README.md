# orkjern-server

Setup for my server.

## Installation

Install with:

```
ansible-galaxy install -r requirements.yml
```

## Usage

Run with

```
$ ansible-playbook -i <inv.file> -l hostname -b provisioning/playbook.yml
```

The inv.file should look something like this:

```
my_hostname ansible_host=my_ssh_alias
```