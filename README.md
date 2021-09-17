xxl-job-admin Image
=================

![GitHub Workflow Status](https://img.shields.io/github/workflow/status/chinayin-docker/xxl-job-admin/Docker%20Image%20CI)
![Docker Image Version (latest semver)](https://img.shields.io/docker/v/chinayin/xxl-job-admin?sort=semver)
![Docker Image Size (latest semver)](https://img.shields.io/docker/image-size/chinayin/xxl-job-admin?sort=semver)
![Docker Pulls](https://img.shields.io/docker/pulls/chinayin/xxl-job-admin)

A distributed task scheduling framework.（分布式任务调度平台XXL-JOB）

Usage
------------

You can use the image directly, e.g.

```bash
docker run --rm -it chinayin/xxl-job-admin:2.3.0
```

The images are built daily and have the security release enabled, so will contain any security updates released more
than 24 hours ago.

You can also use the images as a base for your own Dockerfile:

```bash
FROM chinayin/debian:xxl-job-admin:2.3.0
```
