## `openjdk:9-jre`

```console
$ docker pull openjdk@sha256:9392c30212c18f37be799c340cbc83ed93f7ec6aa112a6b8f92df4d5c2175148
```

-	Platforms:
	-	linux; amd64

### `openjdk:9-jre` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210913572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42f13c0832a863bc0ceb27bdbbe7d86c9485a003d544cf3904c5598a99adafc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Dec 2016 22:12:19 GMT
ADD file:1ec9813ae98ad32fbb472ab2d0a10bfffc02970b272ce3595007bf94381ea99d in / 
# Tue, 13 Dec 2016 22:12:20 GMT
CMD ["/bin/bash"]
# Tue, 13 Dec 2016 23:00:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 02:59:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 02:59:38 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
# Wed, 14 Dec 2016 02:59:38 GMT
ENV LANG=C.UTF-8
# Wed, 14 Dec 2016 02:59:40 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 14 Dec 2016 02:59:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-9-openjdk-amd64
# Fri, 13 Jan 2017 18:18:46 GMT
ENV JAVA_VERSION=9~b151
# Fri, 13 Jan 2017 18:18:46 GMT
ENV JAVA_DEBIAN_VERSION=9~b151-2
# Fri, 13 Jan 2017 18:19:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		openjdk-9-jre-headless="$JAVA_DEBIAN_VERSION" 	&& rm -rf /var/lib/apt/lists/* 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
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
	-	`sha256:801b9fb4552a9cf708a2ced6096640ea30d0750fb00c703b2054ce608edcd65c`  
		Last Modified: Wed, 14 Dec 2016 03:22:57 GMT  
		Size: 616.8 KB (616780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b17e15d30934d4f6fe4b4fa5ac87544d3992615b38bb1d93608aa7afeaf002`  
		Last Modified: Wed, 14 Dec 2016 03:22:56 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788f5e49c1a09a98ee588cea80cbc04ec77049e417ef71cbb908b922963c9887`  
		Last Modified: Wed, 14 Dec 2016 03:22:55 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe678f1649d004c81203281cacc170cb17824e58633201433e83ce413ad3f1a`  
		Last Modified: Fri, 13 Jan 2017 18:35:51 GMT  
		Size: 145.5 MB (145483977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
