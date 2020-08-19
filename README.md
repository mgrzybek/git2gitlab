# git2gitlab

Ansible-playbook-based script to import Git repositories into Gitlab.

You can destroy and recreate the repositories:

* Test if the remote repository still exists
* Delete the local repository
* Import it

You can pull and push changes:

* Test if the remote repository still exists
* Clone the remote repository
* Add Gitlab as a new remote
* Push data to Gitlab

`destroy_and_clone` is set to `true` or `false`.

## Configuration

1. Write a YAML file:

```YAML
- gitlab:
  git:
```

2. Get Gitlab token and API endpoint

## Usage

```bash
# Destroy and reclone the repositories (default)
./git2gitlab.yml \
    -e configfile=repo.yml \
    -e gitlab_token=secret \
    -e gitlab_api=https://gitlab.example.org \
    -e destroy_and_clone=true

# Pull and push data
./git2gitlab.yml \
    -e configfile=repo.yml \
    -e gitlab_token=secret \
    -e gitlab_api=https://gitlab.example.org \
    -e destroy_and_clone=false
```
