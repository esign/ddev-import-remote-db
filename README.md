[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/esign/ddev-import-remote-db/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/esign/ddev-import-remote-db/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/esign/ddev-import-remote-db)](https://github.com/esign/ddev-import-remote-db/commits)
[![release](https://img.shields.io/github/v/release/esign/ddev-import-remote-db)](https://github.com/esign/ddev-import-remote-db/releases/latest)

# DDEV Import Remote Db

## Overview

This add-on allows you to import a remote MySQL database into your local [DDEV](https://ddev.com/) database.
It supports direct connections as well as SSH tunneling for secure access to remote databases.

## Installation

```bash
ddev add-on get esign/ddev-import-remote-db
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

## Usage

| Command | Description |
| ------- | ----------- |
| `ddev describe` | View service status and used ports for Import Remote Db |
| `ddev logs -s import-remote-db` | Check Import Remote Db logs |

## Advanced Customization

To change the Docker image:

```bash
ddev dotenv set .ddev/.env.import-remote-db --import-remote-db-docker-image="ddev/ddev-utilities:latest"
ddev add-on get esign/ddev-import-remote-db
ddev restart
```

Make sure to commit the `.ddev/.env.import-remote-db` file to version control.

All customization options (use with caution):

| Variable | Flag | Default |
| -------- | ---- | ------- |
| `IMPORT_REMOTE_DB_DOCKER_IMAGE` | `--import-remote-db-docker-image` | `ddev/ddev-utilities:latest` |

## Credits

**Contributed and maintained by [@esign](https://github.com/esign)**
