<p align="center">
  <img alt="logo" src="https://hsto.org/webt/p-/z3/fq/p-z3fqd2gnxryhfy6pfpzlp_woe.png" width="70" height="70" />
</p>

# Docker image with [nginx][nginx]

[![Build][badge_build]][link_build]
[![Stars][badge_pulls]][link_pulls]
[![License][badge_license]][link_license]
[![Issues][badge_issues]][link_issues]

A little bit customized. Changes list:

- Default server config without unimportant comments
- Added `errorpages.conf` into `/etc/nginx` directory
- Custom error pages templates
- Fresh default index page with `favicon.ico` and `robots.txt`

### How can I use this?

Pull latest image:

```bash
$ docker pull tarampampam/nginx:stable-alpine
# or
$ docker pull tarampampam/nginx:latest
```

And then you can:

```bash
$ docker run --rm tarampampam/nginx:stable-alpine nginx -v
  nginx version: nginx/1.14.0
$ docker run --rm -p 8080:80 tarampampam/nginx:stable-alpine nginx -g 'daemon off;'
```

And open in your favorite browser [127.0.0.1:8080](http://127.0.0.1:8080/).

### Local image building

You can use next commands:

```bash
$ docker build -t custom-nginx -f ./Dockerfile.stable-alpine .
$ docker run --rm -p 8080:80 custom-nginx nginx -g 'daemon off;'
```

#### License

MIT. Use anywhere for your pleasure.

[badge_build]:https://img.shields.io/docker/build/tarampampam/nginx.svg?style=flat&maxAge=30
[badge_pulls]:https://img.shields.io/docker/pulls/tarampampam/nginx.svg?style=flat&maxAge=30
[badge_license]:https://img.shields.io/github/license/tarampampam/nginx-docker.svg?style=flat&maxAge=30
[badge_issues]:https://img.shields.io/github/issues/tarampampam/nginx-docker.svg?style=flat&maxAge=30
[link_build]:https://hub.docker.com/r/tarampampam/nginx/builds/
[link_pulls]:https://hub.docker.com/r/tarampampam/nginx/
[link_license]:https://github.com/tarampampam/nginx-docker/blob/master/LICENSE
[link_issues]:https://github.com/tarampampam/nginx-docker/issues
[docker_hub]:https://hub.docker.com/r/tarampampam/nginx-docker/
[nginx]:https://nginx.org/
