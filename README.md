<h1 align="center">walruship/flash-development</h1>

<div align="center">
  <p>Docker's environment development</p>
  <a href="https://hub.docker.com/r/walruship/nginx" target="_blank"><img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white&longCache=true" alt="Docker Hub - Nginx" /></a>
  <a href="https://hub.docker.com/r/walruship/php" target="_blank"><img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white&longCache=true" alt="Docker Hub - PHP" /></a>
  <a href="https://hub.docker.com/_/mariadb" target="_blank"><img src="https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white&longCache=true" alt="Docker Hub - MariaDB" /></a>
</div>

## Table of contents
- [Docker Hub](#docker-hub)
- [Custom CLI Commands](#custom-cli-commands)
- [Credits](#credits)
- [License](#license)

## Docker Hub
View Dockerfiles:
- [walruship/nginx (Docker Hub)](https://hub.docker.com/r/walruship/nginx)
  - 1.23
- [walruship/nginx (Docker Hub)](https://hub.docker.com/r/walruship/php)
  - 8.1
  - 8.0
  - 7.4

## Custom CLI Commands
- `bin/bash`: Drop into the bash prompt of your Docker container. The `php` container should be mainly used to access the filesystem within Docker.
- `bin/cli`: Run any CLI command without going into the bash prompt. Ex. `bin/cli ls`
- `bin/clinotty`: Run any CLI command with no TTY. Ex. `bin/clinotty chmod u+x bin/bash`
- `bin/cliq`: The same as `bin/cli`, but pipes all output to `/dev/null`. Useful for a quiet CLI, or implementing long-running processes.
- `bin/composer`: Run the composer binary. Ex. `bin/composer install`
- `bin/copyfromcontainer`: Copy folders or files from container to host. Ex. `bin/copyfromcontainer vendor`
- `bin/copytocontainer`: Copy folders or files from host to container. Ex. `bin/copytocontainer --all`
- `bin/node`: Run the node binary. Ex. `bin/node --version`
- `bin/npm`: Run the npm binary. Ex. `bin/npm install`
- `bin/yarn`: Run the yarn binary. Ex. `bin/yarn install`
- `bin/remove`: Remove all containers.
- `bin/removeall`: Remove all containers, networks, volumes, and images.
- `bin/removevolumes`: Remove all volumes.
- `bin/restart`: Stop and then start all containers.
- `bin/root`: Run any CLI command as root without going into the bash prompt. Ex `bin/root apt-get install nano`
- `bin/rootnotty`: Run any CLI command as root with no TTY. Ex `bin/rootnotty chown -R app:app /var/www`
- `bin/setup-ssl`: Generate an SSL certificate for one or more domains. Ex. `bin/setup-ssl domain.test domain2.test`
- `bin/setup-ssl-ca`: Generate a certificate authority and copy it to the host.
- `bin/start`: Start all containers, good practice to use this instead of `docker-compose up -d`, as it may contain additional helpers.
- `bin/status`: Check the container status.
- `bin/stop`: Stop all containers.
- `bin/xdebug`: Disable or enable Xdebug. Accepts params `disable` (default) or `enable`. Ex. `bin/xdebug enable`

## Credits
Walruship Co,. Ltd and We are the creator of this repo.

You can follow us on Twitter <a href="https://twitter.com/walruship" target="_blank">@walruship</a>, connect with us on LinkedIn <a href="https://www.linkedin.com/in/walruship" target="_blank">@walruship</a>, read our website at <a href="https://walruship.com" target="_blank">https://walruship.com</a>, or contact us directly at <a href="mailto:contact@walruship.com">contact@walruship.com</a>.

## License
[MIT](https://opensource.org/licenses/MIT)