## Usage

### First run

#### 1) Copy the files in your web application root

ex:

```bash
$ cp -v {env,docker-compose.yml} /var/www/acme
```

#### 2) Run [docker-compose](https://docs.docker.com/compose/) to build your stack

```bash
$ cd /var/www/acme
$ docker-compose up -d
```
