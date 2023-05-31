# Mac Playbook

This playbook installs and configures my Macbook for personal purposes. The setup used in this project requires the package manager, Homebrew, to be installed to simplify some management of things.

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

3. Modify/update default config.

```shell
cp default.config.yml config.yml
vim config.yml
mv config.yml default.config.yml # optional
```

4. Run playbook.

```shell
ansible-playbook playbook.yml --ask-become-pass
```


## TODO Setup flow

1. Example 1

## Testing

- Create macOS VM using `tart`

```shell
brew install cirruslabs/cli/tart
tart clone ghcr.io/cirruslabs/macos-ventura-base:latest ventura-base
tart clone ventura-base macos-testing
tart run macos-testing
```

- In macOS VM, clone this git repository

```shell
git clone https://github.com/isaharon/mac-playbook.git
```

- Run playbook as indicated in [usage](#usage)

## References

- https://github.com/geerlingguy/mac-dev-playbook
