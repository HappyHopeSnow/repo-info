## `joomla:fpm`

```console
$ docker pull joomla@sha256:5b71e4d9e93107f7156f1f8082a2971462b0234381da37018ac10f788373b665
```

-	Platforms:
	-	linux; amd64

### `joomla:fpm` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.8 MB (161756575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585107cef5233b573aaf461d71adb83e099705adf22dd7446becfa4dde9ccb5b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 14:43:54 GMT
ENV PHPIZE_DEPS=autoconf 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 14 Dec 2016 14:44:25 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Wed, 14 Dec 2016 14:44:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Dec 2016 14:44:27 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Wed, 14 Dec 2016 14:58:21 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Wed, 14 Dec 2016 14:58:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Wed, 14 Dec 2016 14:58:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Wed, 14 Dec 2016 14:58:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Wed, 14 Dec 2016 15:57:37 GMT
ENV GPG_KEYS=0BD78B5F97500D450838F95DFE857D9A90D90EC1 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Wed, 14 Dec 2016 15:57:38 GMT
ENV PHP_VERSION=5.6.29
# Wed, 14 Dec 2016 15:57:38 GMT
ENV PHP_URL=https://secure.php.net/get/php-5.6.29.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-5.6.29.tar.xz.asc/from/this/mirror
# Wed, 14 Dec 2016 15:57:38 GMT
ENV PHP_SHA256=0ff352a433f73e2c82b0d5b283b600402518569bf72a74e247f356dacbf322a7 PHP_MD5=190bf5b52d1fc68d5500a8cdc7e33164
# Wed, 14 Dec 2016 15:57:53 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove $fetchDeps
# Wed, 14 Dec 2016 15:57:53 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Wed, 14 Dec 2016 16:01:04 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& ./configure 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps
# Mon, 19 Dec 2016 19:26:18 GMT
COPY multi:5c1cc33896847ec6f8a128a1494e83c37aea885824061e1b8e308f9e09499956 in /usr/local/bin/ 
# Mon, 19 Dec 2016 19:26:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 Dec 2016 19:26:19 GMT
WORKDIR /var/www/html
# Mon, 19 Dec 2016 19:26:20 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = [::]:9000'; 	} | tee php-fpm.d/zz-docker.conf
# Mon, 19 Dec 2016 19:26:20 GMT
EXPOSE 9000/tcp
# Mon, 19 Dec 2016 19:26:21 GMT
CMD ["php-fpm"]
# Mon, 19 Dec 2016 23:11:54 GMT
MAINTAINER Michael Babker <michael.babker@joomla.org> (@mbabker)
# Mon, 19 Dec 2016 23:12:17 GMT
RUN apt-get update && apt-get install -y libpng12-dev libjpeg-dev libmcrypt-dev zip unzip && rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr 	&& docker-php-ext-install gd
# Mon, 19 Dec 2016 23:12:32 GMT
RUN docker-php-ext-install mysqli
# Mon, 19 Dec 2016 23:12:47 GMT
RUN docker-php-ext-install mcrypt
# Mon, 19 Dec 2016 23:12:47 GMT
VOLUME [/var/www/html]
# Wed, 04 Jan 2017 23:35:45 GMT
ENV JOOMLA_VERSION=3.6.5
# Wed, 04 Jan 2017 23:35:45 GMT
ENV JOOMLA_SHA1=3143994bb5520c249961cbb5bc297c149399f4b7
# Wed, 04 Jan 2017 23:35:54 GMT
RUN curl -o joomla.zip -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.zip 	&& echo "$JOOMLA_SHA1 *joomla.zip" | sha1sum -c - 	&& mkdir /usr/src/joomla 	&& unzip joomla.zip -d /usr/src/joomla 	&& rm joomla.zip 	&& chown -R www-data:www-data /usr/src/joomla
# Wed, 04 Jan 2017 23:36:00 GMT
COPY file:27ca5c0b8509d6681e80aa6cd05b2e2e68da2f59fb0ee7fa2aa581f55d362b6d in /entrypoint.sh 
# Wed, 04 Jan 2017 23:36:00 GMT
COPY file:7328ebe063e26f7b7716dfd8778bb7d46b90702ea38b23b9147ba2fd837ac2c1 in /makedb.php 
# Wed, 04 Jan 2017 23:36:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Jan 2017 23:36:01 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d8a4e038be43b07879494a44b3b14e668537bd8b4be6d1cf2d22c7bf8b7f35`  
		Last Modified: Wed, 14 Dec 2016 16:18:52 GMT  
		Size: 77.6 MB (77591778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d4d961577a0338c7bf65f9811429611781ba5f6c7c7069e70f6035a0990e3f`  
		Last Modified: Wed, 14 Dec 2016 16:18:25 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54283fea14a4c4ba021ba260178aa1c3c7c26b2254d3a93b94a0b04392b71ba0`  
		Last Modified: Wed, 14 Dec 2016 16:37:09 GMT  
		Size: 12.6 MB (12556563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b82ddb6e57bfc8c4e5b31f6d835fda3dc99089f197d316edb0e5ee83c01b35`  
		Last Modified: Wed, 14 Dec 2016 16:37:04 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe532c7957188a214e0af6de42e16e31e94f0851067862fe771b6ed13068ca56`  
		Last Modified: Wed, 14 Dec 2016 16:37:07 GMT  
		Size: 8.8 MB (8763779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02389f3f13e01ffc75bfc899cfc486f335d9f947b24416d94166bba809930c8`  
		Last Modified: Mon, 19 Dec 2016 19:50:28 GMT  
		Size: 2.0 KB (2009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5777f6cf03c51cbb0ddabad4f1a51770b3f9c216f3da58eddc960b602a60a0c0`  
		Last Modified: Mon, 19 Dec 2016 19:50:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b45111f193e3f3fa5d7e118b2eb42b950bb1252313bf30b7f5b8268782d43b`  
		Last Modified: Mon, 19 Dec 2016 19:50:28 GMT  
		Size: 7.6 KB (7630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0244f046d4e53ac8b275899a2054edcbe6429ea796fa77fcaac2b43b9d67f30`  
		Last Modified: Mon, 19 Dec 2016 23:19:06 GMT  
		Size: 2.7 MB (2717956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db26bc76155d524539bb5552bb68d57a4a7f439290daf7268e7411ec3704b60`  
		Last Modified: Mon, 19 Dec 2016 23:19:03 GMT  
		Size: 56.9 KB (56910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9042e86c3d5c3d926d0e00faec065a599f256c988146678c70d18f0d31447287`  
		Last Modified: Mon, 19 Dec 2016 23:19:03 GMT  
		Size: 19.3 KB (19291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4226949442db6c77c6112a722864af44ec281127427a42dd015f730145329ad5`  
		Last Modified: Wed, 04 Jan 2017 23:41:17 GMT  
		Size: 8.7 MB (8674971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cdf70aaf9fa2c4ef21383484007ee7cc8882ec45678671401daf362e56c4f8`  
		Last Modified: Wed, 04 Jan 2017 23:41:16 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949cbb671156fe0ef973d2dfbb9e1040f0325d055fe7acb85ca2a81576fb7777`  
		Last Modified: Wed, 04 Jan 2017 23:41:14 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
