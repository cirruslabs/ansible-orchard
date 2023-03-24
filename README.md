# Automate Everything!

Ansible roles to configure Orchards workers

# Run Ansible

First, install Ansible Galaxy dependencies:

```bash
ansible-galaxy install -r requirements.yml
```

To install everything needed to participate the workers pool, first populate `orchard_worker_controller_url`
and `orchard_worker_bootstrap_token` in [`production-pool`](production-pool) file. Also don't forget to list all of your
worker hosts to setup in `hosts` field.

Then run the following command:

```bash
ansible-playbook --inventory-file production-pool --ask-pass playbook-workers.yml
```
