---
title: "处理 Excel 图片"
second_title: "文档"
linktype: "图片"
type: docs
url: /zh/pictures/
aliases: [/zh/working-with-pictures/]
keywords: "Excel, 图片, Aspose.Cells Cloud, REST API, 图像处理, Excel 图片"
description: "了解如何使用 Aspose.Cells Cloud REST API 在 Excel 工作表中检索、添加、更新和删除图片。包含 C#、Java、Python 等语言的代码示例。"
weight: 100
ArticleTitle: "处理 Excel 图片 – Aspose.Cells Cloud 文档"
---

## 处理 Excel 文件中的图片

本指南介绍如何通过 Aspose.Cells Cloud REST API 在 Excel 工作表中处理**图片**（也称为图像）。涵盖主要的图片相关操作——检索、添加、更新和删除 Excel 图片，并提供每个任务的详细示例链接。

**前置条件**：Aspose.Cells Cloud 账户、有效的 API 密钥，以及为所选语言安装的相应 SDK。

- [如何从 Excel 工作表中获取特定格式的图片](/zh/cells/pictures/get/) – 从工作表中以指定格式（PNG、JPEG 等）检索单张图片。  
- [如何获取 Excel 工作表中所有图片的信息](/zh/cells/pictures/get-all/) – 列出工作表中每张图片的元数据（索引、名称、位置、尺寸等）。  
- [如何向 Excel 工作表添加图片](/zh/cells/pictures/add/) – 插入新图片到工作表中，并指定其位置和大小。  
- [如何更新 Excel 工作表中的特定图片](/zh/cells/pictures/update/) – 修改现有图片的属性（例如尺寸、位置等）。  
- [如何删除 Excel 工作表中的所有图片](/zh/cells/pictures/clear/) – 一次调用即可删除工作表中的所有图片对象。  
- [如何删除 Excel 工作表中的某张图片](/zh/cells/pictures/delete/) – 删除指定索引的单张图片。  

**API 参考**

**获取特定格式的图片**

| HTTP 方法 | 端点 | 必需参数 | 示例请求 | 示例响应 | 状态码 |
|-----------|------|--------|----------|----------|--------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName`（路径）、`sheetName`（路径）、`pictureIndex`（路径）、`format`（查询参数） | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/0?format=png` | 二进制图像数据（PNG、JPEG 等） | 200 OK、400 请求错误、401 未授权、404 未找到、500 服务器错误 |

**获取所有图片信息**

| HTTP 方法 | 端点 | 必需参数 | 示例请求 | 示例响应 | 状态码 |
|-----------|------|--------|----------|----------|--------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName`（路径）、`sheetName`（路径） | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | 包含图片元数据（索引、名称、位置、尺寸）的 JSON 数组 | 200 OK、400、401、404、500 |

**添加图片**

| HTTP 方法 | 端点 | 必需参数 | 示例请求体 | 示例响应 | 状态码 |
|-----------|------|--------|-----------|----------|--------|
| POST | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName`（路径）、`sheetName`（路径） | `{ "image": "<base64编码的图像>", "upperLeftRow": 5, "upperLeftColumn": 2, "width": 200, "height": 150 }` | `{ "code": 200, "status": "OK", "pictureIndex": 3 }` | 201 已创建、400、401、404、500 |

**更新图片**

| HTTP 方法 | 端点 | 必需参数 | 示例请求体 | 示例响应 | 状态码 |
|-----------|------|--------|-----------|----------|--------|
| PUT | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName`（路径）、`sheetName`（路径）、`pictureIndex`（路径） | `{ "upperLeftRow": 10, "upperLeftColumn": 4, "width": 300, "height": 250 }` | `{ "code": 200, "status": "OK" }` | 200 OK、400、401、404、500 |

**删除所有图片**

| HTTP 方法 | 端点 | 必需参数 | 示例请求 | 示例响应 | 状态码 |
|-----------|------|--------|----------|----------|--------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName`（路径）、`sheetName`（路径） | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | `{ "code": 200, "status": "All pictures deleted." }` | 200 OK、400、401、404、500 |

**删除特定图片**

| HTTP 方法 | 端点 | 必需参数 | 示例请求 | 示例响应 | 状态码 |
|-----------|------|--------|----------|----------|--------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName`（路径）、`sheetName`（路径）、`pictureIndex`（路径） | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/2` | `{ "code": 200, "status": "Picture deleted." }` | 200 OK、400、401、404、500 |

**相关主题**

探索 Aspose.Cells Cloud 中其他与图像相关的操作：
- [处理形状](/zh/cells/shapes/) – 添加、编辑和删除绘图形状。  
- [处理图表](/zh/cells/charts/) – 创建和操作图表对象。  
- [在工作表中处理图像](/zh/cells/images/) – 嵌入和管理原始图像文件。

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "处理 Excel 图片 – Aspose.Cells Cloud 文档",
  "description": "通过 Aspose.Cells Cloud REST API 检索、添加、更新和删除 Excel 图片的指南。",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://cms.admin.containerize.com/templates/asposecloud/images/logo.png"
    }
  },
  "datePublished": "2026-07-30",
  "keywords": "Excel 图片, Aspose.Cells Cloud, REST API, 图像处理",
  "url": "https://docs.aspose.cloud/cells/pictures/"
}
</script>