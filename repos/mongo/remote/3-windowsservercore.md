## `mongo:3-windowsservercore`

```console
$ docker pull mongo@sha256:fe9004ce4ae20d6a1ff8c984ee1336ac32b1008c846d90e56b03440b81d99630
```

-	Platforms:
	-	windows; amd64

### `mongo:3-windowsservercore` - windows; amd64

-	Docker Version: 1.12.2-cs2-ws-beta
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 GB (4991318628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2480b14896c666c28d7e561e2638148f5772b4138e005110ab4ee913fff81c`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Jan 2017 23:27:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 06 Jan 2017 23:30:21 GMT
ENV MONGO_VERSION=3.4.1
# Fri, 06 Jan 2017 23:30:25 GMT
ENV MONGO_DOWNLOAD_URL=http://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.1-signed.msi
# Fri, 06 Jan 2017 23:30:29 GMT
ENV MONGO_DOWNLOAD_SHA256=c530c16b35cbc455d85700991bf96978a3dd1bab89ba7a11ff360777334e006a
# Fri, 06 Jan 2017 23:31:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 06 Jan 2017 23:31:37 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 06 Jan 2017 23:31:40 GMT
EXPOSE 27017/tcp
# Fri, 06 Jan 2017 23:31:44 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:04ee5d718c7adc0144556d740900f778129e41be806c95191710d1d92051a7b3`  
		Size: 854.4 MB (854419699 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f0ff1ee712365925730d5bdda1284ee8e09aa3f7969e5f679f4914fe8c712c12`  
		Last Modified: Fri, 06 Jan 2017 23:32:02 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499352f0ec04cfe2e9e0da498d98f1f6529be591c49f1e7d6c60e6290b6484e4`  
		Last Modified: Fri, 06 Jan 2017 23:32:59 GMT  
		Size: 1.2 KB (1226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e604f6c0987c2f2611a6d513e5378bab3219b181d3e3531c3d02d759b846c8`  
		Last Modified: Fri, 06 Jan 2017 23:32:56 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cd796568efe78d089a175f718cf89ab9fb3790f34f859b1f97ff0447dd12ca`  
		Last Modified: Fri, 06 Jan 2017 23:32:48 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c8543559f8ac88542999a9150021875aa749e869052ed22b28c9795da946a6`  
		Last Modified: Fri, 06 Jan 2017 23:33:02 GMT  
		Size: 66.9 MB (66904501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fbac1e090b0eb7ea1ac281dc00fbe09fd3d928f64244cf1903275c9a47ffa5c`  
		Last Modified: Fri, 06 Jan 2017 23:32:47 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732b653b9719e64a7658273ff12e81e2a046dda878eb914f891ae311e7471b06`  
		Last Modified: Fri, 06 Jan 2017 23:32:47 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fd043dbb36cdf4d7a2cf4c3ae93231382ba934f41aacef13b096d2f61db016`  
		Last Modified: Fri, 06 Jan 2017 23:32:47 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
