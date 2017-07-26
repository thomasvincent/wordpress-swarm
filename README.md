# wordpress-swarm

[![standard-readme compliant](https://img.shields.io/badge/standard--readme-OK-green.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)
TODO: Put more badges here.

> Running Wordpress in docker swarm-mode using DNS name-based discovery

This project will create four services in a Docker swarm cluster:
* A wordpress instance with labels for Traefik to load-balance
* One MariaDB database configured for Galera-based clustering using swarm mode DNS for discovery
* One Traefik proxying/load balancing container 

## Table of Contents

- [Security](#security)
- [Testing](#testing)
- [Background](#background)
- [Install](#install)
- [Usage](#usage)
- [Maintainers](#maintainers)
- [Contribute](#contribute)
- [License](#license)

## Security

## Testing

## Background

## Install

```
docker stack deploy --compose-file docker-stack.yml wordpress
```

## Usage

To see an example of scaling up Galera to 3 nodes, execute:
```
docker service scale wordpress_dbcluster=3
```
When finished, the following command shuts everything down:
```
docker service rm wpcluster wordpress
```

## Maintainers

[@thomasvincent](https://github.com/thomasvincent)

## Contribute

See [the contribute file](contribute.md)!

PRs accepted.

Small note: If editing the README, please conform to the [standard-readme](https://github.com/RichardLitt/standard-readme) specification.

## License

Apache 2.0 License © 2017 Thomas Vincent