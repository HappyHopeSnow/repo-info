## `maven:3-jdk-8-onbuild`

```console
$ docker pull maven@sha256:5870457433d424668f1b72e122c259f238379e5668b972b3e4840815c34fdd2a
```

-	Platforms:
	-	linux; amd64

### `maven:3-jdk-8-onbuild` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251981889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed6262bbbc7e1f748f1ace31841aab8c835b14c2374a1e2cc2d3ba079f000fc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Tue, 13 Dec 2016 23:00:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:00:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:52:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:54:12 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 13 Dec 2016 23:54:12 GMT
ENV LANG=C.UTF-8
# Tue, 13 Dec 2016 23:54:13 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 13 Dec 2016 23:54:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
# Tue, 13 Dec 2016 23:54:14 GMT
ENV JAVA_VERSION=8u111
# Tue, 13 Dec 2016 23:54:14 GMT
ENV JAVA_DEBIAN_VERSION=8u111-b14-2~bpo8+1
# Tue, 13 Dec 2016 23:54:15 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20140324
# Tue, 13 Dec 2016 23:54:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		openjdk-8-jdk="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	&& rm -rf /var/lib/apt/lists/* 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 13 Dec 2016 23:55:00 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Mon, 19 Dec 2016 16:49:42 GMT
ARG MAVEN_VERSION=3.3.9
# Mon, 19 Dec 2016 16:49:42 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Dec 2016 16:49:44 GMT
# ARGS: MAVEN_VERSION=3.3.9 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL http://apache.osuosl.org/maven/maven-3/$MAVEN_VERSION/binaries/apache-maven-$MAVEN_VERSION-bin.tar.gz     | tar -xzC /usr/share/maven --strip-components=1   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 19 Dec 2016 16:49:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Dec 2016 16:49:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Dec 2016 16:49:45 GMT
COPY file:e3aa30a24fcf60a59710465ac66fc1d53c35590a74fcdd51e12a5cbce393904b in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 19 Dec 2016 16:49:45 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Mon, 19 Dec 2016 16:49:45 GMT
VOLUME [/root/.m2]
# Mon, 19 Dec 2016 16:49:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Dec 2016 16:49:46 GMT
CMD ["mvn"]
# Mon, 19 Dec 2016 16:49:54 GMT
RUN mkdir -p /usr/src/app
# Mon, 19 Dec 2016 16:49:54 GMT
WORKDIR /usr/src/app
# Mon, 19 Dec 2016 16:49:54 GMT
ONBUILD ADD . /usr/src/app
# Mon, 19 Dec 2016 16:49:55 GMT
ONBUILD RUN mvn install
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57de64c72267e88e952b064236cb906c7626f7c07a1a2d5900cf6953e72632b3`  
		Last Modified: Wed, 14 Dec 2016 03:04:38 GMT  
		Size: 18.5 MB (18529983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4306be1e8943b446026b96c2ef7b3ab8471c760774fd1cd11334df7084fed57b`  
		Last Modified: Wed, 14 Dec 2016 03:04:50 GMT  
		Size: 42.5 MB (42502002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6944bfb7182c4b1f546a4bcd888d00bdb92bb016bde7d243af3712549534d9`  
		Last Modified: Wed, 14 Dec 2016 03:04:28 GMT  
		Size: 593.4 KB (593384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3521f2f45ed2f586ef5e6423f3dc3f4e36f7460007c2827b827131d2254ecc44`  
		Last Modified: Wed, 14 Dec 2016 03:11:34 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2f0d9b5f90c348276759c85fae2d52adae563fad53786e8e99862eb3aeab90`  
		Last Modified: Wed, 14 Dec 2016 03:11:34 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cedcf6d25273f360503909554028b54a92d914805ed9d834cbe31e8ebfeb923`  
		Last Modified: Wed, 14 Dec 2016 03:12:30 GMT  
		Size: 130.1 MB (130108711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f99da7583d58b782d9a4c14ef448bf6f6771e15a7975a2450111ed0a34b381`  
		Last Modified: Wed, 14 Dec 2016 03:11:34 GMT  
		Size: 284.2 KB (284180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc801fb53e35d73fd267c66eaf162f3a8fe990a50fc99e6ec30dbbe25639baa6`  
		Last Modified: Mon, 19 Dec 2016 23:51:04 GMT  
		Size: 8.6 MB (8598846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f150b71e3b185ebab57f9e8d158d37edbb3aa02a1ceff1ef4bb412a47bb5937`  
		Last Modified: Mon, 19 Dec 2016 23:51:02 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4d6fcdf7068f2c39687bde036e4d4be4849aca3c77a8cc1d1c679c38ff02a3`  
		Last Modified: Mon, 19 Dec 2016 23:51:02 GMT  
		Size: 347.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fb3f29eecf727d925a844828032c527ba6b3c6ea09cdd9aee2520a8a029cbf`  
		Last Modified: Mon, 19 Dec 2016 23:53:00 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
