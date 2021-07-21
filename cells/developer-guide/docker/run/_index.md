---
title: "Run"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /docker/run/
description: "How to run Aspose.Cells Cloud for Docker."
weight: 30
---

## Expose Port 

Port	| Description | Required
---|:--:|---:
5000 | 	Folder with fonts, which will be used to render documents | true


## Required volumes ##
Mount path in container	| Description | Required
---|:--:|---:
C:\fonts | 	Folder with fonts, which will be used to render documents | false
C:\data |	File storage folder | false

## Run Parameters ##

Name |	Description | Required
---|:--:|---:
LicensePublicKey | Public key of the license   | true
LicensePrivateKey	| Private key of the license  | true
storagesCredentialsFilePath | Storage configure file path. Default file is ./storageResource.json  | true

## Run Command ##

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows

docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux

docker run  -d  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud


```

{{< /tab >}}

{{< /tabs >}}


**Reference Document** : 
  - [Docker Run]( https://docs.docker.com/engine/reference/commandline/run/)