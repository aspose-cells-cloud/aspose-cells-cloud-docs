---
title: "处理 Excel 元数据与属性"
second_title: "文档"
linktitle: "元数据与属性"
type: docs
url: /zh/metadata/
aliases:
  - /zh/document-properties/
  - /zh/working-with-document-properties/
keywords: "Aspose.Cells Cloud, Excel 元数据, 文档属性 API, REST API, 获取元数据, 更新 Excel 属性, 删除 Excel 元数据"
description: "了解如何使用 Aspose.Cells Cloud REST API 读取、添加、更新和删除 Excel 文件的元数据。包含 cURL 及多种 SDK（Java、.NET、Python、Node.js 等）的示例。"
ArticleTitle: "处理 Excel 元数据与文档属性 – Aspose.Cells Cloud"
weight: 100
---

Excel 文件可存储多种元数据，有助于识别、组织和管理文档。Aspose.Cells Cloud 提供了简洁的 REST API，用于读取、添加、更新和删除这些元数据，使开发者能够将文档属性管理功能集成到其应用程序中。本指南涵盖标准属性与自定义属性这两类主要属性类型，说明如何操作它们，并提供指向相关 API 端点的直接链接。您还将找到一份简洁的 API 参考表，其中包含请求详情，便于快速实现。

**最后更新时间：** 2026 年 7 月 8 日  

**文档属性类型**

在了解如何使用 Aspose.Cells Cloud API 查看、修改和删除 Excel 文档的属性（元数据）之前，我们先明确 Excel 文档可包含的属性类型。

- **标准属性**：为 Excel 所共有，包含如标题（Title）、主题（Subject）、作者（Author）、类别（Category）等基本信息。您可为这些属性分配自定义文本值，以便更便捷地定位文件。

- **自定义属性**：由用户自行定义，允许您为 Excel 文档添加额外的元数据。

**如何操作 Excel 文件的文档属性**

- [如何通过存储服务获取特定文档属性](/zh/cells/document-properties/get/)
- [如何在不使用存储服务的情况下获取文档属性](/zh/cells/metadata/get/)
- [如何通过存储服务获取所有文档属性](/zh/cells/document-properties/get-all/)
- [如何通过存储服务更新特定文档属性](/zh/cells/document-properties/update/)
- [如何在不使用存储服务的情况下更新特定文档属性](/zh/cells/metadata/update/)
- [如何通过存储服务删除特定文档属性](/zh/cells/document-properties/delete/)
- [如何在不使用存储服务的情况下删除文档属性](/zh/cells/metadata/delete/)
- [如何通过存储服务清除所有文档属性](/zh/cells/document-properties/clear/)

**API 参考（不使用存储服务）**

| 方法 | 端点 | 描述 |
|------|------|------|
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata` | 获取存储于云端的工作簿的所有文档属性。 |
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | 获取由 `propertyName` 标识的特定属性（标准或自定义）的值。 |
| **PUT** | `PUT https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | 更新现有属性的值。请求体以 JSON 格式包含新值。 |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | 从工作簿中删除特定属性。 |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata` | 清除工作簿中的所有自定义与标准属性。 |

*所有请求均需提供 OAuth 2.0 访问令牌；若使用特定存储位置，还可包含 `storage` 和 `folder` 等可选查询参数。*
---