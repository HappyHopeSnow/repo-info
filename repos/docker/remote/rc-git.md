## `docker:rc-git`

```console
$ docker pull docker@sha256:e5b378f0dcbab8a4a724f0587ef013e5a5d4ecb9c51eca2d566a37db0ce17eee
```

-	Platforms:
	-	linux; amd64

### `docker:rc-git` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42111376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02df796309acddd017bb2377348c7a7e838b131580a5805fc7f5dc597c3694d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 27 Dec 2016 18:17:25 GMT
ADD file:92ab746eb22dd3ed2b87469c719adf3c1bed7302653bbd76baafd7cfd95e911e in / 
# Wed, 04 Jan 2017 21:04:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl
# Wed, 04 Jan 2017 21:04:11 GMT
ENV DOCKER_BUCKET=test.docker.com
# Mon, 16 Jan 2017 20:33:34 GMT
ENV DOCKER_VERSION=1.13.0-rc7
# Mon, 16 Jan 2017 20:33:34 GMT
ENV DOCKER_SHA256=beff8e0c5a235c0b9f374e4975401c793ceeca19332ffec965edb557ef7bfbc1
# Mon, 16 Jan 2017 20:33:38 GMT
RUN set -x 	&& curl -fSL "https://${DOCKER_BUCKET}/builds/Linux/x86_64/docker-${DOCKER_VERSION}.tgz" -o docker.tgz 	&& echo "${DOCKER_SHA256} *docker.tgz" | sha256sum -c - 	&& tar -xzvf docker.tgz 	&& mv docker/* /usr/local/bin/ 	&& rmdir docker 	&& rm docker.tgz 	&& docker -v
# Mon, 16 Jan 2017 20:33:38 GMT
COPY file:a8b1446f032ff01ac092c29a0af328f0b9d47bbee72d1049499f2a9a89ee988a in /usr/local/bin/ 
# Mon, 16 Jan 2017 20:33:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Jan 2017 20:33:39 GMT
CMD ["sh"]
# Mon, 16 Jan 2017 20:33:49 GMT
RUN apk add --no-cache 		git 		openssh-client
```

-	Layers:
	-	`sha256:0a8490d0dfd399b3a50e9aaa81dba0d425c3868762d46526b41be00886bcc28b`  
		Last Modified: Tue, 27 Dec 2016 18:19:22 GMT  
		Size: 1.9 MB (1902063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af50e60f15f49e6f8bd6fd84a5388b6de295a9e87ba9bc86878d04b5037d9b7`  
		Last Modified: Wed, 04 Jan 2017 23:28:13 GMT  
		Size: 2.2 MB (2166920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7963daa930c743dcb20a16b5342ff24732d4e907073433290e7e4880447fc293`  
		Last Modified: Mon, 16 Jan 2017 20:34:19 GMT  
		Size: 27.7 MB (27695764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3061553cad054aa8eb2de8be1e428e1862653033e53d892da91088a9c50690b`  
		Last Modified: Mon, 16 Jan 2017 20:34:09 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27d72251d922fa5c961b504b763a1618e12d2e0acec1cdafb96acfb464fd897`  
		Last Modified: Mon, 16 Jan 2017 20:36:28 GMT  
		Size: 10.3 MB (10346141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
