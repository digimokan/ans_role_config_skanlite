# ans_role_config_skanlite

Install and configure the Skanlite image-scanning application.

[![Release](https://img.shields.io/github/release/digimokan/ans_role_config_skanlite.svg?label=release)](https://github.com/digimokan/ans_role_config_skanlite/releases/latest "Latest Release Notes")
[![License](https://img.shields.io/badge/license-MIT-blue.svg?label=license)](LICENSE.md "Project License")

## Table Of Contents

* [Purpose](#purpose)
* [Requirements](#requirements)
* [Supported Operating Systems](#supported-operating-systems)
* [Quick Start](#quick-start)
    * [Use From Playbook](#use-from-playbook)
* [Contributing](#contributing)

## Purpose

* Install and configure [Skanlite](https://apps.kde.org/skanlite/), the KDE
  image and document-scanning application.

## Requirements

* Scanners have been configured with manually-installed drivers, or with
  [IPP Everywhere](https://www.pwg.org/ipp/everywhere.html) "driverless"
  scanning protocol.

## Supported Operating Systems

* FreeBSD.

## Quick Start

### Use From Playbook

1. Create `requirements.yml` in ansible project root, and add this content:

   ```yaml
   # requirements.yml
   - src: https://github.com/digimokan/ans_role_config_skanlite
   ```

2. From the project root directory, install/download the role:

   ```shell
   $ ansible-galaxy install --role-file requirements.yml --roles-path ./roles --force-with-deps
   ```

   * _NOTE:_ `--force-with-deps` _ensures subsequent calls download updates_

3. Include the role like any local role, from the project playbook:

   ```yaml
   # playbook.yml
   - hosts: localhost
     connection: local
     tasks:
       - name: "Install and configure the Scanlite scanning application"
         ansible.builtin.include_role:
           name: ans_role_config_skanlite
   ```

## Contributing

* Feel free to report a bug or propose a feature by opening a new
  [Issue](https://github.com/digimokan/ans_role_config_skanlite/issues).
* Follow the project's [Contributing](CONTRIBUTING.md) guidelines.
* Respect the project's [Code Of Conduct](CODE_OF_CONDUCT.md).

