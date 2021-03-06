## `maven:3-jdk-9`

```console
$ docker pull maven@sha256:cc8391b871134e44d27e42393184c6501894c78ee4beffdca5906d6aefc667bb
```

-	Platforms:
	-	linux; amd64

### `maven:3-jdk-9` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270347709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb9417838d77b58a6c4acffb20581d427ad4e2e7f0eee205f67f08e61efe471`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Dec 2016 22:12:19 GMT
ADD file:1ec9813ae98ad32fbb472ab2d0a10bfffc02970b272ce3595007bf94381ea99d in / 
# Tue, 13 Dec 2016 22:12:20 GMT
CMD ["/bin/bash"]
# Tue, 13 Dec 2016 23:00:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:01:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:55:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:55:38 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
# Tue, 13 Dec 2016 23:55:38 GMT
ENV LANG=C.UTF-8
# Tue, 13 Dec 2016 23:55:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 13 Dec 2016 23:55:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-9-openjdk-amd64
# Fri, 13 Jan 2017 18:17:52 GMT
ENV JAVA_VERSION=9~b151
# Fri, 13 Jan 2017 18:17:52 GMT
ENV JAVA_DEBIAN_VERSION=9~b151-2
# Fri, 13 Jan 2017 18:18:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	&& rm -rf /var/lib/apt/lists/* 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 13 Jan 2017 18:42:30 GMT
ARG MAVEN_VERSION=3.3.9
# Fri, 13 Jan 2017 18:42:31 GMT
ARG USER_HOME_DIR=/root
# Fri, 13 Jan 2017 18:42:33 GMT
# ARGS: MAVEN_VERSION=3.3.9 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL http://apache.osuosl.org/maven/maven-3/$MAVEN_VERSION/binaries/apache-maven-$MAVEN_VERSION-bin.tar.gz     | tar -xzC /usr/share/maven --strip-components=1   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 13 Jan 2017 18:42:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 13 Jan 2017 18:42:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 13 Jan 2017 18:42:46 GMT
COPY file:e3aa30a24fcf60a59710465ac66fc1d53c35590a74fcdd51e12a5cbce393904b in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 13 Jan 2017 18:42:46 GMT
COPY file:b3fc14e8337e0079a4e97eace880b4b7cddc0dc0ea733de80749f78fe1eb089a in /usr/share/maven/ref/ 
# Fri, 13 Jan 2017 18:42:47 GMT
VOLUME [/root/.m2]
# Fri, 13 Jan 2017 18:42:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 13 Jan 2017 18:42:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:96adffeba9716172608de9e458530715467b8d8a3d22b249de6f7d2f0c6e9f55`  
		Last Modified: Tue, 13 Dec 2016 22:20:27 GMT  
		Size: 43.9 MB (43866938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72591232915f25a33b2dcf0ed9fea09256ec5c0988bce2e515b6e9911274adc`  
		Last Modified: Wed, 14 Dec 2016 03:20:29 GMT  
		Size: 20.9 MB (20945421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e5ec7de751dd011b9b64ec0ee93775040bb91451b2b1dc95ec4a175de462c3`  
		Last Modified: Wed, 14 Dec 2016 03:20:43 GMT  
		Size: 51.2 MB (51219215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121993890cd4b642ee91546b2c0b7c655abd4287f759bed0220f854f61d6608f`  
		Last Modified: Wed, 14 Dec 2016 03:20:20 GMT  
		Size: 648.4 KB (648436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c137dfeb464dfb54e087d20ccb9a6525a515aab6121f1184499fa1b539667d7`  
		Last Modified: Wed, 14 Dec 2016 03:20:23 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6d48ce44eb06a1b268d4330e98380ab8ff70b3b5f746a1db08d33da596f50e`  
		Last Modified: Wed, 14 Dec 2016 03:20:19 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13b3017ba3a43b7a6d846a5eb3de5e996696f86fd3be442adea1bccbc92e282`  
		Last Modified: Fri, 13 Jan 2017 18:33:48 GMT  
		Size: 145.1 MB (145067350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b072cd6994b9eacf7e3e7b5334df09ae81035a61d556f9b0eb3be384611f730`  
		Last Modified: Fri, 13 Jan 2017 18:54:25 GMT  
		Size: 8.6 MB (8598851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a11fefb360de3b6909c814c1cb6558f3bd43222c3b38db15adbf9ba0aedb2b`  
		Last Modified: Fri, 13 Jan 2017 18:54:24 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac66798e3be26736fdbd2b3119c6df0a98de349f835d650a7adea65beb83bd7`  
		Last Modified: Fri, 13 Jan 2017 18:54:27 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
