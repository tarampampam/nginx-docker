<p align="center">
  <img alt="logo" src="https://hsto.org/webt/p-/z3/fq/p-z3fqd2gnxryhfy6pfpzlp_woe.png" width="110" />
</p>

# Docker image with [nginx][nginx]

[![Build Status][badge_build]][link_build]
[![Release Status][badge_release]][link_build]
[![Docker Pulls][badge_pulls]][link_docker_hub]
[![Issues][badge_issues]][link_issues]
[![License][badge_license]][link_license]

A little bit customized. Changes list:

- Default server config without unimportant comments
- Added `errorpages.conf` into `/etc/nginx` directory
- Custom error pages templates
- Fresh default index page with `favicon.ico` and `robots.txt`

Error pages sources and configs can be [found here][link_shared_content_branch].

## Supported tags

[![image stats](https://dockeri.co/image/tarampampam/nginx)][link_docker_tags]

All supported image tags [can be found here][link_docker_tags].

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

## Releasing

New versions publishing is very simple - just "publish" new release using repo releases page. Release version can be arbitrary.

All "supported" image versions defined in [releasing scenario](./.github/workflows/release.yml).

### License

WTFPL. Use anywhere for your pleasure.

[badge_build]:https://img.shields.io/github/workflow/status/tarampampam/nginx-docker/tests?maxAge=30&logo=github
[badge_release]:https://img.shields.io/github/workflow/status/tarampampam/nginx-docker/release?maxAge=30&label=release&logo=github
[badge_pulls]:https://img.shields.io/docker/pulls/tarampampam/nginx.svg?maxAge=30
[badge_issues]:https://img.shields.io/github/issues/tarampampam/nginx-docker.svg?maxAge=30
[badge_license]:https://img.shields.io/github/license/tarampampam/nginx-docker.svg?maxAge=30

[link_build]:https://github.com/tarampampam/nginx-docker/actions
[link_docker_hub]:https://hub.docker.com/r/tarampampam/nginx/
[link_docker_tags]:https://hub.docker.com/r/tarampampam/nginx/tags
[link_license]:https://github.com/tarampampam/nginx-docker/blob/master/LICENSE
[link_issues]:https://github.com/tarampampam/nginx-docker/issues
[link_shared_content_branch]:./content
[nginx]:https://nginx.org/
