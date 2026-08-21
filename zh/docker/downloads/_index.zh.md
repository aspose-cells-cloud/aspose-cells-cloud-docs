---
title: "Aspose.Cells Cloud Docker 镜像下载"
second_title: "文档"
ArticleTitle: "Aspose.Cells Cloud Docker 镜像下载"
linktitle: "镜像下载"
type: docs
url: /docker/downloads/
description: "获取适用于 Windows Server 2016/2019 和 Linux 的最新 Aspose.Cells Cloud Docker 镜像。按照分步说明、前置条件和安全建议，在本地运行容器。"
weight: 30
keywords: "Aspose.Cells, 云, Docker, 容器, 镜像, 下载, Windows Server, Linux, REST API"
---

## 概述

`aspose/cells-cloud` —— 托管 **Aspose.Cells Cloud** REST API 的官方 Docker 镜像。该镜像允许您在容器内运行完整的电子表格处理引擎，从而支持离线或私有云部署，无需依赖 Aspose 的公共云服务。

**最后更新时间：** 2026-06-30

**快速入门清单**

- 确认 Docker Engine 版本为 20.10 或更高。
- 根据您的操作系统拉取相应镜像（参见下方各节）。
- 设置 `ASPOSE_CLIENT_ID` 和 `ASPOSE_CLIENT_SECRET` 环境变量。
- 运行容器，并将主机端口 8080 映射到容器内部端口 80。

---

## 前置条件

| 要求 | 详情 |
|------|------|
| **Docker Engine** | 已在主机操作系统上安装 Docker 20.10 或更高版本。 |
| **操作系统** | Windows Server 2016、Windows Server 2019 或任意现代 Linux 发行版。 |
| **Docker Hub 访问权限** | 一个有效的 Docker Hub 账户（可选，但推荐用于私有镜像）。若需从私有仓库拉取镜像，请运行 `docker login`。 |
| **Aspose Cloud 凭据** | `ASPOSE_CLIENT_ID` 和 `ASPOSE_CLIENT_SECRET` —— 可从 Aspose Cloud 仪表板获取。 |

> **提示：** 使用 `docker --version` 验证 Docker 是否安装成功。

---

## Windows Server 2016

```powershell
docker pull aspose/cells-cloud:ltsc2016.21.9
```

---

## Windows Server 2019

```powershell
docker pull aspose/cells-cloud:ltsc2019.21.9
```

---

## Linux

```sh
docker pull aspose/cells-cloud:linux.21.9
```

---

## 运行容器

```sh
docker run -d \
  -e ASPOSE_CLIENT_ID=YOUR_CLIENT_ID \
  -e ASPOSE_CLIENT_SECRET=YOUR_CLIENT_SECRET \
  -p 8080:80 \
  --name aspose-cells \
  aspose/cells-cloud:ltsc2019.21.9
```

* **环境变量** —— `ASPOSE_CLIENT_ID` 和 `ASPOSE_CLIENT_SECRET` 提供 API 所需的凭据。  
* **端口映射** —— 容器暴露端口 80；请将其映射至主机端口（例如 8080）以访问服务。  
* **后台运行模式（`-d`）** —— 在后台运行容器。  

---

## 版本与更新

| 操作系统 | 标签 | 发布日期 | 如何获取最新版本 |
|----------|------|----------|------------------|
| Windows Server 2016 | `ltsc2016.21.9` | 2026-06-30 | `docker pull aspose/cells-cloud:ltsc2016.latest` |
| Windows Server 2019 | `ltsc2019.21.9` | 2026-06-30 | `docker pull aspose/cells-cloud:ltsc2019.latest` |
| Linux | `linux.21.9` | 2026-06-30 | `docker pull aspose/cells-cloud:linux.latest` |

> **注意：** 标签 `21.9` 为当前稳定版本。如需更高版本，请使用 `latest` 标签，或查阅 [Aspose.Cells Cloud 发布说明](/cells/release-notes/)。

---

## 验证与安全

* **镜像摘要校验**

  ```sh
  docker image inspect aspose/cells-cloud:ltsc2019.21.9 --format='{{.RepoDigests}}'
  ```

* **漏洞扫描**（推荐）

  ```sh
  trivy image aspose/cells-cloud:ltsc2019.21.9
  ```

* **最佳实践** —— 保持 Docker 为最新版本；以最小权限运行容器；定期扫描镜像以检测已知 CVE 漏洞。

* **结构化数据（JSON-LD）示例**

  ```html
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "SoftwareApplication",
    "name": "Aspose.Cells Cloud Docker 镜像",
    "operatingSystem": "Windows Server 2016/2019, Linux",
    "softwareVersion": "21.9",
    "downloadUrl": "https://hub.docker.com/r/aspose/cells-cloud",
    "offers": {
      "price": "0",
      "priceCurrency": "USD"
    }
  }
  </script>
  ```

---

## 常见问题及故障排除

| 现象 | 可能原因 | 解决方法 |
|------|----------|----------|
| `docker: command not found` | Docker 未安装或 PATH 未设置 | 安装 Docker 并重启终端。 |
| 拉取镜像时认证失败 | 缺少或错误的 `docker login` | 使用有效的 Docker Hub 凭据运行 `docker login`。 |
| 容器立即退出 | 缺少必需的环境变量 | 按照 **运行容器** 一节所示提供 `ASPOSE_CLIENT_ID` 和 `ASPOSE_CLIENT_SECRET`。 |
| 主机端口冲突 | 主机端口已被占用 | 更换主机端口（例如 `-p 8081:80`）。 |

---

## 参考链接

* [Aspose.Cells Cloud API 文档](/cells/cloud/api/)
* [Aspose.Cells Cloud 发布说明](/cells/release-notes/) —— 包含版本 21.9 及更高版本的详细变更日志。
* [Aspose.Cells Docker 容器功能](/cells/docker/features/)
* [Aspose.Cells Docker 镜像标签列表](/cells/docker/tag-list/)

---

*作者：Aspose Cloud 工程团队*