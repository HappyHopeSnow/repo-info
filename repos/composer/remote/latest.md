## `composer:latest`

```console
$ docker pull composer@sha256:5cd8405d83273030c28d0947b5c9600ee49706e09fe098ddbf7ebb46df0f09b0
```

-	Platforms:
	-	linux; amd64

### `composer:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53976482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3412424b56cf99b89a7402e5094cd7b37db5c166e535181dbb2ecd2669500728`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 27 Dec 2016 18:17:13 GMT
ADD file:eeed5f514a35d18fcd9cbfe6c40c582211020bffdd53e4799018d33826fe5067 in / 
# Tue, 27 Dec 2016 19:18:54 GMT
ENV PHPIZE_DEPS=autoconf 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 27 Dec 2016 19:18:56 GMT
RUN apk add --no-cache --virtual .persistent-deps 		ca-certificates 		curl 		tar 		xz
# Tue, 27 Dec 2016 19:18:57 GMT
RUN set -x 	&& addgroup -g 82 -S www-data 	&& adduser -u 82 -D -S -G www-data www-data
# Tue, 27 Dec 2016 19:19:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 27 Dec 2016 19:19:16 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Tue, 27 Dec 2016 19:19:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Tue, 27 Dec 2016 19:19:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Tue, 27 Dec 2016 19:19:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Tue, 27 Dec 2016 19:19:34 GMT
ENV GPG_KEYS=A917B1ECDA84AEC2B568FED6F50ABC807BD5DCD0
# Tue, 27 Dec 2016 19:19:50 GMT
ENV PHP_VERSION=7.1.0
# Tue, 27 Dec 2016 19:19:51 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.1.0.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.1.0.tar.xz.asc/from/this/mirror
# Tue, 27 Dec 2016 19:19:51 GMT
ENV PHP_SHA256=a810b3f29c21407c24caa88f50649320d20ba6892ae1923132598b8a0ca145b6 PHP_MD5=cf36039303c47f493100afea522a8f53
# Tue, 27 Dec 2016 19:19:58 GMT
RUN set -xe; 		apk add --no-cache --virtual .fetch-deps 		gnupg 		openssl 	; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apk del .fetch-deps
# Tue, 27 Dec 2016 19:20:04 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Tue, 27 Dec 2016 19:31:14 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		curl-dev 		libedit-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& ./configure 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(getconf _NPROCESSORS_ONLN)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --no-cache --virtual .php-rundeps $runDeps 		&& apk del .build-deps
# Tue, 27 Dec 2016 19:31:16 GMT
COPY multi:b2b2a1a4e3c0f0bb8ebdcd527fca158bfce5138468926263f86e5bb0cb41970f in /usr/local/bin/ 
# Tue, 27 Dec 2016 19:31:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 27 Dec 2016 19:31:17 GMT
CMD ["php" "-a"]
# Tue, 27 Dec 2016 22:14:09 GMT
RUN apk --no-cache add curl git subversion openssh openssl mercurial tini bash
# Tue, 27 Dec 2016 22:14:10 GMT
RUN echo "memory_limit=-1" > "$PHP_INI_DIR/conf.d/memory-limit.ini"  && echo "date.timezone=${PHP_TIMEZONE:-UTC}" > "$PHP_INI_DIR/conf.d/date_timezone.ini"
# Tue, 27 Dec 2016 22:14:11 GMT
ENV PATH=/composer/vendor/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Dec 2016 22:14:11 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 27 Dec 2016 22:14:12 GMT
ENV COMPOSER_HOME=/composer
# Tue, 10 Jan 2017 18:32:58 GMT
ENV COMPOSER_VERSION=1.3.1
# Tue, 10 Jan 2017 18:33:02 GMT
RUN curl -s -f -L -o /tmp/installer.php https://raw.githubusercontent.com/composer/getcomposer.org/2091762d2ebef14c02301f3039c41d08468fb49e/web/installer  && php -r "     \$signature = '55d6ead61b29c7bdee5cccfb50076874187bd9f21f65d8991d46ec5cc90518f447387fb9f76ebae1fbbacf329e583e30';     \$hash = hash('SHA384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {         unlink('/tmp/installer.php');         echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;         exit(1);     }"  && php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION}  && rm /tmp/installer.php  && composer --ansi --version --no-interaction
# Tue, 10 Jan 2017 18:33:02 GMT
COPY file:0b943ec33b364492b10e7a774becd40d3fec03eb7db67cc0528769b329117e32 in /docker-entrypoint.sh 
# Tue, 10 Jan 2017 18:33:02 GMT
WORKDIR /app
# Tue, 10 Jan 2017 18:33:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Jan 2017 18:33:03 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b7f33cc0b48ea4fb2f0745def58c25483a5f6b7aed5b41ce8f1cb6e17f5723cf`  
		Last Modified: Tue, 27 Dec 2016 18:18:49 GMT  
		Size: 2.3 MB (2313090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d6bcc00046712ac206a652bc839e40f8f4e6f580123a1a7ac21b92fd757364`  
		Last Modified: Tue, 27 Dec 2016 21:08:34 GMT  
		Size: 1.0 MB (1048526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3822a33fdb297624accfaaaa052a8f4850ae1450aa3edeefcfe0e693a54e689`  
		Last Modified: Tue, 27 Dec 2016 21:08:33 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a47789bbdf4b2c131bf8ba82cc36e09ad0b022627f22862898cae483511aeb`  
		Last Modified: Tue, 27 Dec 2016 21:08:33 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b85d8123005fba8a6b22aa0253a67bd1c2c08d9967cb92ca34dfde6baf70e2`  
		Last Modified: Tue, 27 Dec 2016 21:08:34 GMT  
		Size: 13.0 MB (12966695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40930b32d1c291ab8411e616a439dc8df0da3edede9f9782856479c78b9e898d`  
		Last Modified: Tue, 27 Dec 2016 21:08:30 GMT  
		Size: 483.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb18ef87fdf3d56a6b5f0c38b6439bcd598286b3edcb5e13218524ec90b3e24`  
		Last Modified: Tue, 27 Dec 2016 21:08:38 GMT  
		Size: 10.6 MB (10616412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e3579a0be73f680174361eed897e36cdbf16dc0acb2559107f7129487cecc4`  
		Last Modified: Tue, 27 Dec 2016 21:08:30 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67e6e017632d7a6934ae0f8a0817acffe1ec85f4c6118775d7fa95f8db37fb3`  
		Last Modified: Fri, 30 Dec 2016 19:50:13 GMT  
		Size: 26.5 MB (26541812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5a712a40bcc25973195779b49961f8a2288300ee0efb1b642f66ebc80039a2`  
		Last Modified: Fri, 30 Dec 2016 19:50:08 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aedcf84ef8270d20ddbad8b7fb3346e2d1b82966f03bae5b75263b0a05e6f89`  
		Last Modified: Tue, 10 Jan 2017 18:33:20 GMT  
		Size: 485.1 KB (485128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ffe27d034de659275690ee6d5d51589001d3bbfde9607f09d3e596a4fe27d7`  
		Last Modified: Tue, 10 Jan 2017 18:33:20 GMT  
		Size: 534.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c7eab4d2b566bd9ef20cb572e643ff9bd39848b20e7b104dd34866dab6ebed`  
		Last Modified: Tue, 10 Jan 2017 18:33:20 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
