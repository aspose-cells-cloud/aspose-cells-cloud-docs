---
title: 如何运行 Aspose.Cells Cloud Docker 容器：通过 3 步运行官方 Aspose.Cells Cloud 容器：拉取、配置、启动
second_title: Documen
ArticleTitle: How to Run Aspose.Cells Cloud Docker Containe
LinkTitle: Docker Containe
type: docs
url: /zh/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: 如何运行 Docker Aspose.Cells Cloud 容器。Aspose.Cells Cloud 支持 Excel 创建、转换、合并、拆分、保护、内部对象操作等
weight: 100
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdown、如何运行 Docker 容器
---
这**Docker**该技术旨在通过使用轻量级容器实现应用程序的自动化部署。开发人员可以使用**Docker容器**将应用程序及其所有库和依赖项打包起来，并将所有内容部署为单个包。

 Aspose.Cells 云团队已在[Docker 中心](https://hub.docker.com/r/aspose/cells-cloud)为了方便 Docker 用户，以下章节将指导您如何运行 Docker 命令或在 Docker Compose 工具的 Yaml 文件中编写配置。

## 容器配置

### 所需卷

|容器中的挂载路径|描述|
|:- |:- |
|C:\字体|包含字体的文件夹，用于呈现文档|
|C:\数据|文件存储文件夹|

### 参数

|姓名|描述|
|:- |:- |
|许可证公钥|许可证的公钥|
|许可证私钥|许可证的私钥|

如果省略“许可证”参数，应用程序将以试用模式运行。

### 1. 拉取 Aspose.Cells 云镜像

```bash
# Pull Aspose.Cells Cloud Image latest version
docker pull aspose/cells-cloud:latest
```

```powershell
# Pull Aspose.Cells Cloud Image  version on windows server 2019
docker pull aspose/cells-cloud:ltsc2019.25.9.0 
# Pull Aspose.Cells Cloud Image  version on windows server 2022
docker pull aspose/cells-cloud:ltsc2022.25.9.0 

# Pull Aspose.Cells Cloud Image  version on windows 11
docker pull aspose/cells-cloud:ltsc2019.25.9.0 
```

### 2. Docker-Compose工具的配置

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

### 3. 使用命令行运行 Docker 容器

您只需在从以下位置拉出容器后运行以下 docker 命令即可[Docker 中心](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```
