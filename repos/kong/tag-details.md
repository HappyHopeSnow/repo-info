<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:0.9`](#kong09)
-	[`kong:0.9.7`](#kong097)
-	[`kong:latest`](#konglatest)

## `kong:0.9`

```console
$ docker pull kong@sha256:f93ded780e26d605ae24f5d600289216dc42fb61be47f721a8cb9f035fc3ff70
```

-	Platforms:
	-	linux; amd64

### `kong:0.9` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122812642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f395e86a6518439b9695aaca0fbf8ea3f36d570d46fc8052571095c2059bf1e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","start"]`

```dockerfile
# Tue, 30 Aug 2016 18:18:45 GMT
MAINTAINER https://github.com/CentOS/sig-cloud-instance-images
# Thu, 15 Dec 2016 18:21:21 GMT
ADD file:940c77b6724c00d4208cc72169a63951eaa605672bcc5902ab2013cbae107434 in / 
# Thu, 15 Dec 2016 18:21:23 GMT
LABEL name=CentOS Base Image vendor=CentOS license=GPLv2 build-date=20161214
# Thu, 15 Dec 2016 18:21:23 GMT
CMD ["/bin/bash"]
# Thu, 15 Dec 2016 18:24:28 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Wed, 28 Dec 2016 21:46:42 GMT
ENV KONG_VERSION=0.9.7
# Wed, 28 Dec 2016 21:47:09 GMT
RUN yum install -y wget https://github.com/Mashape/kong/releases/download/$KONG_VERSION/kong-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Wed, 28 Dec 2016 21:47:12 GMT
RUN wget -O /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.1.3/dumb-init_1.1.3_amd64 &&     chmod +x /usr/local/bin/dumb-init
# Wed, 28 Dec 2016 21:47:13 GMT
COPY file:324f2e5f56829733b3c3c8b6971998202fa01bf7368caac6c1971fcec0464e8c in /docker-entrypoint.sh 
# Wed, 28 Dec 2016 21:47:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Dec 2016 21:47:15 GMT
EXPOSE 7946/tcp 8000/tcp 8001/tcp 8443/tcp
# Wed, 28 Dec 2016 21:47:16 GMT
CMD ["kong" "start"]
```

