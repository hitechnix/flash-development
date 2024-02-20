# Flash Development

This repository allows you to quickly get a development environment up and running using Docker, including a MySQL,
PostgreSQL
database and some debugging tools.

This environment includes the latest versions of the following software:

- `nginx`
- `phpfpm`
- `mariadb`
- `postgresql`
- `xdebug`

### 📦 Requirements

The Docker & Docker Compose system requirements are Linux Ubuntu as the OS (other operating systems are supported as
well), an absolute minimum 512MB RAM (2GB recommended)

In order to install docker Ubuntu, you will need to meet the following requirements:

- OS: Linux Ubuntu
- Memory: 512MB RAM (2GB Recommended)
- Disk: Sufficient amount to run the Docker containers you wish to use
- CPU: Dependant on the applications you wish to run in the containers

### 📋 Features

- Easy switch between PHP versions: 8.3, 8.2, 8.1, 8.0, 7.4, 7.3, 7.2, 7.1, 5.6…
- Choose your favorite database engine: MySQL, Postgres, MariaDB…
- Run your own stack: Memcached, HHVM, RabbitMQ…
- Each software runs on its own container: PHP-FPM, NGINX, PHP-CLI…
- Easy to customize any container, with simple edit to the Dockerfile.
- All Images extend from an official base Image. (Trusted base Images).
- Pre-configured NGINX to host any code at your root directory.
- Can use per project,or single for all projects.
- Easy to install/remove software’s in Containers using environment variables.
- Clean and well-structured Dockerfiles (Dockerfile).
- Latest version of the Docker Compose file (docker-compose).
- Everything is visible and editable.
- Fast Images Builds.

### 🔧 Installation

1. Install Docker and Docker-Compose

- [Docker Install documentation](https://docs.docker.com/install/)
- [Docker-Compose Install documentation](https://docs.docker.com/compose/install/)

2. Bring up your stack by running

```shell
git clone https://github.com/hitechnix/flash-development.git \
    && cd flash-development \
    && cp .env.example .env
```

3. Edit environment variable

```dotenv
# Nginx
NGINX_PORT=
NGINX_HTTPS_PORT=

# PHP
BLACKFIRE_CLIENT_ID=
BLACKFIRE_CLIENT_TOKEN=
COMPOSER_DISABLE_XDEBUG_WARN=1
PHP_CS_FIXER_IGNORE_ENV=1

# MariaDB
MARIA_DB_PORT=3306
MYSQL_ROOT_PASSWORD=root

# PostgreSQL
POSTGRES_DB_PORT=5432
POSTGRES_USER=root
POSTGRES_PASSWORD=root
```

4. Start application

```shell
docker-compose up -d
```

### 📝 Usage

Reader-friendly documentation can be found [here][link-docs].

### 📨 Message

I hope you find this useful. If you have any questions, please create an issue.

### 🔐 Security

If you discover any security related issues, please email support@hitechnix.com instead of using the issue tracker.

### 📖 License

This software is released under the [BSD 3-Clause][link-license] License. Please see the [LICENSE](LICENSE) file
or https://opensource.hitechnix.com/LICENSE.txt for more information.

### ✨ Contributors

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <td align="center" valign="top" width="14.28%">
    <a href="https://trants.io">
      <img src="https://avatars.githubusercontent.com/u/40693126?v=4?s=100" width="100px;" alt="Son Tran Thanh" />
      <br />
      <sub>
        <b>Son Tran Thanh</b>
      </sub>
    </a>
    <br />
    <a href="#maintenance-trants" title="Maintenance">🚧</a>
    <a href="https://github.com/hitechnix/flash-development/commits?author=trants" title="Code">💻</a>
  </td>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://allcontributors.org) specification.
Contributions of any kind welcome!

[link-docs]:https://opensource.hitechnix.com/flash-development

[link-license]: https://opensource.org/license/bsd-3-clause
