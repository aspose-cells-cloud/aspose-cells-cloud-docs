---
title: 如何设置Aspose.Cells Cloud Docker 容器存储的存储位置
second_title: Documen
ArticleTitle: Aspose.Cells Cloud Docker Container Storage Configuratio
linktitle: 集装箱存储
type: docs
url: /zh/docker/storage/
description: 如何设置 Aspose.Cells Cloud Docker 容器存储的存储位置
weight: 30
kwords: Excel 云 Docker 容器、自云 Docker 容器、REST Docker 容器、电子表格、PDF、CSV、Json、Markdown、Docker 镜像、运行 Docker 容器
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

- **Linux**

```linux

/app/storageResource.json


```

## 自定义存储配置 ##

当客户需要指定存储文件夹时，需要重新指定Aspose.Cells云图像文件的存储配置文件。

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey  -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.9.0

```

**参考文献** :

- [如何运行 Aspose.Cells Cloud Docker 容器。]( https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
