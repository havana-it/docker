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

#### 3) Your app is now accessible at http://www.localhost.dev:8088

### Customizing

The server configuration file is mounted from `env/nginx/server.conf`.

#### You can modify it to your needs, for example changing the server name:

```nginx
# env/nginx/server.conf

server {
    # ...
    server_name acme.dev www.acme.dev;
    # ...
}
```

#### Don't forget to update your `/etc/hosts` file with the new server name:

```
# /etc/hosts

127.0.0.1 acme.dev www.acme.dev
```

#### Restart services 

```bash
$ docker-compose restart
```

#### Your app is now accessible at http://www.acme.dev:8088
