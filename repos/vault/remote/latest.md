## `vault:latest`

```console
$ docker pull vault@sha256:b513e9d7f79282311145ccd5464a35ef7b293257ae610bab1ec07dc03faeb983
```

-	Platforms:
	-	linux; amd64

### `vault:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15980284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cb7dff86e478daea0112fe0bb372d58bddedbd73d60de0d93cd7acfc4a238b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 27 Dec 2016 18:17:13 GMT
ADD file:eeed5f514a35d18fcd9cbfe6c40c582211020bffdd53e4799018d33826fe5067 in / 
# Tue, 27 Dec 2016 22:08:25 GMT
MAINTAINER Jeff Mitchell <jeff@hashicorp.com> (@jefferai)
# Tue, 27 Dec 2016 22:08:26 GMT
ENV VAULT_VERSION=0.6.4
# Tue, 27 Dec 2016 22:08:26 GMT
ENV DOCKER_BASE_VERSION=0.0.4
# Tue, 27 Dec 2016 22:08:27 GMT
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 27 Dec 2016 22:08:45 GMT
RUN apk add --no-cache ca-certificates gnupg openssl libcap &&     gpg --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_linux_amd64.zip &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/docker-base/${DOCKER_BASE_VERSION}/docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS.sig docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS &&     grep ${DOCKER_BASE_VERSION}_linux_amd64.zip docker-base_${DOCKER_BASE_VERSION}_SHA256SUMS | sha256sum -c &&     unzip docker-base_${DOCKER_BASE_VERSION}_linux_amd64.zip &&     cp bin/gosu bin/dumb-init /bin &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_amd64.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_amd64.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_amd64.zip &&     cd /tmp &&     rm -rf /tmp/build &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 27 Dec 2016 22:08:46 GMT
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 27 Dec 2016 22:08:47 GMT
VOLUME [/vault/logs]
# Tue, 27 Dec 2016 22:08:47 GMT
VOLUME [/vault/file]
# Tue, 27 Dec 2016 22:08:48 GMT
EXPOSE 8200/tcp
# Tue, 27 Dec 2016 22:08:49 GMT
COPY file:01d88618f782cb03a968fcc22db42601b6f76608f95edc07ffeb2a3b7a2db58d in /usr/local/bin/docker-entrypoint.sh 
# Tue, 27 Dec 2016 22:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Dec 2016 22:08:50 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b7f33cc0b48ea4fb2f0745def58c25483a5f6b7aed5b41ce8f1cb6e17f5723cf`  
		Last Modified: Tue, 27 Dec 2016 18:18:49 GMT  
		Size: 2.3 MB (2313090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299f3e567563b4680b3e92ef983c23b1dafc05220c4304526d20ec20d22dc81c`  
		Last Modified: Tue, 27 Dec 2016 22:33:24 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34115770a8efdeac5b8bf05398acc36414797b1348883c7026f1a9143a0ea76`  
		Last Modified: Tue, 27 Dec 2016 22:33:33 GMT  
		Size: 13.7 MB (13664084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d201e1e6b3cbdbf21bf5c24029a3c6cadd876cf069e0e37d124aaecd728f04`  
		Last Modified: Tue, 27 Dec 2016 22:33:24 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eccd8c8e1c207571fb55a82df39314be397a50a9be69961394fb0945c93ca49`  
		Last Modified: Tue, 27 Dec 2016 22:33:25 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
