<!--

********************************************************************************

WARNING:

    DO NOT EDIT "alpine/README.md"

    IT IS AUTO-GENERATED

    (from the other files in "alpine/" combined with a set of templates)

********************************************************************************

-->

# Supported tags and respective `Dockerfile` links

-	[`3.6` (*versions/library-3.6/x86_64/Dockerfile*)](https://github.com/gliderlabs/docker-alpine/blob/2127169e2d9dcbb7ae8c7eca599affd2d61b49a7/versions/library-3.6/x86_64/Dockerfile)
-	[`3.7`, `latest` (*versions/library-3.7/x86_64/Dockerfile*)](https://github.com/gliderlabs/docker-alpine/blob/61c3181ad3127c5bedd098271ac05f49119c9915/versions/library-3.7/x86_64/Dockerfile)
-	[`edge` (*versions/library-edge/x86_64/Dockerfile*)](https://github.com/gliderlabs/docker-alpine/blob/edd30a358e57a880645e25a83e9d9bd79bff06f5/versions/library-edge/x86_64/Dockerfile)
-	[`3.1` (*versions/library-3.1/Dockerfile*)](https://github.com/gliderlabs/docker-alpine/blob/62606823dbae10f763dae1878f44ec918ac8dce5/versions/library-3.1/Dockerfile)
-	[`3.2` (*versions/library-3.2/Dockerfile*)](https://github.com/gliderlabs/docker-alpine/blob/41ee859116107fe6e45487afddbf773c09fe5e41/versions/library-3.2/Dockerfile)
-	[`3.3` (*versions/library-3.3/Dockerfile*)](https://github.com/gliderlabs/docker-alpine/blob/3683598b841a0bbdd4a892ff575e60e02119d37d/versions/library-3.3/Dockerfile)
-	[`3.4` (*versions/library-3.4/Dockerfile*)](https://github.com/gliderlabs/docker-alpine/blob/eaf8d6dd72bacb1d739bcfee475eda78c70e3ecc/versions/library-3.4/Dockerfile)
-	[`3.5` (*versions/library-3.5/Dockerfile*)](https://github.com/gliderlabs/docker-alpine/blob/791bc2db0eef96f9a90b662079114a5eb5a2ffc2/versions/library-3.5/Dockerfile)

# Quick reference

-	**Where to get help**:  
	[the Docker Community Forums](https://forums.docker.com/), [the Docker Community Slack](https://blog.docker.com/2016/11/introducing-docker-community-directory-docker-community-slack/), or [Stack Overflow](https://stackoverflow.com/search?tab=newest&q=docker)

-	**Where to file issues**:  
	[https://github.com/gliderlabs/docker-alpine/issues](https://github.com/gliderlabs/docker-alpine/issues)

-	**Maintained by**:  
	[Glider Labs](https://github.com/gliderlabs/docker-alpine) (an Alpine community contributor)

-	**Supported architectures**: ([more info](https://github.com/docker-library/official-images#architectures-other-than-amd64))  
	[`amd64`](https://hub.docker.com/r/amd64/alpine/), [`arm32v6`](https://hub.docker.com/r/arm32v6/alpine/), [`arm64v8`](https://hub.docker.com/r/arm64v8/alpine/), [`i386`](https://hub.docker.com/r/i386/alpine/), [`ppc64le`](https://hub.docker.com/r/ppc64le/alpine/), [`s390x`](https://hub.docker.com/r/s390x/alpine/)

-	**Published image artifact details**:  
	[repo-info repo's `repos/alpine/` directory](https://github.com/docker-library/repo-info/blob/master/repos/alpine) ([history](https://github.com/docker-library/repo-info/commits/master/repos/alpine))  
	(image metadata, transfer size, etc)

-	**Image updates**:  
	[official-images PRs with label `library/alpine`](https://github.com/docker-library/official-images/pulls?q=label%3Alibrary%2Falpine)  
	[official-images repo's `library/alpine` file](https://github.com/docker-library/official-images/blob/master/library/alpine) ([history](https://github.com/docker-library/official-images/commits/master/library/alpine))

-	**Source of this description**:  
	[docs repo's `alpine/` directory](https://github.com/docker-library/docs/tree/master/alpine) ([history](https://github.com/docker-library/docs/commits/master/alpine))

-	**Supported Docker versions**:  
	[the latest release](https://github.com/docker/docker-ce/releases/latest) (down to 1.6 on a best-effort basis)

# What is Alpine Linux?

[Alpine Linux](http://alpinelinux.org/) is a Linux distribution built around [musl libc](http://www.musl-libc.org/) and [BusyBox](http://www.busybox.net/). The image is only 5 MB in size and has access to a [package repository](http://forum.alpinelinux.org/packages) that is much more complete than other BusyBox based images. This makes Alpine Linux a great image base for utilities and even production applications. [Read more about Alpine Linux here](https://www.alpinelinux.org/about/) and you can see how their mantra fits in right at home with Docker images.

![logo](https://raw.githubusercontent.com/docker-library/docs/781049d54b1bd9b26d7e8ad384a92f7e0dcb0894/alpine/logo.png)

# How to use this image

## Usage

Use like you would any other base image:

```dockerfile
FROM alpine:3.5
RUN apk add --no-cache mysql-client
ENTRYPOINT ["mysql"]
```

This example has a virtual image size of only 36.5MB. Compare that to our good friend Ubuntu:

```dockerfile
FROM ubuntu:16.04
RUN apt-get update \
    && apt-get install -y --no-install-recommends mysql-client \
    && rm -rf /var/lib/apt/lists/*
ENTRYPOINT ["mysql"]
```

This yields us a virtual image size of about 184MB image.

## Documentation

This image is well documented. [Check out the documentation at Viewdocs](http://gliderlabs.viewdocs.io/docker-alpine).

# License

View [license information](https://pkgs.alpinelinux.org) for the software contained in this image.

As with all Docker images, these likely also contain other software which may be under other licenses (such as Bash, etc from the base distribution, along with any direct or indirect dependencies of the primary software being contained).

Some additional license information which was able to be auto-detected might be found in [the `repo-info` repository's `alpine/` directory](https://github.com/docker-library/repo-info/tree/master/repos/alpine).

As for any pre-built image usage, it is the image user's responsibility to ensure that any use of this image complies with any relevant licenses for all software contained within.
