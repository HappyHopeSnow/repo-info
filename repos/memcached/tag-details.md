<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1.4.34`](#memcached1434)
-	[`memcached:1.4`](#memcached14)
-	[`memcached:1`](#memcached1)
-	[`memcached:latest`](#memcachedlatest)
-	[`memcached:1.4.34-alpine`](#memcached1434-alpine)
-	[`memcached:1.4-alpine`](#memcached14-alpine)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:alpine`](#memcachedalpine)

## `memcached:1.4.34`

```console
$ docker pull memcached@sha256:7f702ad1a68dc999b8f277150b695dc0e3b70f50a4a383afd3dc4e9538d9bf42
```

-	Platforms:
	-	linux; amd64

### `memcached:1.4.34` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52239686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a10d7823aad82ace39b6d0eaf8d36bf018198a75bfe35cd716fdcebaafdf34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 01:03:06 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Wed, 14 Dec 2016 01:03:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libevent-2.0-5 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 18:10:29 GMT
ENV MEMCACHED_VERSION=1.4.34
# Fri, 13 Jan 2017 18:10:29 GMT
ENV MEMCACHED_SHA1=7c7214f5183c6e20c22b243e21ed1ffddb91497e
# Fri, 13 Jan 2017 18:10:50 GMT
RUN buildDeps=' 		gcc 		libc6-dev 		libevent-dev 		make 		perl 		wget 	' 	&& set -x 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& wget -O memcached.tar.gz "http://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 	&& cd /usr/src/memcached 	&& ./configure 	&& make -j$(nproc) 	&& make install 	&& cd / && rm -rf /usr/src/memcached 	&& apt-get purge -y --auto-remove $buildDeps
# Fri, 13 Jan 2017 18:10:51 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Fri, 13 Jan 2017 18:10:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 13 Jan 2017 18:10:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 18:10:53 GMT
USER [memcache]
# Fri, 13 Jan 2017 18:10:53 GMT
EXPOSE 11211/tcp
# Fri, 13 Jan 2017 18:10:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b78be39d94d164800f0c9a2e4a617b2281dbbfab6c2a68e9550d1b94d5c314`  
		Last Modified: Mon, 19 Dec 2016 23:56:48 GMT  
		Size: 2.0 KB (2040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a68c6a8c3a07df4f5a8965bdb4c7a1e31e4c37eaa976e8333f9e1c370bfbafe`  
		Last Modified: Mon, 19 Dec 2016 23:56:47 GMT  
		Size: 237.9 KB (237938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e722127a5c096fe498931871e0f69762ba2081106fec8afc60443bb3933ed5b`  
		Last Modified: Fri, 13 Jan 2017 18:11:26 GMT  
		Size: 636.2 KB (636175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d261dd099866d75d9c11e3dcb7042277336c708b8058c03681e623711723ac9d`  
		Last Modified: Fri, 13 Jan 2017 18:11:25 GMT  
		Size: 289.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6fbdd973b7f37ae2a28fc6b474025b35c589c8ca310be685e72c384e08824d`  
		Last Modified: Fri, 13 Jan 2017 18:11:25 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.4`

```console
$ docker pull memcached@sha256:7f702ad1a68dc999b8f277150b695dc0e3b70f50a4a383afd3dc4e9538d9bf42
```

-	Platforms:
	-	linux; amd64

### `memcached:1.4` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52239686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a10d7823aad82ace39b6d0eaf8d36bf018198a75bfe35cd716fdcebaafdf34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 01:03:06 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Wed, 14 Dec 2016 01:03:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libevent-2.0-5 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 18:10:29 GMT
ENV MEMCACHED_VERSION=1.4.34
# Fri, 13 Jan 2017 18:10:29 GMT
ENV MEMCACHED_SHA1=7c7214f5183c6e20c22b243e21ed1ffddb91497e
# Fri, 13 Jan 2017 18:10:50 GMT
RUN buildDeps=' 		gcc 		libc6-dev 		libevent-dev 		make 		perl 		wget 	' 	&& set -x 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& wget -O memcached.tar.gz "http://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 	&& cd /usr/src/memcached 	&& ./configure 	&& make -j$(nproc) 	&& make install 	&& cd / && rm -rf /usr/src/memcached 	&& apt-get purge -y --auto-remove $buildDeps
# Fri, 13 Jan 2017 18:10:51 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Fri, 13 Jan 2017 18:10:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 13 Jan 2017 18:10:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 18:10:53 GMT
USER [memcache]
# Fri, 13 Jan 2017 18:10:53 GMT
EXPOSE 11211/tcp
# Fri, 13 Jan 2017 18:10:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b78be39d94d164800f0c9a2e4a617b2281dbbfab6c2a68e9550d1b94d5c314`  
		Last Modified: Mon, 19 Dec 2016 23:56:48 GMT  
		Size: 2.0 KB (2040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a68c6a8c3a07df4f5a8965bdb4c7a1e31e4c37eaa976e8333f9e1c370bfbafe`  
		Last Modified: Mon, 19 Dec 2016 23:56:47 GMT  
		Size: 237.9 KB (237938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e722127a5c096fe498931871e0f69762ba2081106fec8afc60443bb3933ed5b`  
		Last Modified: Fri, 13 Jan 2017 18:11:26 GMT  
		Size: 636.2 KB (636175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d261dd099866d75d9c11e3dcb7042277336c708b8058c03681e623711723ac9d`  
		Last Modified: Fri, 13 Jan 2017 18:11:25 GMT  
		Size: 289.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6fbdd973b7f37ae2a28fc6b474025b35c589c8ca310be685e72c384e08824d`  
		Last Modified: Fri, 13 Jan 2017 18:11:25 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1`

```console
$ docker pull memcached@sha256:7f702ad1a68dc999b8f277150b695dc0e3b70f50a4a383afd3dc4e9538d9bf42
```

-	Platforms:
	-	linux; amd64

### `memcached:1` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52239686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a10d7823aad82ace39b6d0eaf8d36bf018198a75bfe35cd716fdcebaafdf34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 01:03:06 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Wed, 14 Dec 2016 01:03:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libevent-2.0-5 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 18:10:29 GMT
ENV MEMCACHED_VERSION=1.4.34
# Fri, 13 Jan 2017 18:10:29 GMT
ENV MEMCACHED_SHA1=7c7214f5183c6e20c22b243e21ed1ffddb91497e
# Fri, 13 Jan 2017 18:10:50 GMT
RUN buildDeps=' 		gcc 		libc6-dev 		libevent-dev 		make 		perl 		wget 	' 	&& set -x 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& wget -O memcached.tar.gz "http://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 	&& cd /usr/src/memcached 	&& ./configure 	&& make -j$(nproc) 	&& make install 	&& cd / && rm -rf /usr/src/memcached 	&& apt-get purge -y --auto-remove $buildDeps
# Fri, 13 Jan 2017 18:10:51 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Fri, 13 Jan 2017 18:10:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 13 Jan 2017 18:10:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 18:10:53 GMT
USER [memcache]
# Fri, 13 Jan 2017 18:10:53 GMT
EXPOSE 11211/tcp
# Fri, 13 Jan 2017 18:10:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b78be39d94d164800f0c9a2e4a617b2281dbbfab6c2a68e9550d1b94d5c314`  
		Last Modified: Mon, 19 Dec 2016 23:56:48 GMT  
		Size: 2.0 KB (2040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a68c6a8c3a07df4f5a8965bdb4c7a1e31e4c37eaa976e8333f9e1c370bfbafe`  
		Last Modified: Mon, 19 Dec 2016 23:56:47 GMT  
		Size: 237.9 KB (237938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e722127a5c096fe498931871e0f69762ba2081106fec8afc60443bb3933ed5b`  
		Last Modified: Fri, 13 Jan 2017 18:11:26 GMT  
		Size: 636.2 KB (636175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d261dd099866d75d9c11e3dcb7042277336c708b8058c03681e623711723ac9d`  
		Last Modified: Fri, 13 Jan 2017 18:11:25 GMT  
		Size: 289.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6fbdd973b7f37ae2a28fc6b474025b35c589c8ca310be685e72c384e08824d`  
		Last Modified: Fri, 13 Jan 2017 18:11:25 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:latest`

```console
$ docker pull memcached@sha256:7f702ad1a68dc999b8f277150b695dc0e3b70f50a4a383afd3dc4e9538d9bf42
```

-	Platforms:
	-	linux; amd64

### `memcached:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52239686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a10d7823aad82ace39b6d0eaf8d36bf018198a75bfe35cd716fdcebaafdf34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 01:03:06 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Wed, 14 Dec 2016 01:03:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libevent-2.0-5 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 18:10:29 GMT
ENV MEMCACHED_VERSION=1.4.34
# Fri, 13 Jan 2017 18:10:29 GMT
ENV MEMCACHED_SHA1=7c7214f5183c6e20c22b243e21ed1ffddb91497e
# Fri, 13 Jan 2017 18:10:50 GMT
RUN buildDeps=' 		gcc 		libc6-dev 		libevent-dev 		make 		perl 		wget 	' 	&& set -x 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& wget -O memcached.tar.gz "http://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 	&& cd /usr/src/memcached 	&& ./configure 	&& make -j$(nproc) 	&& make install 	&& cd / && rm -rf /usr/src/memcached 	&& apt-get purge -y --auto-remove $buildDeps
# Fri, 13 Jan 2017 18:10:51 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Fri, 13 Jan 2017 18:10:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 13 Jan 2017 18:10:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 18:10:53 GMT
USER [memcache]
# Fri, 13 Jan 2017 18:10:53 GMT
EXPOSE 11211/tcp
# Fri, 13 Jan 2017 18:10:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b78be39d94d164800f0c9a2e4a617b2281dbbfab6c2a68e9550d1b94d5c314`  
		Last Modified: Mon, 19 Dec 2016 23:56:48 GMT  
		Size: 2.0 KB (2040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a68c6a8c3a07df4f5a8965bdb4c7a1e31e4c37eaa976e8333f9e1c370bfbafe`  
		Last Modified: Mon, 19 Dec 2016 23:56:47 GMT  
		Size: 237.9 KB (237938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e722127a5c096fe498931871e0f69762ba2081106fec8afc60443bb3933ed5b`  
		Last Modified: Fri, 13 Jan 2017 18:11:26 GMT  
		Size: 636.2 KB (636175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d261dd099866d75d9c11e3dcb7042277336c708b8058c03681e623711723ac9d`  
		Last Modified: Fri, 13 Jan 2017 18:11:25 GMT  
		Size: 289.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6fbdd973b7f37ae2a28fc6b474025b35c589c8ca310be685e72c384e08824d`  
		Last Modified: Fri, 13 Jan 2017 18:11:25 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.4.34-alpine`

```console
$ docker pull memcached@sha256:97317346fde08f06ca1e6aa8efa7b96fd6349ed18d103eb900f8dac75a577ac8
```

-	Platforms:
	-	linux; amd64

### `memcached:1.4.34-alpine` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2372452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdef622d405cb35c466aa29ea7411fd594e7985127bec4e8080572d7ef45cfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 27 Dec 2016 18:17:25 GMT
ADD file:92ab746eb22dd3ed2b87469c719adf3c1bed7302653bbd76baafd7cfd95e911e in / 
# Wed, 04 Jan 2017 21:11:39 GMT
RUN adduser -D memcache
# Fri, 13 Jan 2017 18:10:54 GMT
ENV MEMCACHED_VERSION=1.4.34
# Fri, 13 Jan 2017 18:10:55 GMT
ENV MEMCACHED_SHA1=7c7214f5183c6e20c22b243e21ed1ffddb91497e
# Fri, 13 Jan 2017 18:11:05 GMT
RUN set -x 	&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		perl 		tar 	&& wget -O memcached.tar.gz "http://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 	&& cd /usr/src/memcached 	&& ./configure 	&& make -j$(getconf _NPROCESSORS_ONLN) 	&& make install 	&& cd / && rm -rf /usr/src/memcached 	&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps
# Fri, 13 Jan 2017 18:11:06 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Fri, 13 Jan 2017 18:11:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 13 Jan 2017 18:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 18:11:08 GMT
USER [memcache]
# Fri, 13 Jan 2017 18:11:08 GMT
EXPOSE 11211/tcp
# Fri, 13 Jan 2017 18:11:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0a8490d0dfd399b3a50e9aaa81dba0d425c3868762d46526b41be00886bcc28b`  
		Last Modified: Tue, 27 Dec 2016 18:19:22 GMT  
		Size: 1.9 MB (1902063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57076bf87737c2f448e75324ceba121b3b90372ab913f604f928a40da4ebddc7`  
		Last Modified: Thu, 05 Jan 2017 00:08:35 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665bd0ffc53b125e42c7ace50d4b788885bdaf57ac1348014e5cc35600a61d0b`  
		Last Modified: Fri, 13 Jan 2017 18:12:27 GMT  
		Size: 468.7 KB (468749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2072bc4567e1f13081af323d046f39453f010471701fa11fc50b786b60512e99`  
		Last Modified: Fri, 13 Jan 2017 18:12:27 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33066afa1dbb37ce114b2ebafe9702cea9a26c8901da38201bfcdcff17d3d190`  
		Last Modified: Fri, 13 Jan 2017 18:12:26 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.4-alpine`

```console
$ docker pull memcached@sha256:97317346fde08f06ca1e6aa8efa7b96fd6349ed18d103eb900f8dac75a577ac8
```

-	Platforms:
	-	linux; amd64

### `memcached:1.4-alpine` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2372452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdef622d405cb35c466aa29ea7411fd594e7985127bec4e8080572d7ef45cfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 27 Dec 2016 18:17:25 GMT
ADD file:92ab746eb22dd3ed2b87469c719adf3c1bed7302653bbd76baafd7cfd95e911e in / 
# Wed, 04 Jan 2017 21:11:39 GMT
RUN adduser -D memcache
# Fri, 13 Jan 2017 18:10:54 GMT
ENV MEMCACHED_VERSION=1.4.34
# Fri, 13 Jan 2017 18:10:55 GMT
ENV MEMCACHED_SHA1=7c7214f5183c6e20c22b243e21ed1ffddb91497e
# Fri, 13 Jan 2017 18:11:05 GMT
RUN set -x 	&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		perl 		tar 	&& wget -O memcached.tar.gz "http://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 	&& cd /usr/src/memcached 	&& ./configure 	&& make -j$(getconf _NPROCESSORS_ONLN) 	&& make install 	&& cd / && rm -rf /usr/src/memcached 	&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps
# Fri, 13 Jan 2017 18:11:06 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Fri, 13 Jan 2017 18:11:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 13 Jan 2017 18:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 18:11:08 GMT
USER [memcache]
# Fri, 13 Jan 2017 18:11:08 GMT
EXPOSE 11211/tcp
# Fri, 13 Jan 2017 18:11:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0a8490d0dfd399b3a50e9aaa81dba0d425c3868762d46526b41be00886bcc28b`  
		Last Modified: Tue, 27 Dec 2016 18:19:22 GMT  
		Size: 1.9 MB (1902063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57076bf87737c2f448e75324ceba121b3b90372ab913f604f928a40da4ebddc7`  
		Last Modified: Thu, 05 Jan 2017 00:08:35 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665bd0ffc53b125e42c7ace50d4b788885bdaf57ac1348014e5cc35600a61d0b`  
		Last Modified: Fri, 13 Jan 2017 18:12:27 GMT  
		Size: 468.7 KB (468749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2072bc4567e1f13081af323d046f39453f010471701fa11fc50b786b60512e99`  
		Last Modified: Fri, 13 Jan 2017 18:12:27 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33066afa1dbb37ce114b2ebafe9702cea9a26c8901da38201bfcdcff17d3d190`  
		Last Modified: Fri, 13 Jan 2017 18:12:26 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:97317346fde08f06ca1e6aa8efa7b96fd6349ed18d103eb900f8dac75a577ac8
```

-	Platforms:
	-	linux; amd64

### `memcached:1-alpine` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2372452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdef622d405cb35c466aa29ea7411fd594e7985127bec4e8080572d7ef45cfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 27 Dec 2016 18:17:25 GMT
ADD file:92ab746eb22dd3ed2b87469c719adf3c1bed7302653bbd76baafd7cfd95e911e in / 
# Wed, 04 Jan 2017 21:11:39 GMT
RUN adduser -D memcache
# Fri, 13 Jan 2017 18:10:54 GMT
ENV MEMCACHED_VERSION=1.4.34
# Fri, 13 Jan 2017 18:10:55 GMT
ENV MEMCACHED_SHA1=7c7214f5183c6e20c22b243e21ed1ffddb91497e
# Fri, 13 Jan 2017 18:11:05 GMT
RUN set -x 	&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		perl 		tar 	&& wget -O memcached.tar.gz "http://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 	&& cd /usr/src/memcached 	&& ./configure 	&& make -j$(getconf _NPROCESSORS_ONLN) 	&& make install 	&& cd / && rm -rf /usr/src/memcached 	&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps
# Fri, 13 Jan 2017 18:11:06 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Fri, 13 Jan 2017 18:11:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 13 Jan 2017 18:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 18:11:08 GMT
USER [memcache]
# Fri, 13 Jan 2017 18:11:08 GMT
EXPOSE 11211/tcp
# Fri, 13 Jan 2017 18:11:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0a8490d0dfd399b3a50e9aaa81dba0d425c3868762d46526b41be00886bcc28b`  
		Last Modified: Tue, 27 Dec 2016 18:19:22 GMT  
		Size: 1.9 MB (1902063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57076bf87737c2f448e75324ceba121b3b90372ab913f604f928a40da4ebddc7`  
		Last Modified: Thu, 05 Jan 2017 00:08:35 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665bd0ffc53b125e42c7ace50d4b788885bdaf57ac1348014e5cc35600a61d0b`  
		Last Modified: Fri, 13 Jan 2017 18:12:27 GMT  
		Size: 468.7 KB (468749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2072bc4567e1f13081af323d046f39453f010471701fa11fc50b786b60512e99`  
		Last Modified: Fri, 13 Jan 2017 18:12:27 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33066afa1dbb37ce114b2ebafe9702cea9a26c8901da38201bfcdcff17d3d190`  
		Last Modified: Fri, 13 Jan 2017 18:12:26 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:alpine`

```console
$ docker pull memcached@sha256:97317346fde08f06ca1e6aa8efa7b96fd6349ed18d103eb900f8dac75a577ac8
```

-	Platforms:
	-	linux; amd64

### `memcached:alpine` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2372452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdef622d405cb35c466aa29ea7411fd594e7985127bec4e8080572d7ef45cfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 27 Dec 2016 18:17:25 GMT
ADD file:92ab746eb22dd3ed2b87469c719adf3c1bed7302653bbd76baafd7cfd95e911e in / 
# Wed, 04 Jan 2017 21:11:39 GMT
RUN adduser -D memcache
# Fri, 13 Jan 2017 18:10:54 GMT
ENV MEMCACHED_VERSION=1.4.34
# Fri, 13 Jan 2017 18:10:55 GMT
ENV MEMCACHED_SHA1=7c7214f5183c6e20c22b243e21ed1ffddb91497e
# Fri, 13 Jan 2017 18:11:05 GMT
RUN set -x 	&& apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		perl 		tar 	&& wget -O memcached.tar.gz "http://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 	&& cd /usr/src/memcached 	&& ./configure 	&& make -j$(getconf _NPROCESSORS_ONLN) 	&& make install 	&& cd / && rm -rf /usr/src/memcached 	&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps
# Fri, 13 Jan 2017 18:11:06 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Fri, 13 Jan 2017 18:11:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 13 Jan 2017 18:11:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 18:11:08 GMT
USER [memcache]
# Fri, 13 Jan 2017 18:11:08 GMT
EXPOSE 11211/tcp
# Fri, 13 Jan 2017 18:11:09 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:0a8490d0dfd399b3a50e9aaa81dba0d425c3868762d46526b41be00886bcc28b`  
		Last Modified: Tue, 27 Dec 2016 18:19:22 GMT  
		Size: 1.9 MB (1902063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57076bf87737c2f448e75324ceba121b3b90372ab913f604f928a40da4ebddc7`  
		Last Modified: Thu, 05 Jan 2017 00:08:35 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665bd0ffc53b125e42c7ace50d4b788885bdaf57ac1348014e5cc35600a61d0b`  
		Last Modified: Fri, 13 Jan 2017 18:12:27 GMT  
		Size: 468.7 KB (468749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2072bc4567e1f13081af323d046f39453f010471701fa11fc50b786b60512e99`  
		Last Modified: Fri, 13 Jan 2017 18:12:27 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33066afa1dbb37ce114b2ebafe9702cea9a26c8901da38201bfcdcff17d3d190`  
		Last Modified: Fri, 13 Jan 2017 18:12:26 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
