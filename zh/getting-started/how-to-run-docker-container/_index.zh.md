---
title: 如何运行 Docker 容器
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: 如何运行 Docker Aspose.Cells 云容器。 Aspose.Cells 云支持Excel创建、转换、合并、拆分、保护、内部对象操作等
weight: 100
---
这**码头工人**该技术旨在通过使用轻量级容器来自动化应用程序的部署。开发人员可以使用**Docker容器**将应用程序及其所有库和依赖项包装起来，并将所有内容部署为单个包。

 Aspose.Cells 云团队已在[码头工人中心](https://hub.docker.com/r/aspose/cells-cloud)方便Docker用户。以下部分将指导您如何运行 Docker 命令或在 Docker compose 工具的 Yaml 文件中编写配置。

## 容器配置

### 所需数量

|容器中的挂载路径|描述|
|:- |:- |
|C:\字体|包含字体的文件夹，将用于渲染文档|
|C:\数据|文件存放文件夹|

### 参数

|姓名|描述|
|:- |:- |
|许可证公钥|许可证的公钥|
|许可证私钥|许可证私钥|


如果省略“License”参数，应用程序将以试用模式运行。


### 使用命令行运行 Docker 容器

您只需在从容器中拉取容器后运行以下 docker 命令即可[码头工人中心](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

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
