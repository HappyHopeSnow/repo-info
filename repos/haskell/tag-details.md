<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `haskell`

-	[`haskell:8.0.1`](#haskell801)
-	[`haskell:8.0`](#haskell80)
-	[`haskell:8`](#haskell8)
-	[`haskell:latest`](#haskelllatest)

## `haskell:8.0.1`

```console
$ docker pull haskell@sha256:0399b393fc7e58bc8bcf6d274b55e47eb1a2e7ac9a2ac18d8f35fb3fa2322887
```

-	Platforms:
	-	linux; amd64

### `haskell:8.0.1` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255369713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25a156a6777220df0e15528568e7d2b049eeb508fd68890380acfadb3a32733`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Tue, 13 Dec 2016 23:45:10 GMT
MAINTAINER Chris Biscardi <chris@christopherbiscardi.com>
# Tue, 13 Dec 2016 23:45:10 GMT
ENV LANG=C.UTF-8
# Tue, 13 Dec 2016 23:46:43 GMT
RUN echo 'deb http://ppa.launchpad.net/hvr/ghc/ubuntu trusty main' > /etc/apt/sources.list.d/ghc.list &&     echo 'deb http://download.fpcomplete.com/debian/jessie stable main'| tee /etc/apt/sources.list.d/fpco.list &&     apt-key adv --keyserver keyserver.ubuntu.com --recv-keys F6F88286 &&     apt-key adv --keyserver keyserver.ubuntu.com --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     apt-get update &&     apt-get install -y --no-install-recommends cabal-install-1.24 ghc-8.0.1 happy-1.19.5 alex-3.1.7             stack zlib1g-dev libtinfo-dev libsqlite3-0 libsqlite3-dev ca-certificates g++ git &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:46:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/1.24/bin:/opt/ghc/8.0.1/bin:/opt/happy/1.19.5/bin:/opt/alex/3.1.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Dec 2016 23:46:45 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330a1cac2bdb1b1888281ed6ebc94b9b277b5274bb2f84e4242f18c593ba03da`  
		Last Modified: Mon, 19 Dec 2016 22:39:40 GMT  
		Size: 204.0 MB (204006588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.0`

```console
$ docker pull haskell@sha256:0399b393fc7e58bc8bcf6d274b55e47eb1a2e7ac9a2ac18d8f35fb3fa2322887
```

-	Platforms:
	-	linux; amd64

### `haskell:8.0` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255369713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25a156a6777220df0e15528568e7d2b049eeb508fd68890380acfadb3a32733`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Tue, 13 Dec 2016 23:45:10 GMT
MAINTAINER Chris Biscardi <chris@christopherbiscardi.com>
# Tue, 13 Dec 2016 23:45:10 GMT
ENV LANG=C.UTF-8
# Tue, 13 Dec 2016 23:46:43 GMT
RUN echo 'deb http://ppa.launchpad.net/hvr/ghc/ubuntu trusty main' > /etc/apt/sources.list.d/ghc.list &&     echo 'deb http://download.fpcomplete.com/debian/jessie stable main'| tee /etc/apt/sources.list.d/fpco.list &&     apt-key adv --keyserver keyserver.ubuntu.com --recv-keys F6F88286 &&     apt-key adv --keyserver keyserver.ubuntu.com --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     apt-get update &&     apt-get install -y --no-install-recommends cabal-install-1.24 ghc-8.0.1 happy-1.19.5 alex-3.1.7             stack zlib1g-dev libtinfo-dev libsqlite3-0 libsqlite3-dev ca-certificates g++ git &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:46:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/1.24/bin:/opt/ghc/8.0.1/bin:/opt/happy/1.19.5/bin:/opt/alex/3.1.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Dec 2016 23:46:45 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330a1cac2bdb1b1888281ed6ebc94b9b277b5274bb2f84e4242f18c593ba03da`  
		Last Modified: Mon, 19 Dec 2016 22:39:40 GMT  
		Size: 204.0 MB (204006588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8`

```console
$ docker pull haskell@sha256:0399b393fc7e58bc8bcf6d274b55e47eb1a2e7ac9a2ac18d8f35fb3fa2322887
```

-	Platforms:
	-	linux; amd64

### `haskell:8` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255369713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25a156a6777220df0e15528568e7d2b049eeb508fd68890380acfadb3a32733`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Tue, 13 Dec 2016 23:45:10 GMT
MAINTAINER Chris Biscardi <chris@christopherbiscardi.com>
# Tue, 13 Dec 2016 23:45:10 GMT
ENV LANG=C.UTF-8
# Tue, 13 Dec 2016 23:46:43 GMT
RUN echo 'deb http://ppa.launchpad.net/hvr/ghc/ubuntu trusty main' > /etc/apt/sources.list.d/ghc.list &&     echo 'deb http://download.fpcomplete.com/debian/jessie stable main'| tee /etc/apt/sources.list.d/fpco.list &&     apt-key adv --keyserver keyserver.ubuntu.com --recv-keys F6F88286 &&     apt-key adv --keyserver keyserver.ubuntu.com --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     apt-get update &&     apt-get install -y --no-install-recommends cabal-install-1.24 ghc-8.0.1 happy-1.19.5 alex-3.1.7             stack zlib1g-dev libtinfo-dev libsqlite3-0 libsqlite3-dev ca-certificates g++ git &&     rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:46:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/1.24/bin:/opt/ghc/8.0.1/bin:/opt/happy/1.19.5/bin:/opt/alex/3.1.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Dec 2016 23:46:45 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330a1cac2bdb1b1888281ed6ebc94b9b277b5274bb2f84e4242f18c593ba03da`  
		Last Modified: Mon, 19 Dec 2016 22:39:40 GMT  
		Size: 204.0 MB (204006588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:latest`

```console
$ docker pull haskell@sha256:f69898bed304b6abb32f0349469d2789ec379a3cff41cd1fd27cadf74d2800d5
```

-	Platforms:
	-	linux; amd64

### `haskell:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254865086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f974c5f08c220aed7bc075f70fce3b772a5b2ee09046eb309a15115f8f1765e`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 07 Nov 2016 20:30:25 GMT
ADD file:41ea5187c50116884c38d9ec51d920d79cfaeb2a61c52e07a97f457419a10a4f in / 
# Mon, 07 Nov 2016 20:30:26 GMT
CMD ["/bin/bash"]
# Tue, 08 Nov 2016 19:46:10 GMT
MAINTAINER Chris Biscardi <chris@christopherbiscardi.com>
# Tue, 08 Nov 2016 19:46:10 GMT
ENV LANG=C.UTF-8
# Tue, 08 Nov 2016 19:48:17 GMT
RUN echo 'deb http://ppa.launchpad.net/hvr/ghc/ubuntu trusty main' > /etc/apt/sources.list.d/ghc.list &&     echo 'deb http://download.fpcomplete.com/debian/jessie stable main'| tee /etc/apt/sources.list.d/fpco.list &&     apt-key adv --keyserver keyserver.ubuntu.com --recv-keys F6F88286 &&     apt-key adv --keyserver keyserver.ubuntu.com --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     apt-get update &&     apt-get install -y --no-install-recommends cabal-install-1.24 ghc-8.0.1 happy-1.19.5 alex-3.1.7             stack zlib1g-dev libtinfo-dev libsqlite3-0 libsqlite3-dev ca-certificates g++ git &&     rm -rf /var/lib/apt/lists/*
# Tue, 08 Nov 2016 19:50:46 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/1.24/bin:/opt/ghc/8.0.1/bin:/opt/happy/1.19.5/bin:/opt/alex/3.1.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Nov 2016 19:50:46 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:386a066cd84a33a04d560c42bef66d1dd64ebfc76de78550e5fd0f8d57778bca`  
		Last Modified: Mon, 07 Nov 2016 20:34:04 GMT  
		Size: 51.4 MB (51356989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedf14b47028459d4d2c5ede535e2e0a3271a1454e8d3c4fca73365e3f84f74e`  
		Last Modified: Tue, 08 Nov 2016 19:52:11 GMT  
		Size: 203.5 MB (203508097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
