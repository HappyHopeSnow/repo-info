## `wordpress:php7.0-fpm-alpine`

```console
$ docker pull wordpress@sha256:ed8b42b7cf4f3e00666ee81142bbe60d70c6d7aa6392707693bfea7e44cb6f8b
```

-	Platforms:
	-	linux; amd64

### `wordpress:php7.0-fpm-alpine` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39251889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67164762a42e5799d084673bcaab310e6acb8d91c413bdac40b2628b9c682b49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

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
# Tue, 27 Dec 2016 19:31:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Tue, 27 Dec 2016 19:31:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Tue, 27 Dec 2016 19:31:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Tue, 27 Dec 2016 19:31:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Tue, 27 Dec 2016 20:06:50 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763
# Tue, 27 Dec 2016 20:06:51 GMT
ENV PHP_VERSION=7.0.14
# Tue, 27 Dec 2016 20:06:51 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.14.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.14.tar.xz.asc/from/this/mirror
# Tue, 27 Dec 2016 20:06:51 GMT
ENV PHP_SHA256=0f1dff6392a1cc2ed126b9695f580a2ed77eb09d2c23b41cabfb41e6f27a8c89 PHP_MD5=a51f1d4f03f4e4c745856e9f76fca476
# Tue, 27 Dec 2016 20:06:58 GMT
RUN set -xe; 		apk add --no-cache --virtual .fetch-deps 		gnupg 		openssl 	; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apk del .fetch-deps
# Tue, 27 Dec 2016 20:06:59 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Tue, 27 Dec 2016 20:17:52 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		curl-dev 		libedit-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& ./configure 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(getconf _NPROCESSORS_ONLN)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& runDeps="$( 		scanelf --needed --nobanner --recursive /usr/local 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --no-cache --virtual .php-rundeps $runDeps 		&& apk del .build-deps
# Tue, 27 Dec 2016 20:17:53 GMT
COPY multi:5c1cc33896847ec6f8a128a1494e83c37aea885824061e1b8e308f9e09499956 in /usr/local/bin/ 
# Tue, 27 Dec 2016 20:17:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 27 Dec 2016 20:17:54 GMT
WORKDIR /var/www/html
# Tue, 27 Dec 2016 20:17:56 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = [::]:9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 27 Dec 2016 20:17:56 GMT
EXPOSE 9000/tcp
# Tue, 27 Dec 2016 20:17:57 GMT
CMD ["php-fpm"]
# Tue, 27 Dec 2016 22:11:15 GMT
RUN apk add --no-cache 		bash 		sed
# Tue, 27 Dec 2016 22:11:50 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		libjpeg-turbo-dev 		libpng-dev 	; 		docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr; 	docker-php-ext-install gd mysqli opcache; 		runDeps="$( 		scanelf --needed --nobanner --recursive 			/usr/local/lib/php/extensions 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)"; 	apk add --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del .build-deps
# Tue, 27 Dec 2016 22:12:00 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 27 Dec 2016 22:12:01 GMT
VOLUME [/var/www/html]
# Fri, 13 Jan 2017 19:38:03 GMT
ENV WORDPRESS_VERSION=4.7.1
# Fri, 13 Jan 2017 19:38:04 GMT
ENV WORDPRESS_SHA1=8e56ba56c10a3f245c616b13e46bd996f63793d6
# Fri, 13 Jan 2017 19:38:06 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Fri, 13 Jan 2017 19:38:07 GMT
COPY file:0d5c945fedcf9886801149dd830388361dfc1a00e4f95510833987f19e98e986 in /usr/local/bin/ 
# Fri, 13 Jan 2017 19:38:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 19:38:08 GMT
CMD ["php-fpm"]
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
	-	`sha256:9c932d51f8969f8927aca95461ea7f2464ce48f64a11a1809041731e9cfe7991`  
		Last Modified: Tue, 27 Dec 2016 21:23:09 GMT  
		Size: 12.7 MB (12707446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b3641112dacbf6c12175ac7a7767c3e4c48252371f4cd30733a1966d4e9847`  
		Last Modified: Tue, 27 Dec 2016 21:23:05 GMT  
		Size: 484.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a662e9e65f9a2f281d57882377e629d2017753c744f8237c84465b154d6991`  
		Last Modified: Tue, 27 Dec 2016 21:23:13 GMT  
		Size: 14.0 MB (14029671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed19f787696118272d5df6f0c38eb5e6655de17d9bad6a58aef35a2b0c52104`  
		Last Modified: Tue, 27 Dec 2016 21:23:05 GMT  
		Size: 2.0 KB (2006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f4a3aefe522db6e4a1d97e81a22a6e8ffdc3da40c2a874bdb601e3212961fe`  
		Last Modified: Tue, 27 Dec 2016 21:23:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2c2bfd87757f1aee2dfe86b0bd85a026164268af8d5d1974b310eb2b6c0463`  
		Last Modified: Tue, 27 Dec 2016 21:23:05 GMT  
		Size: 7.7 KB (7677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288aae37db2ac5c46516bffe111837e8fdc7e77c6efbbf9d1f727a8ca3280de4`  
		Last Modified: Tue, 27 Dec 2016 22:37:57 GMT  
		Size: 590.0 KB (589979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82d562e22c3d31233e283e3822166147023325ba64d90a152f3fdc4740c1b84`  
		Last Modified: Tue, 27 Dec 2016 22:37:58 GMT  
		Size: 721.9 KB (721910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9bedbd8fd6095b1c8d45369425aaa45862c1377cfc610a6e2bcfaebdd62e81`  
		Last Modified: Tue, 27 Dec 2016 22:37:57 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052c0f63bb3a028fbbe24797a8fac3a1107df8b9db5cfaaf360584474d60a27f`  
		Last Modified: Fri, 13 Jan 2017 19:49:57 GMT  
		Size: 7.8 MB (7826285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01a651e638636a164b28007a57e5301ede28f6fb029b4aebe86e3f258b87ff2`  
		Last Modified: Fri, 13 Jan 2017 19:49:55 GMT  
		Size: 2.9 KB (2929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
