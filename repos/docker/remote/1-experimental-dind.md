## `docker:1-experimental-dind`

```console
$ docker pull docker@sha256:50484bbedab068e778d3356092f7a1a9efe96cffbed9a6d90be94b0ada81815f
```

-	Platforms:
	-	linux; amd64

### `docker:1-experimental-dind` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34242951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff51b3124dfd274cb2861cd41dbf7598529d898d2d9ad764d08ed87d6dd6d20`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 27 Dec 2016 18:17:13 GMT
ADD file:eeed5f514a35d18fcd9cbfe6c40c582211020bffdd53e4799018d33826fe5067 in / 
# Tue, 27 Dec 2016 18:36:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl
# Tue, 27 Dec 2016 18:36:57 GMT
ENV DOCKER_BUCKET=experimental.docker.com
# Wed, 11 Jan 2017 03:24:21 GMT
ENV DOCKER_VERSION=1.12.6
# Wed, 11 Jan 2017 03:24:21 GMT
ENV DOCKER_SHA256=7f0c0fee0a302a4c3b6f62f9ed063813976200386b2299b36db52a6b67994674
# Wed, 11 Jan 2017 03:24:26 GMT
RUN set -x 	&& curl -fSL "https://${DOCKER_BUCKET}/builds/Linux/x86_64/docker-${DOCKER_VERSION}.tgz" -o docker.tgz 	&& echo "${DOCKER_SHA256} *docker.tgz" | sha256sum -c - 	&& tar -xzvf docker.tgz 	&& mv docker/* /usr/local/bin/ 	&& rmdir docker 	&& rm docker.tgz 	&& docker -v
# Wed, 11 Jan 2017 03:24:26 GMT
COPY file:399605dc1850a60a586b5494ab538bad495fd6f94eabca0c5f8a26468ce6030f in /usr/local/bin/ 
# Wed, 11 Jan 2017 03:24:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Jan 2017 03:24:27 GMT
CMD ["sh"]
# Wed, 11 Jan 2017 03:24:29 GMT
RUN apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		xfsprogs 		xz
# Wed, 11 Jan 2017 03:24:30 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Wed, 11 Jan 2017 03:24:31 GMT
ENV DIND_COMMIT=3b5fac462d21ca164b3778647420016315289034
# Wed, 11 Jan 2017 03:24:32 GMT
RUN wget "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind" -O /usr/local/bin/dind 	&& chmod +x /usr/local/bin/dind
# Wed, 11 Jan 2017 03:24:32 GMT
COPY file:7070e4b35c137a8ec5904300d19b8f7ee74aa76659517767c617249cece98a4a in /usr/local/bin/ 
# Wed, 11 Jan 2017 03:24:33 GMT
VOLUME [/var/lib/docker]
# Wed, 11 Jan 2017 03:24:33 GMT
EXPOSE 2375/tcp
# Wed, 11 Jan 2017 03:24:33 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 11 Jan 2017 03:24:33 GMT
CMD []
```

-	Layers:
	-	`sha256:b7f33cc0b48ea4fb2f0745def58c25483a5f6b7aed5b41ce8f1cb6e17f5723cf`  
		Last Modified: Tue, 27 Dec 2016 18:18:49 GMT  
		Size: 2.3 MB (2313090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1438997aafae96dc7e9ae08d25a298432204c909dbf82d191d5372d8be867fec`  
		Last Modified: Tue, 27 Dec 2016 18:37:58 GMT  
		Size: 915.7 KB (915672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453645374b4731f9b386af4256a9bf5987a6b4a46ac15129938c132d0edd8723`  
		Last Modified: Wed, 11 Jan 2017 03:30:19 GMT  
		Size: 28.9 MB (28945031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d486dc75fe765f5b88bf07f3477dd9ca7806952d376a9270051ac3058f20662`  
		Last Modified: Wed, 11 Jan 2017 03:30:08 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6aa6b0fa72788dba6fa729a0a173ad4598aad3b3a45f38d4e480c5b40496492`  
		Last Modified: Wed, 11 Jan 2017 03:31:22 GMT  
		Size: 2.1 MB (2065044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5957f662dafb3f23c9d40f6068d8b9f8d34144c9a5a98453c03e975f953038c`  
		Last Modified: Wed, 11 Jan 2017 03:31:20 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a704ffce55db70019ba548394751e3bd7142f94a02f1b773dc782eac680f34`  
		Last Modified: Wed, 11 Jan 2017 03:31:20 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73e3dc6ef191d47432f5bbe8f63b8631e69e42603c55191d429880510c97939`  
		Last Modified: Wed, 11 Jan 2017 03:31:20 GMT  
		Size: 481.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
