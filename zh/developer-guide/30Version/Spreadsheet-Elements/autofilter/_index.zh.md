---
title: "使用 Excel 自动筛选"
second_title: "文档"
linktitle: "自动筛选"
type: docs
url: /autofilter/
aliases: [/working-with-autofilter/]
keywords: "自动筛选, Aspose.Cells Cloud, Excel 筛选, 颜色筛选, 日期筛选, 动态筛选, 数值筛选, 文本筛选, 空白筛选, 自定义筛选"
description: "了解如何使用 Aspose.Cells Cloud API 添加、编辑和删除 Excel 自动筛选（颜色、日期、动态、数值、文本、空白）。提供多种语言的代码示例。"
weight: 100
ArticleTitle: "使用 Excel 自动筛选 – Aspose.Cells Cloud 文档"
---

自动筛选是仅显示工作表中所需项目的最快方式。自动筛选功能允许用户根据指定条件（如文本、数值或日期）对列表进行筛选。

**不同类型的筛选器**

Aspose.Cells Cloud 提供多种 API，用于应用各种筛选类型，例如颜色筛选、日期筛选、数值筛选、文本筛选、空白筛选和非空白筛选。

<table class="table table-striped">
  <tr>
    <td class="col-md-2"><strong>填充颜色</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud 提供了 <a href="/cells/autofilter/add-color-filter/">添加填充颜色筛选 API</a>，用于根据单元格的填充颜色属性筛选数据。</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>日期</strong></td>
    <td class="col-md-10">
      <p>可应用多种日期筛选，例如筛选出 2018 年 1 月的日期行。使用 <a href="/cells/autofilter/add-date-filter/">添加日期筛选 API</a> 添加日期筛选。</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>动态日期</strong></td>
    <td class="col-md-10">
      <p>动态日期筛选允许您筛选出特定月份（不考虑年份）的单元格（例如所有 1 月的日期）。参见 <a href="/cells/autofilter/add-dynamic-filter/">动态筛选 API</a>。</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>数值</strong></td>
    <td class="col-md-10">
      <p><a href="/cells/autofilter/add-filter/">自定义筛选 API</a> 允许筛选数值范围内的单元格。</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>文本</strong></td>
    <td class="col-md-10">
      <p>如果某列包含文本，可使用 <a href="/cells/autofilter/add-filter/">添加筛选 API</a> 选择包含特定字符串的单元格。</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>空白</strong></td>
    <td class="col-md-10">
      <p>要检索某列为空白的行，请使用 <a href="/cells/autofilter/match-all-blank/">匹配所有空白单元格 API</a>。</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>非空白</strong></td>
    <td class="col-md-10">
      <p>要筛选某列包含任意非空白值的行，请使用 <a href="/cells/autofilter/match-all-non-blank/">匹配所有非空白单元格 API</a>。</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>自定义筛选</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud 提供了 <a href="/cells/autofilter/add-custom-filter/">自定义筛选 API</a>，用于高级场景，例如筛选包含特定子字符串或以特定字符串开头/结尾的行。</p>
    </td>
  </tr>
</table>

**自动筛选操作**

- [如何在 Excel 工作表中添加颜色筛选](/cells/autofilter/add-color-filter/) – **方法：** POST，**端点：** `/cells/autofilter/add-color-filter/`
- [如何在 Excel 工作表中添加自定义筛选](/cells/autofilter/add-custom-filter/) – **方法：** POST，**端点：** `/cells/autofilter/add-custom-filter/`
- [如何在 Excel 工作表中添加日期筛选](/cells/autofilter/add-date-filter/) – **方法：** POST，**端点：** `/cells/autofilter/add-date-filter/`
- [如何在 Excel 工作表中添加动态筛选](/cells/autofilter/add-dynamic-filter/) – **方法：** POST，**端点：** `/cells/autofilter/add-dynamic-filter/`
- [如何在 Excel 工作表中添加筛选](/cells/autofilter/add-filter/) – **方法：** POST，**端点：** `/cells/autofilter/add-filter/`
- [如何在 Excel 工作表中添加图标筛选](/cells/autofilter/add-icon-filter/) – **方法：** POST，**端点：** `/cells/autofilter/add-icon-filter/`
- [如何在 Excel 工作表中删除日期筛选](/cells/autofilter/delete-a-date-filter/) – **方法：** DELETE，**端点：** `/cells/autofilter/delete-a-date-filter/`
- [如何在 Excel 工作表中删除筛选](/cells/delete-filter/) – **方法：** DELETE，**端点：** `/cells/delete-filter/`
- [如何获取 Excel 工作表中的自动筛选描述](/cells/autofilter/get/) – **方法：** GET，**端点：** `/cells/autofilter/get/`
- [如何在 Excel 工作表中匹配所有空白单元格](/cells/autofilter/match-all-blank/) – **方法：** POST，**端点：** `/cells/autofilter/match-all-blank/`
- [如何在 Excel 工作表中匹配所有非空白单元格](/cells/autofilter/match-all-non-blank/) – **方法：** POST，**端点：** `/cells/autofilter/match-all-non-blank/`
- [如何刷新 Excel 工作表中的自动筛选](/cells/autofilter/refresh/) – **方法：** POST，**端点：** `/cells/autofilter/refresh/`
---