-	Layers:
	-	`sha256:45a2e645736c4c66ef34acce2407ded21f7a9b231199d3b92d6c9776df264729`  
		Last Modified: Thu, 15 Dec 2016 18:22:30 GMT  
		Size: 70.4 MB (70389679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d1898a6ca19f8ce40931aa1bd7c30090e69790197e1630dca9014d21cbee69`  
		Last Modified: Wed, 28 Dec 2016 21:47:34 GMT  
		Size: 52.4 MB (52398078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58cbaa3d15a5d561bfea2c6635fd5ca45c82a814e718dc6143e133561ca13f9`  
		Last Modified: Wed, 28 Dec 2016 21:47:21 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa205a53e0c13268ce3076962609f7c08451f3ab6324ddcd1145d632b69e4dda`  
		Last Modified: Wed, 28 Dec 2016 21:47:20 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.9.7`

```console
$ docker pull kong@sha256:f93ded780e26d605ae24f5d600289216dc42fb61be47f721a8cb9f035fc3ff70
```

-	Platforms:
	-	linux; amd64

### `kong:0.9.7` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122812642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f395e86a6518439b9695aaca0fbf8ea3f36d570d46fc8052571095c2059bf1e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","start"]`

```dockerfile
# Tue, 30 Aug 2016 18:18:45 GMT
MAINTAINER https://github.com/CentOS/sig-cloud-instance-images
# Thu, 15 Dec 2016 18:21:21 GMT
ADD file:940c77b6724c00d4208cc72169a63951eaa605672bcc5902ab2013cbae107434 in / 
# Thu, 15 Dec 2016 18:21:23 GMT
LABEL name=CentOS Base Image vendor=CentOS license=GPLv2 build-date=20161214
# Thu, 15 Dec 2016 18:21:23 GMT
CMD ["/bin/bash"]
# Thu, 15 Dec 2016 18:24:28 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Wed, 28 Dec 2016 21:46:42 GMT
ENV KONG_VERSION=0.9.7
# Wed, 28 Dec 2016 21:47:09 GMT
RUN yum install -y wget https://github.com/Mashape/kong/releases/download/$KONG_VERSION/kong-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Wed, 28 Dec 2016 21:47:12 GMT
RUN wget -O /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.1.3/dumb-init_1.1.3_amd64 &&     chmod +x /usr/local/bin/dumb-init
# Wed, 28 Dec 2016 21:47:13 GMT
COPY file:324f2e5f56829733b3c3c8b6971998202fa01bf7368caac6c1971fcec0464e8c in /docker-entrypoint.sh 
# Wed, 28 Dec 2016 21:47:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Dec 2016 21:47:15 GMT
EXPOSE 7946/tcp 8000/tcp 8001/tcp 8443/tcp
# Wed, 28 Dec 2016 21:47:16 GMT
CMD ["kong" "start"]
```

-	Layers:
	-	`sha256:45a2e645736c4c66ef34acce2407ded21f7a9b231199d3b92d6c9776df264729`  
		Last Modified: Thu, 15 Dec 2016 18:22:30 GMT  
		Size: 70.4 MB (70389679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d1898a6ca19f8ce40931aa1bd7c30090e69790197e1630dca9014d21cbee69`  
		Last Modified: Wed, 28 Dec 2016 21:47:34 GMT  
		Size: 52.4 MB (52398078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58cbaa3d15a5d561bfea2c6635fd5ca45c82a814e718dc6143e133561ca13f9`  
		Last Modified: Wed, 28 Dec 2016 21:47:21 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa205a53e0c13268ce3076962609f7c08451f3ab6324ddcd1145d632b69e4dda`  
		Last Modified: Wed, 28 Dec 2016 21:47:20 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:f93ded780e26d605ae24f5d600289216dc42fb61be47f721a8cb9f035fc3ff70
```

-	Platforms:
	-	linux; amd64

### `kong:latest` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122812642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f395e86a6518439b9695aaca0fbf8ea3f36d570d46fc8052571095c2059bf1e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","start"]`

```dockerfile
# Tue, 30 Aug 2016 18:18:45 GMT
MAINTAINER https://github.com/CentOS/sig-cloud-instance-images
# Thu, 15 Dec 2016 18:21:21 GMT
ADD file:940c77b6724c00d4208cc72169a63951eaa605672bcc5902ab2013cbae107434 in / 
# Thu, 15 Dec 2016 18:21:23 GMT
LABEL name=CentOS Base Image vendor=CentOS license=GPLv2 build-date=20161214
# Thu, 15 Dec 2016 18:21:23 GMT
CMD ["/bin/bash"]
# Thu, 15 Dec 2016 18:24:28 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Wed, 28 Dec 2016 21:46:42 GMT
ENV KONG_VERSION=0.9.7
# Wed, 28 Dec 2016 21:47:09 GMT
RUN yum install -y wget https://github.com/Mashape/kong/releases/download/$KONG_VERSION/kong-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Wed, 28 Dec 2016 21:47:12 GMT
RUN wget -O /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.1.3/dumb-init_1.1.3_amd64 &&     chmod +x /usr/local/bin/dumb-init
# Wed, 28 Dec 2016 21:47:13 GMT
COPY file:324f2e5f56829733b3c3c8b6971998202fa01bf7368caac6c1971fcec0464e8c in /docker-entrypoint.sh 
# Wed, 28 Dec 2016 21:47:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 28 Dec 2016 21:47:15 GMT
EXPOSE 7946/tcp 8000/tcp 8001/tcp 8443/tcp
# Wed, 28 Dec 2016 21:47:16 GMT
CMD ["kong" "start"]
```

-	Layers:
	-	`sha256:45a2e645736c4c66ef34acce2407ded21f7a9b231199d3b92d6c9776df264729`  
		Last Modified: Thu, 15 Dec 2016 18:22:30 GMT  
		Size: 70.4 MB (70389679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d1898a6ca19f8ce40931aa1bd7c30090e69790197e1630dca9014d21cbee69`  
		Last Modified: Wed, 28 Dec 2016 21:47:34 GMT  
		Size: 52.4 MB (52398078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58cbaa3d15a5d561bfea2c6635fd5ca45c82a814e718dc6143e133561ca13f9`  
		Last Modified: Wed, 28 Dec 2016 21:47:21 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa205a53e0c13268ce3076962609f7c08451f3ab6324ddcd1145d632b69e4dda`  
		Last Modified: Wed, 28 Dec 2016 21:47:20 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
