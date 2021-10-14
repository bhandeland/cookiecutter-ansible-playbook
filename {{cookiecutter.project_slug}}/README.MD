# {{ cookiecutter.project_slug }} playbook 

{{ cookiecutter.project_short_description }}

## How to use


## Creating venv (optional but highly recommended)

The easiest way to ensure you have the right ansible and properly libs installed is to use a python venv. You only have to set it up once:

```
    python3 -m venv .env
    .env/bin/pip install --upgrade pip
    .env/bin/pip install ansible[azure]==2.9.13
```

After creating the venv you can enter it in order to use ansible (this has to be repeated once per shell session):

```
    source .env/bin/activate
```

### Running playbook locally

1. Run `ansible-galaxy install -r roles/requirements.yml -p roles` in this directory to get the required Ansible roles.
2. Run `ansible-playbook -c local -i inventory/inventory.ini {{ cookiecutter.project_slug }}-playbook.yml`

### Running playbook on remote target server from local machine

1. Run `ansible-galaxy install -r roles/requirements.yml -p roles` in this directory to get the required Ansible roles.
2. Run `ansible-playbook -i inventory/<inventory_file> --key-file "~/.ssh/<private_key>" -u <user-remote> {{ cookiecutter.project_slug }}-playbook.yml`

### Running playbook in dry mode (check)

1. Run `ansible-galaxy install -r roles/requirements.yml -p roles` in this directory to get the required Ansible roles.
2. Run `ansible-playbook -i inventory/<inventory_file> --key-file "~/.ssh/<private_key>" -u <user-remote> {{ cookiecutter.project_slug }}-playbook.yml --diff --check`

## License

{{ cookiecutter.license }}

## Author

[{{ cookiecutter.full_name }}](mailto:{{ cookiecutter.email }})

## Version

Release date: {{ cookiecutter.release_date }}
Version: {{ cookiecutter.version }}
