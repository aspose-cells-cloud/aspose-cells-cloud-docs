---
title: 如何运行 Docker
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: 如何运行Docker Aspose.Cells云容器。Aspose.Cells云支持Excel创建、转换、合并、拆分、保护、内部对象操作等
weight: 100
kwords: Excel，Office 云，REST API，电子表格，PDF，CSV，Json，Markdwon，如何运行 Docker 容器
---
这**Docker**该技术旨在通过使用轻量级容器来自动化部署应用程序。开发人员可以使用**Docker 容器**将应用程序及其所有库和依赖项打包起来，并将所有内容作为单个包进行部署。

 Aspose.Cells 云团队已在[Docker 中心](https://hub.docker.com/r/aspose/cells-cloud)以方便 Docker 用户。以下部分将指导您如何运行 Docker 命令或在 Yaml 文件中为 Docker Compose 工具编写配置。

## 容器配置

### 所需卷

|容器中的挂载路径|描述|
|:- |:- |
|字体目录|包含字体的文件夹，用于呈现文档|
|数据目录|文件存储文件夹|

### 参数

|姓名|描述|
|:- |:- |
|许可证公钥|许可证的公钥|
|许可证私钥|许可证私钥|


如果省略“许可证”参数，应用程序将以试用模式运行。


### 使用命令行运行 Docker 容器

从以下位置拉取容器后，您只需运行以下docker命令即可[Docker 中心](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```

### Docker-Compose 工具的配置

您可以在 Docker-Compose 工具的 yaml 文件中写入以下配置：

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
