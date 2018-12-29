<p align="center">
  <img alt="logo" src="https://hsto.org/webt/p-/z3/fq/p-z3fqd2gnxryhfy6pfpzlp_woe.png" width="70" height="70" />
</p>

# Docker image with [nginx][nginx]

[![Build][badge_automated]][link_hub]
[![Build][badge_build]][link_hub]
[![Docker Pulls][badge_pulls]][link_hub]
[![Issues][badge_issues]][link_issues]
[![License][badge_license]][link_license]

A little bit customized. Changes list:

- Default server config without unimportant comments
- Added `errorpages.conf` into `/etc/nginx` directory
- Custom error pages templates
- Fresh default index page with `favicon.ico` and `robots.txt`

Error pages sources and configs can be [found here][link_shared_content_branch].

> Page on `hub.docker.com` can be [found here][link_hub].

Supported tags:

Tag name        | Details | Full image name | Dockerfile
:-------------: | :-----: | :-------------: | :--------:
`latest`        | ![Size][badge_size_latest] | `tarampampam/nginx:latest` | [link][dockerfile_latest]
`stable`        | ![Size][badge_size_stable] | `tarampampam/nginx:stable` | [link][dockerfile_stable]
`1.11`          | ![Size][badge_size_1_11] | `tarampampam/nginx:1.11` | [link][dockerfile_1_11]
`1.12`          | ![Size][badge_size_1_12] | `tarampampam/nginx:1.12` | [link][dockerfile_1_12]
`1.13`          | ![Size][badge_size_1_13] | `tarampampam/nginx:1.13` | [link][dockerfile_1_13]
`1.14`          | ![Size][badge_size_1_14] | `tarampampam/nginx:1.14` | [link][dockerfile_1_14]
`1.15`          | ![Size][badge_size_1_15] | `tarampampam/nginx:1.15` | [link][dockerfile_1_15]
`stable-alpine` | ![Size][badge_size_stable_alpine] | `tarampampam/nginx:stable-alpine` | [link][dockerfile_stable_alpine]
`1.11-alpine`   | ![Size][badge_size_1_11_alpine] | `tarampampam/nginx:1.11-alpine` | [link][dockerfile_1_11_alpine]
`1.12-alpine`   | ![Size][badge_size_1_12_alpine] | `tarampampam/nginx:1.12-alpine` | [link][dockerfile_1_12_alpine]
`1.13-alpine`   | ![Size][badge_size_1_13_alpine] | `tarampampam/nginx:1.13-alpine` | [link][dockerfile_1_13_alpine]
`1.14-alpine`   | ![Size][badge_size_1_14_alpine] | `tarampampam/nginx:1.14-alpine` | [link][dockerfile_1_14_alpine]
`1.15-alpine`   | ![Size][badge_size_1_15_alpine] | `tarampampam/nginx:1.15-alpine` | [link][dockerfile_1_15_alpine]

[badge_size_latest]:https://images.microbadger.com/badges/image/tarampampam/nginx.svg
[badge_size_stable]:https://images.microbadger.com/badges/image/tarampampam/nginx:stable.svg
[badge_size_1_11]:https://images.microbadger.com/badges/image/tarampampam/nginx:1.11.svg
[badge_size_1_12]:https://images.microbadger.com/badges/image/tarampampam/nginx:1.12.svg
[badge_size_1_13]:https://images.microbadger.com/badges/image/tarampampam/nginx:1.13.svg
[badge_size_1_14]:https://images.microbadger.com/badges/image/tarampampam/nginx:1.14.svg
[badge_size_1_15]:https://images.microbadger.com/badges/image/tarampampam/nginx:1.15.svg
[badge_size_stable_alpine]:https://images.microbadger.com/badges/image/tarampampam/nginx:stable-alpine.svg
[badge_size_1_11_alpine]:https://images.microbadger.com/badges/image/tarampampam/nginx:1.11-alpine.svg
[badge_size_1_12_alpine]:https://images.microbadger.com/badges/image/tarampampam/nginx:1.12-alpine.svg
[badge_size_1_13_alpine]:https://images.microbadger.com/badges/image/tarampampam/nginx:1.13-alpine.svg
[badge_size_1_14_alpine]:https://images.microbadger.com/badges/image/tarampampam/nginx:1.14-alpine.svg
[badge_size_1_15_alpine]:https://images.microbadger.com/badges/image/tarampampam/nginx:1.15-alpine.svg

[dockerfile_latest]:https://github.com/tarampampam/nginx-docker/blob/image-latest/Dockerfile
[dockerfile_stable]:https://github.com/tarampampam/nginx-docker/blob/image-stable/Dockerfile
[dockerfile_1_11]:https://github.com/tarampampam/nginx-docker/blob/image-1.11/Dockerfile
[dockerfile_1_12]:https://github.com/tarampampam/nginx-docker/blob/image-1.12/Dockerfile
[dockerfile_1_13]:https://github.com/tarampampam/nginx-docker/blob/image-1.13/Dockerfile
[dockerfile_1_14]:https://github.com/tarampampam/nginx-docker/blob/image-1.14/Dockerfile
[dockerfile_1_15]:https://github.com/tarampampam/nginx-docker/blob/image-1.15/Dockerfile
[dockerfile_stable_alpine]:https://github.com/tarampampam/nginx-docker/blob/image-stable-alpine/Dockerfile
[dockerfile_1_11_alpine]:https://github.com/tarampampam/nginx-docker/blob/image-1.11-alpine/Dockerfile
[dockerfile_1_12_alpine]:https://github.com/tarampampam/nginx-docker/blob/image-1.12-alpine/Dockerfile
[dockerfile_1_13_alpine]:https://github.com/tarampampam/nginx-docker/blob/image-1.13-alpine/Dockerfile
[dockerfile_1_14_alpine]:https://github.com/tarampampam/nginx-docker/blob/image-1.14-alpine/Dockerfile
[dockerfile_1_15_alpine]:https://github.com/tarampampam/nginx-docker/blob/image-1.15-alpine/Dockerfile

## How can I use this?

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

![Screen shot](https://hsto.org/webt/yz/sw/kq/yzswkqi-4nuyql4kaumnczvjjy8.png)
![Screen shot](https://hsto.org/webt/by/qu/xz/byquxz7nxaj8bbnl08nwpncf-oi.png)

### License

WTFPL. Use anywhere for your pleasure.

[badge_automated]:https://img.shields.io/docker/automated/tarampampam/nginx.svg?style=flat-square&maxAge=30
[badge_pulls]:https://img.shields.io/docker/pulls/tarampampam/nginx.svg?style=flat-square&maxAge=30
[badge_issues]:https://img.shields.io/github/issues/tarampampam/nginx-docker.svg?style=flat-square&maxAge=30
[badge_build]:https://img.shields.io/docker/build/tarampampam/nginx.svg?style=flat-square&maxAge=30
[badge_license]:https://img.shields.io/github/license/tarampampam/nginx-docker.svg?style=flat-square&maxAge=30
[link_base_nginx_image]:https://hub.docker.com/_/nginx?tab=tags
[link_hub]:https://hub.docker.com/r/tarampampam/nginx/
[link_license]:https://github.com/tarampampam/nginx-docker/blob/master/LICENSE
[link_issues]:https://github.com/tarampampam/nginx-docker/issues
[link_shared_content_branch]:https://github.com/tarampampam/nginx-docker/tree/shared-content
[nginx]:https://nginx.org/
