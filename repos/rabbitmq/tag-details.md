<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rabbitmq`

-	[`rabbitmq:3.6.6`](#rabbitmq366)
-	[`rabbitmq:3.6`](#rabbitmq36)
-	[`rabbitmq:3`](#rabbitmq3)
-	[`rabbitmq:latest`](#rabbitmqlatest)
-	[`rabbitmq:3.6.6-management`](#rabbitmq366-management)
-	[`rabbitmq:3.6-management`](#rabbitmq36-management)
-	[`rabbitmq:3-management`](#rabbitmq3-management)
-	[`rabbitmq:management`](#rabbitmqmanagement)

## `rabbitmq:3.6.6`

```console
$ docker pull rabbitmq@sha256:621c02ae1b8b960bbb8fc0209f706fc8e836a08ef134c4bc6b67a0ec90961e8e
```

-	Platforms:
	-	linux; amd64

### `rabbitmq:3.6.6` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86652500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f51ee498225bdbb3c766c911cb00cc3436163f0dca62e7a337a8fda5fbd672c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 19:02:57 GMT
RUN groupadd -r rabbitmq && useradd -r -d /var/lib/rabbitmq -m -g rabbitmq rabbitmq
# Wed, 14 Dec 2016 19:02:58 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 19:14:25 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Fri, 13 Jan 2017 19:03:13 GMT
RUN set -ex; 	key='434975BD900CCBE4F7EE1B1ED208507CA14F4FCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/erlang-solutions.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 13 Jan 2017 19:03:14 GMT
RUN echo 'deb http://packages.erlang-solutions.com/debian jessie contrib' > /etc/apt/sources.list.d/erlang.list
# Fri, 13 Jan 2017 19:03:53 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		erlang-asn1 		erlang-base-hipe 		erlang-crypto 		erlang-eldap 		erlang-inets 		erlang-mnesia 		erlang-nox 		erlang-os-mon 		erlang-public-key 		erlang-ssl 		erlang-xmerl 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 19:03:56 GMT
ENV RABBITMQ_LOGS=- RABBITMQ_SASL_LOGS=-
# Fri, 13 Jan 2017 19:03:58 GMT
RUN set -ex; 	key='0A9AF2115F4687BD29803A206B73A36E6026DFCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/rabbitmq.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 13 Jan 2017 19:03:59 GMT
RUN echo 'deb http://www.rabbitmq.com/debian testing main' > /etc/apt/sources.list.d/rabbitmq.list
# Fri, 13 Jan 2017 19:03:59 GMT
ENV RABBITMQ_VERSION=3.6.6
# Fri, 13 Jan 2017 19:04:11 GMT
ENV RABBITMQ_DEBIAN_VERSION=3.6.6-1
# Fri, 13 Jan 2017 19:04:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		rabbitmq-server=$RABBITMQ_DEBIAN_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 19:04:26 GMT
ENV PATH=/usr/lib/rabbitmq/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Jan 2017 19:04:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Jan 2017 19:04:27 GMT
RUN mkdir -p /var/lib/rabbitmq /etc/rabbitmq 	&& echo '[ { rabbit, [ { loopback_users, [ ] } ] } ].' > /etc/rabbitmq/rabbitmq.config 	&& chown -R rabbitmq:rabbitmq /var/lib/rabbitmq /etc/rabbitmq 	&& chmod -R 777 /var/lib/rabbitmq /etc/rabbitmq
# Fri, 13 Jan 2017 19:04:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Jan 2017 19:04:29 GMT
RUN ln -sf /var/lib/rabbitmq/.erlang.cookie /root/
# Fri, 13 Jan 2017 19:04:42 GMT
RUN ln -sf /usr/lib/rabbitmq/lib/rabbitmq_server-$RABBITMQ_VERSION/plugins /plugins
# Fri, 13 Jan 2017 19:04:43 GMT
COPY file:aea0de868079820b38523daba3301f9d1b03f85139fbcab491d2bc10c2540046 in /usr/local/bin/ 
# Fri, 13 Jan 2017 19:04:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 13 Jan 2017 19:04:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 19:04:57 GMT
EXPOSE 25672/tcp 4369/tcp 5671/tcp 5672/tcp
# Fri, 13 Jan 2017 19:04:57 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7d779bbd840f454e19f8fd4c399ad45640a295a371b4916da1499cbe4e5963`  
		Last Modified: Wed, 21 Dec 2016 19:27:46 GMT  
		Size: 4.3 KB (4336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea153d7516c01f37d84c6b9706985891b84ecb66bcb1a79f13ade006e2fade5`  
		Last Modified: Wed, 21 Dec 2016 19:27:45 GMT  
		Size: 1.2 MB (1216943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f656f03472716f35b8a9e86dc397ebf536b120d15b77c61aba499a91af25863a`  
		Last Modified: Fri, 13 Jan 2017 19:05:32 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b04450726118e71bde558f6045279ec6e581bbb232c17462db6724d13c0099`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b81b42ca9c4bfe6f140817eaef1a691a884a8a601ce01a0602442601494477`  
		Last Modified: Fri, 13 Jan 2017 19:05:34 GMT  
		Size: 27.8 MB (27823218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9960250b1c9b6a60f5cb8fac856748adf11a5d1d3efb22009b6c903eb1948a`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 3.1 KB (3095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab86b57d0f4ee8fa66f872799eee50a11baa6e7d06e654ee9d29a774ff5d807`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80502d0123d52c73f18dad597a0419fe016a0eaea4a7a6348242daa9910846`  
		Last Modified: Fri, 13 Jan 2017 19:05:31 GMT  
		Size: 6.2 MB (6233458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ceba8724f40895e8f79dfc5617e9fe2039adb50018d399aad83624d97181260`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3471c2646f876e043a1f494f35200d08a39712aa54b27b3f72c5ea99915d3d1a`  
		Last Modified: Fri, 13 Jan 2017 19:05:26 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ce5aa873f05eaea88cc90a553ac8e4f2199c5059c7187d9487c8ac0851602a`  
		Last Modified: Fri, 13 Jan 2017 19:05:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef5c79c044dafdb7711182f7d446ed83da7386a1c0a9d6f8e19e7c0a2cc968`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38d928a3c66bad638c9d01859ea18459fe39887665e3e561c34679c85f21073`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rabbitmq:3.6`

```console
$ docker pull rabbitmq@sha256:621c02ae1b8b960bbb8fc0209f706fc8e836a08ef134c4bc6b67a0ec90961e8e
```

-	Platforms:
	-	linux; amd64

### `rabbitmq:3.6` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86652500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f51ee498225bdbb3c766c911cb00cc3436163f0dca62e7a337a8fda5fbd672c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 19:02:57 GMT
RUN groupadd -r rabbitmq && useradd -r -d /var/lib/rabbitmq -m -g rabbitmq rabbitmq
# Wed, 14 Dec 2016 19:02:58 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 19:14:25 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Fri, 13 Jan 2017 19:03:13 GMT
RUN set -ex; 	key='434975BD900CCBE4F7EE1B1ED208507CA14F4FCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/erlang-solutions.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 13 Jan 2017 19:03:14 GMT
RUN echo 'deb http://packages.erlang-solutions.com/debian jessie contrib' > /etc/apt/sources.list.d/erlang.list
# Fri, 13 Jan 2017 19:03:53 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		erlang-asn1 		erlang-base-hipe 		erlang-crypto 		erlang-eldap 		erlang-inets 		erlang-mnesia 		erlang-nox 		erlang-os-mon 		erlang-public-key 		erlang-ssl 		erlang-xmerl 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 19:03:56 GMT
ENV RABBITMQ_LOGS=- RABBITMQ_SASL_LOGS=-
# Fri, 13 Jan 2017 19:03:58 GMT
RUN set -ex; 	key='0A9AF2115F4687BD29803A206B73A36E6026DFCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/rabbitmq.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 13 Jan 2017 19:03:59 GMT
RUN echo 'deb http://www.rabbitmq.com/debian testing main' > /etc/apt/sources.list.d/rabbitmq.list
# Fri, 13 Jan 2017 19:03:59 GMT
ENV RABBITMQ_VERSION=3.6.6
# Fri, 13 Jan 2017 19:04:11 GMT
ENV RABBITMQ_DEBIAN_VERSION=3.6.6-1
# Fri, 13 Jan 2017 19:04:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		rabbitmq-server=$RABBITMQ_DEBIAN_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 19:04:26 GMT
ENV PATH=/usr/lib/rabbitmq/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Jan 2017 19:04:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Jan 2017 19:04:27 GMT
RUN mkdir -p /var/lib/rabbitmq /etc/rabbitmq 	&& echo '[ { rabbit, [ { loopback_users, [ ] } ] } ].' > /etc/rabbitmq/rabbitmq.config 	&& chown -R rabbitmq:rabbitmq /var/lib/rabbitmq /etc/rabbitmq 	&& chmod -R 777 /var/lib/rabbitmq /etc/rabbitmq
# Fri, 13 Jan 2017 19:04:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Jan 2017 19:04:29 GMT
RUN ln -sf /var/lib/rabbitmq/.erlang.cookie /root/
# Fri, 13 Jan 2017 19:04:42 GMT
RUN ln -sf /usr/lib/rabbitmq/lib/rabbitmq_server-$RABBITMQ_VERSION/plugins /plugins
# Fri, 13 Jan 2017 19:04:43 GMT
COPY file:aea0de868079820b38523daba3301f9d1b03f85139fbcab491d2bc10c2540046 in /usr/local/bin/ 
# Fri, 13 Jan 2017 19:04:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 13 Jan 2017 19:04:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 19:04:57 GMT
EXPOSE 25672/tcp 4369/tcp 5671/tcp 5672/tcp
# Fri, 13 Jan 2017 19:04:57 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7d779bbd840f454e19f8fd4c399ad45640a295a371b4916da1499cbe4e5963`  
		Last Modified: Wed, 21 Dec 2016 19:27:46 GMT  
		Size: 4.3 KB (4336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea153d7516c01f37d84c6b9706985891b84ecb66bcb1a79f13ade006e2fade5`  
		Last Modified: Wed, 21 Dec 2016 19:27:45 GMT  
		Size: 1.2 MB (1216943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f656f03472716f35b8a9e86dc397ebf536b120d15b77c61aba499a91af25863a`  
		Last Modified: Fri, 13 Jan 2017 19:05:32 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b04450726118e71bde558f6045279ec6e581bbb232c17462db6724d13c0099`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b81b42ca9c4bfe6f140817eaef1a691a884a8a601ce01a0602442601494477`  
		Last Modified: Fri, 13 Jan 2017 19:05:34 GMT  
		Size: 27.8 MB (27823218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9960250b1c9b6a60f5cb8fac856748adf11a5d1d3efb22009b6c903eb1948a`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 3.1 KB (3095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab86b57d0f4ee8fa66f872799eee50a11baa6e7d06e654ee9d29a774ff5d807`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80502d0123d52c73f18dad597a0419fe016a0eaea4a7a6348242daa9910846`  
		Last Modified: Fri, 13 Jan 2017 19:05:31 GMT  
		Size: 6.2 MB (6233458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ceba8724f40895e8f79dfc5617e9fe2039adb50018d399aad83624d97181260`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3471c2646f876e043a1f494f35200d08a39712aa54b27b3f72c5ea99915d3d1a`  
		Last Modified: Fri, 13 Jan 2017 19:05:26 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ce5aa873f05eaea88cc90a553ac8e4f2199c5059c7187d9487c8ac0851602a`  
		Last Modified: Fri, 13 Jan 2017 19:05:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef5c79c044dafdb7711182f7d446ed83da7386a1c0a9d6f8e19e7c0a2cc968`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38d928a3c66bad638c9d01859ea18459fe39887665e3e561c34679c85f21073`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rabbitmq:3`

```console
$ docker pull rabbitmq@sha256:621c02ae1b8b960bbb8fc0209f706fc8e836a08ef134c4bc6b67a0ec90961e8e
```

-	Platforms:
	-	linux; amd64

### `rabbitmq:3` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86652500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f51ee498225bdbb3c766c911cb00cc3436163f0dca62e7a337a8fda5fbd672c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 19:02:57 GMT
RUN groupadd -r rabbitmq && useradd -r -d /var/lib/rabbitmq -m -g rabbitmq rabbitmq
# Wed, 14 Dec 2016 19:02:58 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 19:14:25 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Fri, 13 Jan 2017 19:03:13 GMT
RUN set -ex; 	key='434975BD900CCBE4F7EE1B1ED208507CA14F4FCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/erlang-solutions.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 13 Jan 2017 19:03:14 GMT
RUN echo 'deb http://packages.erlang-solutions.com/debian jessie contrib' > /etc/apt/sources.list.d/erlang.list
# Fri, 13 Jan 2017 19:03:53 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		erlang-asn1 		erlang-base-hipe 		erlang-crypto 		erlang-eldap 		erlang-inets 		erlang-mnesia 		erlang-nox 		erlang-os-mon 		erlang-public-key 		erlang-ssl 		erlang-xmerl 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 19:03:56 GMT
ENV RABBITMQ_LOGS=- RABBITMQ_SASL_LOGS=-
# Fri, 13 Jan 2017 19:03:58 GMT
RUN set -ex; 	key='0A9AF2115F4687BD29803A206B73A36E6026DFCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/rabbitmq.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 13 Jan 2017 19:03:59 GMT
RUN echo 'deb http://www.rabbitmq.com/debian testing main' > /etc/apt/sources.list.d/rabbitmq.list
# Fri, 13 Jan 2017 19:03:59 GMT
ENV RABBITMQ_VERSION=3.6.6
# Fri, 13 Jan 2017 19:04:11 GMT
ENV RABBITMQ_DEBIAN_VERSION=3.6.6-1
# Fri, 13 Jan 2017 19:04:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		rabbitmq-server=$RABBITMQ_DEBIAN_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 19:04:26 GMT
ENV PATH=/usr/lib/rabbitmq/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Jan 2017 19:04:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Jan 2017 19:04:27 GMT
RUN mkdir -p /var/lib/rabbitmq /etc/rabbitmq 	&& echo '[ { rabbit, [ { loopback_users, [ ] } ] } ].' > /etc/rabbitmq/rabbitmq.config 	&& chown -R rabbitmq:rabbitmq /var/lib/rabbitmq /etc/rabbitmq 	&& chmod -R 777 /var/lib/rabbitmq /etc/rabbitmq
# Fri, 13 Jan 2017 19:04:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Jan 2017 19:04:29 GMT
RUN ln -sf /var/lib/rabbitmq/.erlang.cookie /root/
# Fri, 13 Jan 2017 19:04:42 GMT
RUN ln -sf /usr/lib/rabbitmq/lib/rabbitmq_server-$RABBITMQ_VERSION/plugins /plugins
# Fri, 13 Jan 2017 19:04:43 GMT
COPY file:aea0de868079820b38523daba3301f9d1b03f85139fbcab491d2bc10c2540046 in /usr/local/bin/ 
# Fri, 13 Jan 2017 19:04:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 13 Jan 2017 19:04:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 19:04:57 GMT
EXPOSE 25672/tcp 4369/tcp 5671/tcp 5672/tcp
# Fri, 13 Jan 2017 19:04:57 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7d779bbd840f454e19f8fd4c399ad45640a295a371b4916da1499cbe4e5963`  
		Last Modified: Wed, 21 Dec 2016 19:27:46 GMT  
		Size: 4.3 KB (4336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea153d7516c01f37d84c6b9706985891b84ecb66bcb1a79f13ade006e2fade5`  
		Last Modified: Wed, 21 Dec 2016 19:27:45 GMT  
		Size: 1.2 MB (1216943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f656f03472716f35b8a9e86dc397ebf536b120d15b77c61aba499a91af25863a`  
		Last Modified: Fri, 13 Jan 2017 19:05:32 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b04450726118e71bde558f6045279ec6e581bbb232c17462db6724d13c0099`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b81b42ca9c4bfe6f140817eaef1a691a884a8a601ce01a0602442601494477`  
		Last Modified: Fri, 13 Jan 2017 19:05:34 GMT  
		Size: 27.8 MB (27823218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9960250b1c9b6a60f5cb8fac856748adf11a5d1d3efb22009b6c903eb1948a`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 3.1 KB (3095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab86b57d0f4ee8fa66f872799eee50a11baa6e7d06e654ee9d29a774ff5d807`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80502d0123d52c73f18dad597a0419fe016a0eaea4a7a6348242daa9910846`  
		Last Modified: Fri, 13 Jan 2017 19:05:31 GMT  
		Size: 6.2 MB (6233458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ceba8724f40895e8f79dfc5617e9fe2039adb50018d399aad83624d97181260`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3471c2646f876e043a1f494f35200d08a39712aa54b27b3f72c5ea99915d3d1a`  
		Last Modified: Fri, 13 Jan 2017 19:05:26 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ce5aa873f05eaea88cc90a553ac8e4f2199c5059c7187d9487c8ac0851602a`  
		Last Modified: Fri, 13 Jan 2017 19:05:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef5c79c044dafdb7711182f7d446ed83da7386a1c0a9d6f8e19e7c0a2cc968`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38d928a3c66bad638c9d01859ea18459fe39887665e3e561c34679c85f21073`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rabbitmq:latest`

```console
$ docker pull rabbitmq@sha256:621c02ae1b8b960bbb8fc0209f706fc8e836a08ef134c4bc6b67a0ec90961e8e
```

-	Platforms:
	-	linux; amd64

### `rabbitmq:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86652500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f51ee498225bdbb3c766c911cb00cc3436163f0dca62e7a337a8fda5fbd672c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 19:02:57 GMT
RUN groupadd -r rabbitmq && useradd -r -d /var/lib/rabbitmq -m -g rabbitmq rabbitmq
# Wed, 14 Dec 2016 19:02:58 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 19:14:25 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Fri, 13 Jan 2017 19:03:13 GMT
RUN set -ex; 	key='434975BD900CCBE4F7EE1B1ED208507CA14F4FCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/erlang-solutions.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 13 Jan 2017 19:03:14 GMT
RUN echo 'deb http://packages.erlang-solutions.com/debian jessie contrib' > /etc/apt/sources.list.d/erlang.list
# Fri, 13 Jan 2017 19:03:53 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		erlang-asn1 		erlang-base-hipe 		erlang-crypto 		erlang-eldap 		erlang-inets 		erlang-mnesia 		erlang-nox 		erlang-os-mon 		erlang-public-key 		erlang-ssl 		erlang-xmerl 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 19:03:56 GMT
ENV RABBITMQ_LOGS=- RABBITMQ_SASL_LOGS=-
# Fri, 13 Jan 2017 19:03:58 GMT
RUN set -ex; 	key='0A9AF2115F4687BD29803A206B73A36E6026DFCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/rabbitmq.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 13 Jan 2017 19:03:59 GMT
RUN echo 'deb http://www.rabbitmq.com/debian testing main' > /etc/apt/sources.list.d/rabbitmq.list
# Fri, 13 Jan 2017 19:03:59 GMT
ENV RABBITMQ_VERSION=3.6.6
# Fri, 13 Jan 2017 19:04:11 GMT
ENV RABBITMQ_DEBIAN_VERSION=3.6.6-1
# Fri, 13 Jan 2017 19:04:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		rabbitmq-server=$RABBITMQ_DEBIAN_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 19:04:26 GMT
ENV PATH=/usr/lib/rabbitmq/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Jan 2017 19:04:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Jan 2017 19:04:27 GMT
RUN mkdir -p /var/lib/rabbitmq /etc/rabbitmq 	&& echo '[ { rabbit, [ { loopback_users, [ ] } ] } ].' > /etc/rabbitmq/rabbitmq.config 	&& chown -R rabbitmq:rabbitmq /var/lib/rabbitmq /etc/rabbitmq 	&& chmod -R 777 /var/lib/rabbitmq /etc/rabbitmq
# Fri, 13 Jan 2017 19:04:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Jan 2017 19:04:29 GMT
RUN ln -sf /var/lib/rabbitmq/.erlang.cookie /root/
# Fri, 13 Jan 2017 19:04:42 GMT
RUN ln -sf /usr/lib/rabbitmq/lib/rabbitmq_server-$RABBITMQ_VERSION/plugins /plugins
# Fri, 13 Jan 2017 19:04:43 GMT
COPY file:aea0de868079820b38523daba3301f9d1b03f85139fbcab491d2bc10c2540046 in /usr/local/bin/ 
# Fri, 13 Jan 2017 19:04:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 13 Jan 2017 19:04:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 19:04:57 GMT
EXPOSE 25672/tcp 4369/tcp 5671/tcp 5672/tcp
# Fri, 13 Jan 2017 19:04:57 GMT
CMD ["rabbitmq-server"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7d779bbd840f454e19f8fd4c399ad45640a295a371b4916da1499cbe4e5963`  
		Last Modified: Wed, 21 Dec 2016 19:27:46 GMT  
		Size: 4.3 KB (4336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea153d7516c01f37d84c6b9706985891b84ecb66bcb1a79f13ade006e2fade5`  
		Last Modified: Wed, 21 Dec 2016 19:27:45 GMT  
		Size: 1.2 MB (1216943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f656f03472716f35b8a9e86dc397ebf536b120d15b77c61aba499a91af25863a`  
		Last Modified: Fri, 13 Jan 2017 19:05:32 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b04450726118e71bde558f6045279ec6e581bbb232c17462db6724d13c0099`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b81b42ca9c4bfe6f140817eaef1a691a884a8a601ce01a0602442601494477`  
		Last Modified: Fri, 13 Jan 2017 19:05:34 GMT  
		Size: 27.8 MB (27823218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9960250b1c9b6a60f5cb8fac856748adf11a5d1d3efb22009b6c903eb1948a`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 3.1 KB (3095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab86b57d0f4ee8fa66f872799eee50a11baa6e7d06e654ee9d29a774ff5d807`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80502d0123d52c73f18dad597a0419fe016a0eaea4a7a6348242daa9910846`  
		Last Modified: Fri, 13 Jan 2017 19:05:31 GMT  
		Size: 6.2 MB (6233458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ceba8724f40895e8f79dfc5617e9fe2039adb50018d399aad83624d97181260`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3471c2646f876e043a1f494f35200d08a39712aa54b27b3f72c5ea99915d3d1a`  
		Last Modified: Fri, 13 Jan 2017 19:05:26 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ce5aa873f05eaea88cc90a553ac8e4f2199c5059c7187d9487c8ac0851602a`  
		Last Modified: Fri, 13 Jan 2017 19:05:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef5c79c044dafdb7711182f7d446ed83da7386a1c0a9d6f8e19e7c0a2cc968`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38d928a3c66bad638c9d01859ea18459fe39887665e3e561c34679c85f21073`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rabbitmq:3.6.6-management`

```console
$ docker pull rabbitmq@sha256:096063a702099032ae9b7c4ed067e98ec95da0395a0369d6fad52979bfee4246
```

-	Platforms:
	-	linux; amd64

### `rabbitmq:3.6.6-management` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86652688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca30fd9beed79b64f9b1404425712afef04b3ae9d9cc3e7453dfcf89bb0b5705`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 19:02:57 GMT
RUN groupadd -r rabbitmq && useradd -r -d /var/lib/rabbitmq -m -g rabbitmq rabbitmq
# Wed, 14 Dec 2016 19:02:58 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 19:14:25 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Fri, 13 Jan 2017 19:03:13 GMT
RUN set -ex; 	key='434975BD900CCBE4F7EE1B1ED208507CA14F4FCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/erlang-solutions.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 13 Jan 2017 19:03:14 GMT
RUN echo 'deb http://packages.erlang-solutions.com/debian jessie contrib' > /etc/apt/sources.list.d/erlang.list
# Fri, 13 Jan 2017 19:03:53 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		erlang-asn1 		erlang-base-hipe 		erlang-crypto 		erlang-eldap 		erlang-inets 		erlang-mnesia 		erlang-nox 		erlang-os-mon 		erlang-public-key 		erlang-ssl 		erlang-xmerl 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 19:03:56 GMT
ENV RABBITMQ_LOGS=- RABBITMQ_SASL_LOGS=-
# Fri, 13 Jan 2017 19:03:58 GMT
RUN set -ex; 	key='0A9AF2115F4687BD29803A206B73A36E6026DFCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/rabbitmq.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 13 Jan 2017 19:03:59 GMT
RUN echo 'deb http://www.rabbitmq.com/debian testing main' > /etc/apt/sources.list.d/rabbitmq.list
# Fri, 13 Jan 2017 19:03:59 GMT
ENV RABBITMQ_VERSION=3.6.6
# Fri, 13 Jan 2017 19:04:11 GMT
ENV RABBITMQ_DEBIAN_VERSION=3.6.6-1
# Fri, 13 Jan 2017 19:04:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		rabbitmq-server=$RABBITMQ_DEBIAN_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 19:04:26 GMT
ENV PATH=/usr/lib/rabbitmq/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Jan 2017 19:04:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Jan 2017 19:04:27 GMT
RUN mkdir -p /var/lib/rabbitmq /etc/rabbitmq 	&& echo '[ { rabbit, [ { loopback_users, [ ] } ] } ].' > /etc/rabbitmq/rabbitmq.config 	&& chown -R rabbitmq:rabbitmq /var/lib/rabbitmq /etc/rabbitmq 	&& chmod -R 777 /var/lib/rabbitmq /etc/rabbitmq
# Fri, 13 Jan 2017 19:04:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Jan 2017 19:04:29 GMT
RUN ln -sf /var/lib/rabbitmq/.erlang.cookie /root/
# Fri, 13 Jan 2017 19:04:42 GMT
RUN ln -sf /usr/lib/rabbitmq/lib/rabbitmq_server-$RABBITMQ_VERSION/plugins /plugins
# Fri, 13 Jan 2017 19:04:43 GMT
COPY file:aea0de868079820b38523daba3301f9d1b03f85139fbcab491d2bc10c2540046 in /usr/local/bin/ 
# Fri, 13 Jan 2017 19:04:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 13 Jan 2017 19:04:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 19:04:57 GMT
EXPOSE 25672/tcp 4369/tcp 5671/tcp 5672/tcp
# Fri, 13 Jan 2017 19:04:57 GMT
CMD ["rabbitmq-server"]
# Fri, 13 Jan 2017 19:04:59 GMT
RUN rabbitmq-plugins enable --offline rabbitmq_management
# Fri, 13 Jan 2017 19:05:11 GMT
EXPOSE 15671/tcp 15672/tcp
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7d779bbd840f454e19f8fd4c399ad45640a295a371b4916da1499cbe4e5963`  
		Last Modified: Wed, 21 Dec 2016 19:27:46 GMT  
		Size: 4.3 KB (4336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea153d7516c01f37d84c6b9706985891b84ecb66bcb1a79f13ade006e2fade5`  
		Last Modified: Wed, 21 Dec 2016 19:27:45 GMT  
		Size: 1.2 MB (1216943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f656f03472716f35b8a9e86dc397ebf536b120d15b77c61aba499a91af25863a`  
		Last Modified: Fri, 13 Jan 2017 19:05:32 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b04450726118e71bde558f6045279ec6e581bbb232c17462db6724d13c0099`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b81b42ca9c4bfe6f140817eaef1a691a884a8a601ce01a0602442601494477`  
		Last Modified: Fri, 13 Jan 2017 19:05:34 GMT  
		Size: 27.8 MB (27823218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9960250b1c9b6a60f5cb8fac856748adf11a5d1d3efb22009b6c903eb1948a`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 3.1 KB (3095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab86b57d0f4ee8fa66f872799eee50a11baa6e7d06e654ee9d29a774ff5d807`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80502d0123d52c73f18dad597a0419fe016a0eaea4a7a6348242daa9910846`  
		Last Modified: Fri, 13 Jan 2017 19:05:31 GMT  
		Size: 6.2 MB (6233458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ceba8724f40895e8f79dfc5617e9fe2039adb50018d399aad83624d97181260`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3471c2646f876e043a1f494f35200d08a39712aa54b27b3f72c5ea99915d3d1a`  
		Last Modified: Fri, 13 Jan 2017 19:05:26 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ce5aa873f05eaea88cc90a553ac8e4f2199c5059c7187d9487c8ac0851602a`  
		Last Modified: Fri, 13 Jan 2017 19:05:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef5c79c044dafdb7711182f7d446ed83da7386a1c0a9d6f8e19e7c0a2cc968`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38d928a3c66bad638c9d01859ea18459fe39887665e3e561c34679c85f21073`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e57da21b8b8202d80289109f529e2eec33709aced330128e17877cc67be8f4`  
		Last Modified: Fri, 13 Jan 2017 19:07:14 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rabbitmq:3.6-management`

```console
$ docker pull rabbitmq@sha256:096063a702099032ae9b7c4ed067e98ec95da0395a0369d6fad52979bfee4246
```

-	Platforms:
	-	linux; amd64

### `rabbitmq:3.6-management` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86652688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca30fd9beed79b64f9b1404425712afef04b3ae9d9cc3e7453dfcf89bb0b5705`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 19:02:57 GMT
RUN groupadd -r rabbitmq && useradd -r -d /var/lib/rabbitmq -m -g rabbitmq rabbitmq
# Wed, 14 Dec 2016 19:02:58 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 19:14:25 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Fri, 13 Jan 2017 19:03:13 GMT
RUN set -ex; 	key='434975BD900CCBE4F7EE1B1ED208507CA14F4FCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/erlang-solutions.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 13 Jan 2017 19:03:14 GMT
RUN echo 'deb http://packages.erlang-solutions.com/debian jessie contrib' > /etc/apt/sources.list.d/erlang.list
# Fri, 13 Jan 2017 19:03:53 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		erlang-asn1 		erlang-base-hipe 		erlang-crypto 		erlang-eldap 		erlang-inets 		erlang-mnesia 		erlang-nox 		erlang-os-mon 		erlang-public-key 		erlang-ssl 		erlang-xmerl 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 19:03:56 GMT
ENV RABBITMQ_LOGS=- RABBITMQ_SASL_LOGS=-
# Fri, 13 Jan 2017 19:03:58 GMT
RUN set -ex; 	key='0A9AF2115F4687BD29803A206B73A36E6026DFCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/rabbitmq.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 13 Jan 2017 19:03:59 GMT
RUN echo 'deb http://www.rabbitmq.com/debian testing main' > /etc/apt/sources.list.d/rabbitmq.list
# Fri, 13 Jan 2017 19:03:59 GMT
ENV RABBITMQ_VERSION=3.6.6
# Fri, 13 Jan 2017 19:04:11 GMT
ENV RABBITMQ_DEBIAN_VERSION=3.6.6-1
# Fri, 13 Jan 2017 19:04:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		rabbitmq-server=$RABBITMQ_DEBIAN_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 19:04:26 GMT
ENV PATH=/usr/lib/rabbitmq/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Jan 2017 19:04:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Jan 2017 19:04:27 GMT
RUN mkdir -p /var/lib/rabbitmq /etc/rabbitmq 	&& echo '[ { rabbit, [ { loopback_users, [ ] } ] } ].' > /etc/rabbitmq/rabbitmq.config 	&& chown -R rabbitmq:rabbitmq /var/lib/rabbitmq /etc/rabbitmq 	&& chmod -R 777 /var/lib/rabbitmq /etc/rabbitmq
# Fri, 13 Jan 2017 19:04:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Jan 2017 19:04:29 GMT
RUN ln -sf /var/lib/rabbitmq/.erlang.cookie /root/
# Fri, 13 Jan 2017 19:04:42 GMT
RUN ln -sf /usr/lib/rabbitmq/lib/rabbitmq_server-$RABBITMQ_VERSION/plugins /plugins
# Fri, 13 Jan 2017 19:04:43 GMT
COPY file:aea0de868079820b38523daba3301f9d1b03f85139fbcab491d2bc10c2540046 in /usr/local/bin/ 
# Fri, 13 Jan 2017 19:04:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 13 Jan 2017 19:04:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 19:04:57 GMT
EXPOSE 25672/tcp 4369/tcp 5671/tcp 5672/tcp
# Fri, 13 Jan 2017 19:04:57 GMT
CMD ["rabbitmq-server"]
# Fri, 13 Jan 2017 19:04:59 GMT
RUN rabbitmq-plugins enable --offline rabbitmq_management
# Fri, 13 Jan 2017 19:05:11 GMT
EXPOSE 15671/tcp 15672/tcp
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7d779bbd840f454e19f8fd4c399ad45640a295a371b4916da1499cbe4e5963`  
		Last Modified: Wed, 21 Dec 2016 19:27:46 GMT  
		Size: 4.3 KB (4336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea153d7516c01f37d84c6b9706985891b84ecb66bcb1a79f13ade006e2fade5`  
		Last Modified: Wed, 21 Dec 2016 19:27:45 GMT  
		Size: 1.2 MB (1216943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f656f03472716f35b8a9e86dc397ebf536b120d15b77c61aba499a91af25863a`  
		Last Modified: Fri, 13 Jan 2017 19:05:32 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b04450726118e71bde558f6045279ec6e581bbb232c17462db6724d13c0099`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b81b42ca9c4bfe6f140817eaef1a691a884a8a601ce01a0602442601494477`  
		Last Modified: Fri, 13 Jan 2017 19:05:34 GMT  
		Size: 27.8 MB (27823218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9960250b1c9b6a60f5cb8fac856748adf11a5d1d3efb22009b6c903eb1948a`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 3.1 KB (3095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab86b57d0f4ee8fa66f872799eee50a11baa6e7d06e654ee9d29a774ff5d807`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80502d0123d52c73f18dad597a0419fe016a0eaea4a7a6348242daa9910846`  
		Last Modified: Fri, 13 Jan 2017 19:05:31 GMT  
		Size: 6.2 MB (6233458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ceba8724f40895e8f79dfc5617e9fe2039adb50018d399aad83624d97181260`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3471c2646f876e043a1f494f35200d08a39712aa54b27b3f72c5ea99915d3d1a`  
		Last Modified: Fri, 13 Jan 2017 19:05:26 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ce5aa873f05eaea88cc90a553ac8e4f2199c5059c7187d9487c8ac0851602a`  
		Last Modified: Fri, 13 Jan 2017 19:05:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef5c79c044dafdb7711182f7d446ed83da7386a1c0a9d6f8e19e7c0a2cc968`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38d928a3c66bad638c9d01859ea18459fe39887665e3e561c34679c85f21073`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e57da21b8b8202d80289109f529e2eec33709aced330128e17877cc67be8f4`  
		Last Modified: Fri, 13 Jan 2017 19:07:14 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rabbitmq:3-management`

```console
$ docker pull rabbitmq@sha256:096063a702099032ae9b7c4ed067e98ec95da0395a0369d6fad52979bfee4246
```

-	Platforms:
	-	linux; amd64

### `rabbitmq:3-management` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86652688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca30fd9beed79b64f9b1404425712afef04b3ae9d9cc3e7453dfcf89bb0b5705`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 19:02:57 GMT
RUN groupadd -r rabbitmq && useradd -r -d /var/lib/rabbitmq -m -g rabbitmq rabbitmq
# Wed, 14 Dec 2016 19:02:58 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 19:14:25 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Fri, 13 Jan 2017 19:03:13 GMT
RUN set -ex; 	key='434975BD900CCBE4F7EE1B1ED208507CA14F4FCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/erlang-solutions.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 13 Jan 2017 19:03:14 GMT
RUN echo 'deb http://packages.erlang-solutions.com/debian jessie contrib' > /etc/apt/sources.list.d/erlang.list
# Fri, 13 Jan 2017 19:03:53 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		erlang-asn1 		erlang-base-hipe 		erlang-crypto 		erlang-eldap 		erlang-inets 		erlang-mnesia 		erlang-nox 		erlang-os-mon 		erlang-public-key 		erlang-ssl 		erlang-xmerl 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 19:03:56 GMT
ENV RABBITMQ_LOGS=- RABBITMQ_SASL_LOGS=-
# Fri, 13 Jan 2017 19:03:58 GMT
RUN set -ex; 	key='0A9AF2115F4687BD29803A206B73A36E6026DFCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/rabbitmq.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 13 Jan 2017 19:03:59 GMT
RUN echo 'deb http://www.rabbitmq.com/debian testing main' > /etc/apt/sources.list.d/rabbitmq.list
# Fri, 13 Jan 2017 19:03:59 GMT
ENV RABBITMQ_VERSION=3.6.6
# Fri, 13 Jan 2017 19:04:11 GMT
ENV RABBITMQ_DEBIAN_VERSION=3.6.6-1
# Fri, 13 Jan 2017 19:04:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		rabbitmq-server=$RABBITMQ_DEBIAN_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 19:04:26 GMT
ENV PATH=/usr/lib/rabbitmq/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Jan 2017 19:04:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Jan 2017 19:04:27 GMT
RUN mkdir -p /var/lib/rabbitmq /etc/rabbitmq 	&& echo '[ { rabbit, [ { loopback_users, [ ] } ] } ].' > /etc/rabbitmq/rabbitmq.config 	&& chown -R rabbitmq:rabbitmq /var/lib/rabbitmq /etc/rabbitmq 	&& chmod -R 777 /var/lib/rabbitmq /etc/rabbitmq
# Fri, 13 Jan 2017 19:04:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Jan 2017 19:04:29 GMT
RUN ln -sf /var/lib/rabbitmq/.erlang.cookie /root/
# Fri, 13 Jan 2017 19:04:42 GMT
RUN ln -sf /usr/lib/rabbitmq/lib/rabbitmq_server-$RABBITMQ_VERSION/plugins /plugins
# Fri, 13 Jan 2017 19:04:43 GMT
COPY file:aea0de868079820b38523daba3301f9d1b03f85139fbcab491d2bc10c2540046 in /usr/local/bin/ 
# Fri, 13 Jan 2017 19:04:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 13 Jan 2017 19:04:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 19:04:57 GMT
EXPOSE 25672/tcp 4369/tcp 5671/tcp 5672/tcp
# Fri, 13 Jan 2017 19:04:57 GMT
CMD ["rabbitmq-server"]
# Fri, 13 Jan 2017 19:04:59 GMT
RUN rabbitmq-plugins enable --offline rabbitmq_management
# Fri, 13 Jan 2017 19:05:11 GMT
EXPOSE 15671/tcp 15672/tcp
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7d779bbd840f454e19f8fd4c399ad45640a295a371b4916da1499cbe4e5963`  
		Last Modified: Wed, 21 Dec 2016 19:27:46 GMT  
		Size: 4.3 KB (4336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea153d7516c01f37d84c6b9706985891b84ecb66bcb1a79f13ade006e2fade5`  
		Last Modified: Wed, 21 Dec 2016 19:27:45 GMT  
		Size: 1.2 MB (1216943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f656f03472716f35b8a9e86dc397ebf536b120d15b77c61aba499a91af25863a`  
		Last Modified: Fri, 13 Jan 2017 19:05:32 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b04450726118e71bde558f6045279ec6e581bbb232c17462db6724d13c0099`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b81b42ca9c4bfe6f140817eaef1a691a884a8a601ce01a0602442601494477`  
		Last Modified: Fri, 13 Jan 2017 19:05:34 GMT  
		Size: 27.8 MB (27823218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9960250b1c9b6a60f5cb8fac856748adf11a5d1d3efb22009b6c903eb1948a`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 3.1 KB (3095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab86b57d0f4ee8fa66f872799eee50a11baa6e7d06e654ee9d29a774ff5d807`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80502d0123d52c73f18dad597a0419fe016a0eaea4a7a6348242daa9910846`  
		Last Modified: Fri, 13 Jan 2017 19:05:31 GMT  
		Size: 6.2 MB (6233458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ceba8724f40895e8f79dfc5617e9fe2039adb50018d399aad83624d97181260`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3471c2646f876e043a1f494f35200d08a39712aa54b27b3f72c5ea99915d3d1a`  
		Last Modified: Fri, 13 Jan 2017 19:05:26 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ce5aa873f05eaea88cc90a553ac8e4f2199c5059c7187d9487c8ac0851602a`  
		Last Modified: Fri, 13 Jan 2017 19:05:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef5c79c044dafdb7711182f7d446ed83da7386a1c0a9d6f8e19e7c0a2cc968`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38d928a3c66bad638c9d01859ea18459fe39887665e3e561c34679c85f21073`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e57da21b8b8202d80289109f529e2eec33709aced330128e17877cc67be8f4`  
		Last Modified: Fri, 13 Jan 2017 19:07:14 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rabbitmq:management`

```console
$ docker pull rabbitmq@sha256:096063a702099032ae9b7c4ed067e98ec95da0395a0369d6fad52979bfee4246
```

-	Platforms:
	-	linux; amd64

### `rabbitmq:management` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86652688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca30fd9beed79b64f9b1404425712afef04b3ae9d9cc3e7453dfcf89bb0b5705`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["rabbitmq-server"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 19:02:57 GMT
RUN groupadd -r rabbitmq && useradd -r -d /var/lib/rabbitmq -m -g rabbitmq rabbitmq
# Wed, 14 Dec 2016 19:02:58 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 19:14:25 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Fri, 13 Jan 2017 19:03:13 GMT
RUN set -ex; 	key='434975BD900CCBE4F7EE1B1ED208507CA14F4FCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/erlang-solutions.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 13 Jan 2017 19:03:14 GMT
RUN echo 'deb http://packages.erlang-solutions.com/debian jessie contrib' > /etc/apt/sources.list.d/erlang.list
# Fri, 13 Jan 2017 19:03:53 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		erlang-asn1 		erlang-base-hipe 		erlang-crypto 		erlang-eldap 		erlang-inets 		erlang-mnesia 		erlang-nox 		erlang-os-mon 		erlang-public-key 		erlang-ssl 		erlang-xmerl 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 19:03:56 GMT
ENV RABBITMQ_LOGS=- RABBITMQ_SASL_LOGS=-
# Fri, 13 Jan 2017 19:03:58 GMT
RUN set -ex; 	key='0A9AF2115F4687BD29803A206B73A36E6026DFCA'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/rabbitmq.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 13 Jan 2017 19:03:59 GMT
RUN echo 'deb http://www.rabbitmq.com/debian testing main' > /etc/apt/sources.list.d/rabbitmq.list
# Fri, 13 Jan 2017 19:03:59 GMT
ENV RABBITMQ_VERSION=3.6.6
# Fri, 13 Jan 2017 19:04:11 GMT
ENV RABBITMQ_DEBIAN_VERSION=3.6.6-1
# Fri, 13 Jan 2017 19:04:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		rabbitmq-server=$RABBITMQ_DEBIAN_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 19:04:26 GMT
ENV PATH=/usr/lib/rabbitmq/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Jan 2017 19:04:26 GMT
ENV HOME=/var/lib/rabbitmq
# Fri, 13 Jan 2017 19:04:27 GMT
RUN mkdir -p /var/lib/rabbitmq /etc/rabbitmq 	&& echo '[ { rabbit, [ { loopback_users, [ ] } ] } ].' > /etc/rabbitmq/rabbitmq.config 	&& chown -R rabbitmq:rabbitmq /var/lib/rabbitmq /etc/rabbitmq 	&& chmod -R 777 /var/lib/rabbitmq /etc/rabbitmq
# Fri, 13 Jan 2017 19:04:28 GMT
VOLUME [/var/lib/rabbitmq]
# Fri, 13 Jan 2017 19:04:29 GMT
RUN ln -sf /var/lib/rabbitmq/.erlang.cookie /root/
# Fri, 13 Jan 2017 19:04:42 GMT
RUN ln -sf /usr/lib/rabbitmq/lib/rabbitmq_server-$RABBITMQ_VERSION/plugins /plugins
# Fri, 13 Jan 2017 19:04:43 GMT
COPY file:aea0de868079820b38523daba3301f9d1b03f85139fbcab491d2bc10c2540046 in /usr/local/bin/ 
# Fri, 13 Jan 2017 19:04:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 13 Jan 2017 19:04:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 19:04:57 GMT
EXPOSE 25672/tcp 4369/tcp 5671/tcp 5672/tcp
# Fri, 13 Jan 2017 19:04:57 GMT
CMD ["rabbitmq-server"]
# Fri, 13 Jan 2017 19:04:59 GMT
RUN rabbitmq-plugins enable --offline rabbitmq_management
# Fri, 13 Jan 2017 19:05:11 GMT
EXPOSE 15671/tcp 15672/tcp
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7d779bbd840f454e19f8fd4c399ad45640a295a371b4916da1499cbe4e5963`  
		Last Modified: Wed, 21 Dec 2016 19:27:46 GMT  
		Size: 4.3 KB (4336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea153d7516c01f37d84c6b9706985891b84ecb66bcb1a79f13ade006e2fade5`  
		Last Modified: Wed, 21 Dec 2016 19:27:45 GMT  
		Size: 1.2 MB (1216943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f656f03472716f35b8a9e86dc397ebf536b120d15b77c61aba499a91af25863a`  
		Last Modified: Fri, 13 Jan 2017 19:05:32 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b04450726118e71bde558f6045279ec6e581bbb232c17462db6724d13c0099`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b81b42ca9c4bfe6f140817eaef1a691a884a8a601ce01a0602442601494477`  
		Last Modified: Fri, 13 Jan 2017 19:05:34 GMT  
		Size: 27.8 MB (27823218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9960250b1c9b6a60f5cb8fac856748adf11a5d1d3efb22009b6c903eb1948a`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 3.1 KB (3095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab86b57d0f4ee8fa66f872799eee50a11baa6e7d06e654ee9d29a774ff5d807`  
		Last Modified: Fri, 13 Jan 2017 19:05:29 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80502d0123d52c73f18dad597a0419fe016a0eaea4a7a6348242daa9910846`  
		Last Modified: Fri, 13 Jan 2017 19:05:31 GMT  
		Size: 6.2 MB (6233458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ceba8724f40895e8f79dfc5617e9fe2039adb50018d399aad83624d97181260`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3471c2646f876e043a1f494f35200d08a39712aa54b27b3f72c5ea99915d3d1a`  
		Last Modified: Fri, 13 Jan 2017 19:05:26 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ce5aa873f05eaea88cc90a553ac8e4f2199c5059c7187d9487c8ac0851602a`  
		Last Modified: Fri, 13 Jan 2017 19:05:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faef5c79c044dafdb7711182f7d446ed83da7386a1c0a9d6f8e19e7c0a2cc968`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38d928a3c66bad638c9d01859ea18459fe39887665e3e561c34679c85f21073`  
		Last Modified: Fri, 13 Jan 2017 19:05:27 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e57da21b8b8202d80289109f529e2eec33709aced330128e17877cc67be8f4`  
		Last Modified: Fri, 13 Jan 2017 19:07:14 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
