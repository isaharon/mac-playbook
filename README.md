# Mac Playbook

This playbook installs and configures my Macbook for my personal purposes. The setup used in this project requires the package manager, Homebrew, to be installed first which is probably not ideal for full automation but can hopefully simplify some management of things.

## Requirements

- Apple Command Line Tools installed - `xcode-select --install`
- Homebrew installed - `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
- Ansible installed via Homebrew - `brew install ansible`

## Usage

1. Clone this repository to local drive.

2. Install required Ansible roles.

```shell
ansible-galaxy install -r requirements.yml
```

3. Run playbook.

```shell
ansible-playbook playbook.yml --ask-become-pass
```

## TODO Setup flow

1. Example 1

## References

- https://github.com/geerlingguy/mac-dev-playbook