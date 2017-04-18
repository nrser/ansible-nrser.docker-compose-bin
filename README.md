nrser.docker-compose-bin [QB][]/Ansible Role
=============================================================================

Install [Docker Compose][] from the binary on their GitHub [releases][] page.


Compatibility
-----------------------------------------------------------------------------

-   Architecture (`ansible_architecture` fact)
    -   `x86_64`
        -   System (`ansible_system` fact)
            -   Darwin: **YES**
                -   Tested on macOS Sierra 10.12.4.
            -   Linux: **PROBABLY**
                -   Untested but I don't see why it wouldn't work.
            -   Windows: **NO**
                -   I don't have any Windows.
    -   Others
        -   **NO** - no binaries provided by Docker Compose at time of writing.


Motivation
-----------------------------------------------------------------------------

The standard Docker Compose install that comes with [Docker for Mac][] depends on the [docker Python package][], which conflicts with the [docker-py][] library that Ansible uses.

Using the Docker Compose binary allows you to remove the `docker` Python package and install `docker-py`, keeping Ansible happy.


Installation
-----------------------------------------------------------------------------

If you're using [QB][]:

    qb install nrser.docker-compose-bin

Otherwise, something like

    git clone https://github.com/nrser/ansible-nrser.docker-compose-bin.git <ANSIBLE_ROLES_DIR>/nrser.docker-compose-bin


Usage
-----------------------------------------------------------------------------

see

    qb nrser.docker-compose-bin --help

or add as a role in a playbook:

```YAML
- role: nrser.docker-compose-bin
```

see [`meta/qb.yml`](meta/qb.yml) or [`defaults/main.yml`](defaults/main.yml) for options.


License
-----------------------------------------------------------------------------

ISC


[QB]: https://github.com/nrser/qb
[Docker Compose]: https://github.com/docker/compose
[releases]: https://github.com/docker/compose/releases
[Docker for Mac]: https://docs.docker.com/docker-for-mac/
[docker-py]: https://pypi.python.org/pypi/docker-py
[docker Python package]: https://pypi.python.org/pypi/docker
