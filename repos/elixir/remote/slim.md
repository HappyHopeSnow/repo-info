## `elixir:slim`

```console
$ docker pull elixir@sha256:187e7e2f62b1f9edfeb209671ebfc94b4598791cf11f5915362c96d86bbf5c22
```

-	Platforms:
	-	linux; amd64

### `elixir:slim` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156747085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17a97f44ad0424f1f2c7b59c04c83c88149eab0a0d53e747a3025a38c24fcb9`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Thu, 15 Dec 2016 23:47:20 GMT
ENV OTP_VERSION=19.2
# Thu, 15 Dec 2016 23:53:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c6adbc82a45baa49bf9f5b524089da480dd27113c51b3d147aeb196fdb90516b" 	&& runtimeDeps=' 		libodbc1 		libssl1.0.0 		libsctp1 		libwxgtk3.0-0 	' 	&& buildDeps=' 		curl 		ca-certificates 		autoconf 		gcc 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 		libwxgtk3.0-dev 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256 otp-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/otp-src 	&& tar -xzf otp-src.tar.gz -C /usr/src/otp-src --strip-components=1 	&& rm otp-src.tar.gz 	&& cd /usr/src/otp-src 	&& ./otp_build autoconf 	&& ./configure 		--enable-sctp 		--enable-dirty-schedulers 	&& make -j$(nproc) 	&& make install 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/otp-src /var/lib/apt/lists/*
# Thu, 15 Dec 2016 23:53:10 GMT
CMD ["erl"]
# Fri, 06 Jan 2017 17:47:48 GMT
ENV ELIXIR_VERSION=v1.4.0 LANG=C.UTF-8
# Fri, 06 Jan 2017 17:48:05 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/releases/download/${ELIXIR_VERSION}/Precompiled.zip" 	&& ELIXIR_DOWNLOAD_SHA256="60d077bc242e65f4f430beb43c968b5632dfb07ec89a7d689da254ffdc791b98"	&& buildDeps=' 		ca-certificates 		curl 		unzip 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-precompiled.zip $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256 elixir-precompiled.zip" | sha256sum -c - 	&& unzip -d /usr/local elixir-precompiled.zip 	&& rm elixir-precompiled.zip 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2017 17:48:05 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fd6555a8e5270c0013eb8a39cd5c7a2099be87431359a5499044fc0427d1d9`  
		Last Modified: Thu, 15 Dec 2016 23:55:08 GMT  
		Size: 101.3 MB (101332543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14f6fec84d0b806dd5885529526c37437601eea21984837d194cbe75a0980b7`  
		Last Modified: Fri, 06 Jan 2017 17:50:03 GMT  
		Size: 4.1 MB (4051417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
