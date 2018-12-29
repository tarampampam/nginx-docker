# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog][keepachangelog] and this project adheres to [Semantic Versioning][semver].

## 18.12.29

### Changed

- Dockerfiles moved onto protected branches (like `image-*`)
- [Docker hub][own_docker_hub] now use single rule for all images builds:
  - Type: `branch`
  - Name: `/^image\-(.+)$/`
  - Dockerfile location: `/`
  - Docker Tag Name: `{\1}`
- Licence type changed from `MIT` to `WTFPL` :)

### Added

- Protected branch named `shared-content` for static content - error pages, default configs
- Automatic rebuilding (once in a 2 weeks, plus/minus; used `gitlab.com` "Scheduling Pipelines" for calling triggers on `hub.docker.com`) for next images *(tags)*:
  - `1.11`
  - `1.12`
  - `1.13`
  - `1.14`
  - `1.15`
  - `1.11-alpine`
  - `1.12-alpine`
  - `1.13-alpine`
  - `1.14-alpine`
  - `1.15-alpine`
  - `stable`

## 18.9.11

### Added

- `.git*` files
- Dockerfile for `latest`
- Dockerfile for `stable-alpine`

[own_docker_hub]:https://hub.docker.com/r/tarampampam/nginx
[keepachangelog]:https://keepachangelog.com/en/1.0.0/
[semver]:https://semver.org/spec/v2.0.0.html
