---
title: 斯托拉格
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/docker/storage/
description: Aspose.Cells Cloud for Docker如何设置存储位置
weight: 30
---
## 默认存储配置 ##

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

``` json

{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "c:/data"
    }
  ]
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

``` json

{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "/data"
    }
  ]
}

```

{{< /tab >}}

{{< /tabs >}}

## 默认位置 ##


- **视窗**

```powershell

c:\app\storageResource.json

```

- **操作系统**

```linux

/app/storageResource.json


```

## 自定义存储配置 ##

当客户需要指定存储文件夹时，需要重新指定Aspose.Cells云镜像文件的存储配置文件。

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey	 -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.2.0

```

**参考文件** : 
  - [码头运行]( https://docs.docker.com/engine/reference/commandline/run/)