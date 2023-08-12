---
title: 汝
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/docker/run/
description: 如何运行Aspose.Cells Cloud for Docker
weight: 30
---
## 暴露端口

港口|描述 |必需的
---|:--:|---:
5000 |带有字体的文件夹，将用于渲染文档 |真的


## 所需数量 ##
容器中的挂载路径 |描述 |必需的
---|:--:|---:
C:\字体|带有字体的文件夹，将用于渲染文档 |错误的
C：\数据|文件存放文件夹|错误的

## 运行参数 ##

名称 |描述 |必需的
---|:--:|---:
许可证公钥 |许可证的公钥 |真的
许可证私钥 |许可证私钥 |真的
存储凭证文件路径 |存储配置文件路径。默认文件是 ./storageResource.json |真的

## 运行命令 ##

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows

docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux

docker run  -d  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0


```

{{< /tab >}}

{{< /tabs >}}


**参考文件** : 
  - [码头运行]( https://docs.docker.com/engine/reference/commandline/run/)