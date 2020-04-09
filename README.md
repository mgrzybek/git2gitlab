# git2gitlab

Ansible-playbook-based script to import Git repositories into Gitlab:

* Test if the remove repository still exists
* Delete the local repository
* Import them

## Configuration

1. Write a YAML file:

```YAML
repositories:
  - gitlab:
    git:
```

2. Get Gitlab token and API endpoint

## Usage

```bash
./git2gitlab.yml -e configfile=repo.yml -e gitlab_token=secret -e gitlab_api=https://gitlab.example.org
```

