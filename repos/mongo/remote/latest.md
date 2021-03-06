## `mongo:latest`

```console
$ docker pull mongo@sha256:fa7a1184384abc0f76adec9cfba3535a0fecc4762e04c172ff2445106bcc7c0f
```

-	Platforms:
	-	linux; amd64

### `mongo:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150408822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b8f19244cd8a7f81147d29612c006aad0e4ea3a72b51b014e3badef3bb47f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 01:03:39 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 14 Dec 2016 01:03:46 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 01:03:46 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 01:04:04 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Fri, 13 Jan 2017 18:13:59 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Fri, 13 Jan 2017 18:14:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 13 Jan 2017 18:14:01 GMT
ENV MONGO_MAJOR=3.4
# Fri, 13 Jan 2017 18:14:01 GMT
ENV MONGO_VERSION=3.4.1
# Fri, 13 Jan 2017 18:14:02 GMT
ENV MONGO_PACKAGE=mongodb-org
# Fri, 13 Jan 2017 18:14:03 GMT
RUN echo "deb http://repo.mongodb.org/apt/debian jessie/mongodb-org/$MONGO_MAJOR main" > /etc/apt/sources.list.d/mongodb-org.list
# Fri, 13 Jan 2017 18:14:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 13 Jan 2017 18:14:18 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 13 Jan 2017 18:14:18 GMT
VOLUME [/data/db /data/configdb]
# Fri, 13 Jan 2017 18:14:19 GMT
COPY file:7f1f8bb27f73563768bb938208148a281b70ba028a8d544671abcb276c8f741c in /entrypoint.sh 
# Fri, 13 Jan 2017 18:14:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Jan 2017 18:14:20 GMT
EXPOSE 27017/tcp
# Fri, 13 Jan 2017 18:14:21 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf369f658b6e4148ed366e1b3433ffd3d2187c54398a73773fca1063d126ebc`  
		Last Modified: Mon, 19 Dec 2016 23:59:15 GMT  
		Size: 2.0 KB (2041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7cb343d20eb7857450e9941bfe56fa088af8ee5d72e7749c1d0e786d45887e`  
		Last Modified: Mon, 19 Dec 2016 23:59:15 GMT  
		Size: 134.6 KB (134593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a933a908f75926d8bfb0dc65d604d53d2b4b128ecacb9bed02f5c155ddffbd`  
		Last Modified: Mon, 19 Dec 2016 23:59:15 GMT  
		Size: 1.2 MB (1217869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e3f377cb7c91a6c1cce2dfb1297dd971afc9fa5dae0c41df5990cbd5c28b79`  
		Last Modified: Fri, 13 Jan 2017 18:16:33 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c966a5ad0306b35bfbe16612d7f8b91b3d909cc667ec5f2a9dc910e74bcb47b`  
		Last Modified: Fri, 13 Jan 2017 18:16:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187315b08446792ecf97684f61bdbc4413b0e584f4b3007430ba85a5476ccf20`  
		Last Modified: Fri, 13 Jan 2017 18:17:03 GMT  
		Size: 97.7 MB (97689056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d669318a89abf3b5adc83a81aab9fbf7846e7cc2795ca3f06ce5128f29fead7c`  
		Last Modified: Fri, 13 Jan 2017 18:16:33 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5d7f61f934002d0fd8017d9223ed485fe079f9d618fa7e6b92bd3de088676b`  
		Last Modified: Fri, 13 Jan 2017 18:16:33 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
