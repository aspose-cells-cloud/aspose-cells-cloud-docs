---
title: 如何运行 Docker 容器
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: 如何运行 Docker Aspose.Cells 云容器。 Aspose.Cells Cloud 支持Excel 创建、转换、合并、拆分、保护、内部对象操作等
weight: 100
---
这**码头工人**技术旨在通过使用轻量级容器自动部署应用程序。开发人员可以使用**码头集装箱**将应用程序及其所有库和依赖项打包，并将所有内容部署为一个包。

 Aspose.Cells 云团队发布了 Docker 容器[泊坞枢纽](https://hub.docker.com/r/aspose/cells-cloud)方便Docker用户。以下部分将指导您如何运行 Docker 命令或在 Yaml 文件中为 Docker 组合工具编写配置。

## 容器配置

### 所需数量

|容器中的挂载路径|描述|
|:- |:- |
|C:\字体|带有字体的文件夹，将用于呈现文档|
|C:\数据|文件存放文件夹|

### 参数

|姓名|描述|
|:- |:- |
|许可证公钥|许可证的公钥|
|许可证私钥|许可证的私钥|


如果省略“License”参数，应用程序将在试用模式下运行。


### 使用命令行运行 Docker 容器

从中拉取容器后，您可以简单地运行以下 docker 命令[泊坞枢纽](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```

### Docker-Compose 工具的配置

您可以在 Docker-Compose 工具的 yaml 文件中编写以下配置：

```JAVA
AsposeCellsCloud:
      image: aspose/cells-cloud
      ports: ["5000:80"]
      volumes: [
        "C:/Windows/Fonts:C:/Windows/Fonts",
        "c:/data:c:/data",
      ]
      environment:
        "LicensePublicKey": "yourKeyHere"
        "LicensePrivateKey": "yourKeyHere"
```
