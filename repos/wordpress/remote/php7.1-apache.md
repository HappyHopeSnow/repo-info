## `wordpress:php7.1-apache`

```console
$ docker pull wordpress@sha256:edd23f3309054e20b1fba618c96d1dbbfab9b207913b3c5b623c3bc9be3fc526
```

-	Platforms:
	-	linux; amd64

### `wordpress:php7.1-apache` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168392956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b1d6fefe53e12df3ae122860c922d07cd09431b5d0e828f2a58a198a98238a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

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
# Wed, 14 Dec 2016 14:55:33 GMT
RUN apt-get update && apt-get install -y apache2-bin apache2.2-common --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 14:55:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 14 Dec 2016 14:55:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 14 Dec 2016 14:55:35 GMT
RUN set -ex 		&& sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS" 		&& . "$APACHE_ENVVARS" 	&& for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		/var/www/html 	; do 		rm -rvf "$dir" 		&& mkdir -p "$dir" 		&& chown -R "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 	done
# Wed, 14 Dec 2016 14:55:36 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 14 Dec 2016 14:55:37 GMT
RUN set -ex 	&& . "$APACHE_ENVVARS" 	&& ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log" 	&& ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"
# Wed, 14 Dec 2016 14:55:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 14 Dec 2016 14:55:38 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Wed, 14 Dec 2016 14:55:39 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2
# Wed, 14 Dec 2016 14:55:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Wed, 14 Dec 2016 14:55:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Wed, 14 Dec 2016 14:55:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Wed, 14 Dec 2016 14:55:40 GMT
ENV GPG_KEYS=A917B1ECDA84AEC2B568FED6F50ABC807BD5DCD0
# Wed, 14 Dec 2016 14:55:40 GMT
ENV PHP_VERSION=7.1.0
# Wed, 14 Dec 2016 14:55:41 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.1.0.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.1.0.tar.xz.asc/from/this/mirror
# Wed, 14 Dec 2016 14:55:41 GMT
ENV PHP_SHA256=a810b3f29c21407c24caa88f50649320d20ba6892ae1923132598b8a0ca145b6 PHP_MD5=cf36039303c47f493100afea522a8f53
# Wed, 14 Dec 2016 14:55:52 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove $fetchDeps
# Wed, 14 Dec 2016 14:55:53 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Wed, 14 Dec 2016 14:58:18 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& ./configure 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps
# Mon, 19 Dec 2016 19:25:30 GMT
COPY multi:2b7e23dbf0e975ef1ec1f186511e2789ab94e8c8734ca9fa8419c893f7357d6c in /usr/local/bin/ 
# Mon, 19 Dec 2016 19:25:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 Dec 2016 19:25:31 GMT
COPY file:3014772111b66da3129ca8caeafdd1dcfa9a3bf518f015ae9acc3c7b9b1b44c9 in /usr/local/bin/ 
# Mon, 19 Dec 2016 19:25:32 GMT
WORKDIR /var/www/html
# Mon, 19 Dec 2016 19:25:32 GMT
EXPOSE 80/tcp
# Mon, 19 Dec 2016 19:25:32 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jan 2017 23:58:41 GMT
RUN set -ex; 		apt-get update; 	apt-get install -y 		libjpeg-dev 		libpng12-dev 	; 	rm -rf /var/lib/apt/lists/*; 		docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr; 	docker-php-ext-install gd mysqli opcache
# Fri, 06 Jan 2017 23:58:42 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 06 Jan 2017 23:58:43 GMT
RUN a2enmod rewrite expires
# Fri, 06 Jan 2017 23:58:44 GMT
VOLUME [/var/www/html]
# Fri, 13 Jan 2017 19:38:09 GMT
ENV WORDPRESS_VERSION=4.7.1
# Fri, 13 Jan 2017 19:38:10 GMT
ENV WORDPRESS_SHA1=8e56ba56c10a3f245c616b13e46bd996f63793d6
# Fri, 13 Jan 2017 19:38:12 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Fri, 13 Jan 2017 19:38:13 GMT
COPY file:0d5c945fedcf9886801149dd830388361dfc1a00e4f95510833987f19e98e986 in /usr/local/bin/ 
# Fri, 13 Jan 2017 19:38:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Jan 2017 19:38:14 GMT
CMD ["apache2-foreground"]
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
	-	`sha256:f0a3d7c702e3016084af8e44630e2f706a34f4491d2e92334de6ce72590de967`  
		Last Modified: Wed, 14 Dec 2016 16:22:16 GMT  
		Size: 2.8 MB (2849496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b7d2c4c9cc51259b13fa250aab59702bf26bf6d04e64c6bc71e18c5be30067`  
		Last Modified: Wed, 14 Dec 2016 16:22:14 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3fbbff60a9ec3f682af9f3502f05707866a9230290b870994b27676e57d5eb`  
		Last Modified: Wed, 14 Dec 2016 16:22:11 GMT  
		Size: 425.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336c38203cc25a4cc35e2de549a1787a6e27142a023da0e0238e10c290fe6665`  
		Last Modified: Wed, 14 Dec 2016 16:22:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628c443fd26f8db61077f442d38b3726ecf6c6138fc7b36a0a8c9e041cda27be`  
		Last Modified: Wed, 14 Dec 2016 16:22:12 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488d6737080b379a8ee91ab509a38b66b4d253fe59105e8b2b71e48e4ca44722`  
		Last Modified: Wed, 14 Dec 2016 16:22:33 GMT  
		Size: 12.9 MB (12924566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09922121d03fb8faaa3510988228573ed96f730e1f7302f8e3ccb2f4e3374c87`  
		Last Modified: Wed, 14 Dec 2016 16:22:08 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2cc6ada1a67704476bf1191be0b8837e70486fef1056a47c7a277d7d12c23d`  
		Last Modified: Wed, 14 Dec 2016 16:22:13 GMT  
		Size: 13.6 MB (13596997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92d3155988765c7e54ee7a57757e50a58da0f6bcc06ba8802514d872067f463`  
		Last Modified: Mon, 19 Dec 2016 19:35:54 GMT  
		Size: 2.0 KB (2014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6ab278e229a1bccece0327acca0ca077cbe1bd87b3dd87215aea71cb929dce`  
		Last Modified: Mon, 19 Dec 2016 19:35:54 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928702a1813f2ae5ddffc49fc87ebd2fe2ed1b754445a9b8dbded05fd055dcd3`  
		Last Modified: Sat, 07 Jan 2017 00:12:15 GMT  
		Size: 2.2 MB (2231575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff05ce22eebae72819d83fb717faabfb9942b081dbcec44ab33d1920bf9b4c67`  
		Last Modified: Sat, 07 Jan 2017 00:12:14 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195d8c1a33f9f8e5060bb0734a7c24b43f007151d5153e09e883a377a47befbd`  
		Last Modified: Sat, 07 Jan 2017 00:12:14 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54ff62f820fb65dc090028d2419004296bc2f16ecb1fb60533153fc94fd2e05`  
		Last Modified: Fri, 13 Jan 2017 19:51:01 GMT  
		Size: 7.8 MB (7826192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d4d8ab59b42feed60e2c0e795398550efd268d2a613659535ff2bc8050c123`  
		Last Modified: Fri, 13 Jan 2017 19:50:59 GMT  
		Size: 2.9 KB (2936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
