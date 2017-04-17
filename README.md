nrser.docker-compose-bin
========================

Install [Docker Compose][] from the binary on their GitHub [releases][] page.

Seems to work for macOS x86_64. should probably work on Linux x86_64. Won't work for the Windows version.

The standard Docker Compose install depends on the [docker Python package][], which conflicts with the [docker-py][] library that Ansible uses.

Using the Docker Compose binary allows you to remove the `docker` Python package and install `docker-py`, keeping Ansible happy.

[Docker Compose]: https://github.com/docker/compose
[releases]: https://github.com/docker/compose/releases
[docker-py]: https://pypi.python.org/pypi/docker-py
[docker Python package]: https://pypi.python.org/pypi/docker
