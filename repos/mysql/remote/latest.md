## `mysql:latest`

```console
$ docker pull mysql@sha256:5cc898cf7da96e544ce209953f3a17a9965e7c310a51b21a45da7b766e49c568
```

-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137832248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7ce207390ede31adb6abd73e9e2f68f7258a555c6efabb47558191c5b80be0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 01:00:10 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Dec 2016 01:00:11 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 01:00:29 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 14 Dec 2016 01:00:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Dec 2016 02:47:50 GMT
RUN apt-get update && apt-get install -y perl pwgen --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Fri, 13 Jan 2017 23:12:35 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 13 Jan 2017 23:13:09 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 13 Jan 2017 23:13:09 GMT
ENV MYSQL_VERSION=5.7.17-1debian8
# Fri, 13 Jan 2017 23:13:10 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 13 Jan 2017 23:13:28 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Fri, 13 Jan 2017 23:13:29 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/mysql.conf.d/mysqld.cnf 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 13 Jan 2017 23:13:30 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Jan 2017 23:13:31 GMT
COPY file:915aa28b0ee915243ed916898ba2c6103acca9fe847f9365ced97a8b7ee5e4c9 in /usr/local/bin/ 
# Fri, 13 Jan 2017 23:13:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 13 Jan 2017 23:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 23:13:33 GMT
EXPOSE 3306/tcp
# Fri, 13 Jan 2017 23:13:34 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d5846e536af54d4f4773fb5173c759fb8b3673a34710a7e1fe15b4120dc8d2`  
		Last Modified: Wed, 14 Dec 2016 03:24:37 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e9152a1702d9b527b4e753786743d20ceea693424429f5da60410d7b02ddf`  
		Last Modified: Wed, 14 Dec 2016 03:24:36 GMT  
		Size: 1.2 MB (1216944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832e6b0304969b9baa6a38a8e32da0aaf7d7cbf9476c31d006f335264edc6147`  
		Last Modified: Wed, 14 Dec 2016 01:03:50 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4a6c835905c74aa7540cb63201fb2b87287ea2e7fdba0513db04dddfed1e95`  
		Last Modified: Wed, 14 Dec 2016 03:28:16 GMT  
		Size: 8.2 MB (8248277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c2c732c77ff239f41984b98a307c6d127f460bc129948fbe90ea8205b42d9c`  
		Last Modified: Fri, 13 Jan 2017 23:14:18 GMT  
		Size: 19.0 KB (18968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a1e36fd27528a657d2ac4d507eda4e24e9817a978735eafb9147c5b75a42a2`  
		Last Modified: Fri, 13 Jan 2017 23:15:22 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b8bacae77a39764b551dac0e666e574465f6d78ec90962178b310a42a752e2`  
		Last Modified: Fri, 13 Jan 2017 23:15:43 GMT  
		Size: 77.0 MB (76979086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52c7c073f423d56e2a642e21d1be7ab6e35c6c2bfc391cc68bcc15636e3e460`  
		Last Modified: Fri, 13 Jan 2017 23:15:22 GMT  
		Size: 936.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbcda15a0579a7fbbeea22fcff1230bbd190cc8efd0c2877b1920e27734065f`  
		Last Modified: Fri, 13 Jan 2017 23:15:22 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a3ee1c693e3d69754c4b1fae317d1f98cb05e852a9c49b829900b654af7e63`  
		Last Modified: Fri, 13 Jan 2017 23:15:22 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
