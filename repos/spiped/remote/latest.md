## `spiped:latest`

```console
$ docker pull spiped@sha256:06202383bf616a4572534bcd6c6d471d9a9c5a44bbbe3d7678d8dcacfa7de0c6
```

-	Platforms:
	-	linux; amd64

### `spiped:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55615489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fcd24ec354082c91dc47ed6bedf226fee3f5744a209659530dbe21b11907ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Tue, 10 Jan 2017 18:37:57 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 10 Jan 2017 18:38:05 GMT
RUN apt-get update &&	apt-get install -y libssl1.0.0 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 10 Jan 2017 18:38:12 GMT
ENV SPIPED_VERSION=1.5.0
# Tue, 10 Jan 2017 18:38:12 GMT
ENV SPIPED_DOWNLOAD_URL=https://www.tarsnap.com/spiped/spiped-1.5.0.tgz
# Tue, 10 Jan 2017 18:38:13 GMT
ENV SPIPED_DOWNLOAD_SHA256=b2f74b34fb62fd37d6e2bfc969a209c039b88847e853a49e91768dec625facd7
# Tue, 10 Jan 2017 18:38:14 GMT
COPY file:0f26a499fef90f06070551ff66a17abfb7e814a4f023905e52236c31b216a7bb in /0001-Fix-docker-stop-issue.patch 
# Tue, 10 Jan 2017 18:38:40 GMT
RUN buildDeps='libssl-dev gcc make curl ca-certificates patch' &&	apt-get update && apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "$SPIPED_DOWNLOAD_URL" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	patch -p1 -d /usr/local/src/spiped/ < /0001-Fix-docker-stop-issue.patch &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 10 Jan 2017 18:38:40 GMT
VOLUME [/spiped]
# Tue, 10 Jan 2017 18:38:40 GMT
WORKDIR /spiped
# Tue, 10 Jan 2017 18:38:41 GMT
COPY multi:cece67136bcb3e9eb15d965c7f2f0aa1577fa83acbd640e2016eb71cc01e0cfa in /usr/local/bin/ 
# Tue, 10 Jan 2017 18:38:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Jan 2017 18:38:42 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b27f0eea48c8fc00bf3d00646fe5afcd6c0f7133ad64d202c73b2280a8b24d`  
		Last Modified: Tue, 10 Jan 2017 18:39:27 GMT  
		Size: 2.0 KB (2045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f421dd0d74903f0849abb4107816ceaaf163eb13be759e0f2c96d2dca513ef3`  
		Last Modified: Tue, 10 Jan 2017 18:39:24 GMT  
		Size: 1.7 MB (1690923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7f94e7ddbaafc974d296a2429fe6eb74acdf2b76d80fe3c6c8c89fcf1fc614`  
		Last Modified: Tue, 10 Jan 2017 18:39:23 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfe1a39f8c4960fb4619ea3de351c09e77809fd23bba6a983cc35851977a067`  
		Last Modified: Tue, 10 Jan 2017 18:39:24 GMT  
		Size: 2.6 MB (2557730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3076220fe6ff0cec9b203727a539903546261b4268500b0b51fab2b9f910242e`  
		Last Modified: Tue, 10 Jan 2017 18:39:24 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e377143f2decca018afcc15061768bf80d039be01fe9eb01007d02e24471c09c`  
		Last Modified: Tue, 10 Jan 2017 18:39:23 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
