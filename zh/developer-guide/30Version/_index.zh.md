---
title: "Aspose.Cells Cloud 3.0 开发者指南"
ArticleTitle: "Aspose.Cells Cloud 3.0 REST API 开发者指南 — Excel 工作簿创建、转换与样式设置"
second_title: "文档"
type: docs
url: /zh/developer-guide-3.0/
aliases: [  /zh/developer-guide/v3.0/ , /zh/developer-guide-v3.0/ ]
keywords: "Aspose.Cells Cloud, Excel REST API, 工作簿转换, 图表 API, 数据导入, 导出, PDF, CSV, JSON, 开发者指南"
description: "学习如何使用 Aspose.Cells Cloud 3.0 REST API 实现 Excel 工作簿的创建、转换、样式设置、图表、表格等功能。包含代码示例及最佳实践提示。"
weight: 150
---

## 使用 Aspose.Cells Cloud REST API

**Aspose.Cells Cloud 3.0 开发者指南** 提供了对最常用 Excel 工作簿与工作表 REST API 操作的简明、可搜索概览。本指南面向需要以编程方式创建、修改、转换及操作 Excel 文件的开发者。请通过下方章节快速定位所需操作；每个链接均指向详细页面，包含请求语法、参数说明及示例。本中心页面集中汇总了 **Aspose.Cells Cloud REST API** 参考文档，便于开发者快速查找与工作簿相关的端点、图表处理、数据导入与导出功能。

**前置条件：** 使用 API 前，请确保您已拥有有效的 Aspose Cloud 账户、API 密钥与密钥（secret），并为您的开发环境安装了相应的 SDK。

### 目录
- [文件操作](#文件操作)
- [主页（单元格格式化与行/列管理）](#主页单元格格式化与行列管理)
- [插入（图表、表格与 OLE 对象）](#插入图表表格与-ole-对象)
- [页面布局（分页符与页面设置）](#页面布局分页符与页面设置)
- [公式（计算与名称管理）](#公式计算与名称管理)
- [数据（分级显示、筛选与导入）](#数据分级显示筛选与导入)
- [审阅（批注与保护）](#审阅批注与保护)
- [视图（窗口冻结与缩放控制）](#视图窗口冻结与缩放控制)

### 快速 API 摘要

| API 分组 | 示例端点 | 主要操作 |
|---------|---------|---------|
| **创建工作簿** | `POST /cells/workbook` | 创建一个空的 Excel 工作簿 |
| **转换工作簿** | `PUT /cells/workbook/convert` | 将 Excel 文件转换为 PDF、CSV、JSON 等格式 |
| **添加图表** | `POST /cells/worksheets/{sheetName}/charts` | 向工作表中插入新图表 |
| **管理表格** | `PUT /cells/worksheets/{sheetName}/tables/{tableName}` | 更新或删除列表对象（表格） |
| **导入数据** | `POST /cells/worksheets/{sheetName}/import` | 将 CSV、JSON、图片或数组导入工作表 |
| **计算公式** | `POST /cells/workbook/calculate` | 重新计算工作簿中的所有公式 |
| **应用筛选** | `POST /cells/worksheets/{sheetName}/filters` | 添加或移除自动筛选条件 |
| **保护工作簿** | `POST /cells/workbook/protect` | 对工作簿应用密码保护 |

上述高频操作涵盖了 **Aspose.Cells Cloud Excel REST API** 的核心功能，链接均指向详细文档页面。

您可下载本快速 API 摘要表的 PDF 版本，便于离线查阅。

{{< tabs tabTotal="8" tabID="1" tabName1="文件" tabName2="主页" tabName3="插入" tabName4="页面布局" tabName5="公式" tabName6="数据" tabName7="审阅" tabName8="视图" >}}
{{< tab tabNum="1" >}}
<div class="row">
    <div class="col-md-6">
        <p>工作簿：新建、转换、另存为</p>
        <ul>
            <li><a href="/zh/cells/create-an-empty-excel-workbook/" title="通过 API 创建空的 Excel 工作簿" rel="noopener">创建空的 Excel 工作簿。</a></li>
            <li><a href="/zh/cells/create-excel-workbook-from-a-template-file/" title="从模板文件创建工作簿" rel="noopener">从模板文件创建 Excel 工作簿。</a></li>
            <li><a href="/zh/cells/create-excel-workbook-from-a-smartmarker-template/" title="从 SmartMarker 模板创建工作簿" rel="noopener">从 SmartMarker 模板创建 Excel 工作簿。</a></li>
            <li><a href="/zh/cells/convert/" title="将 Excel 工作簿转换为其他格式" rel="noopener">将 Excel 工作簿转换为不同文件格式。</a></li>
            <li><a href="/zh/cells/saveas-other-formats/" title="将 Excel 工作簿另存为其他格式" rel="noopener">将 Excel 工作簿保存为不同文件格式。</a></li>
        </ul>
        <p>查找与替换</p>
        <ul>
            <li><a href="/zh/cells/search/" title="在 Excel 文件中搜索文本" rel="noopener">从 Excel 文件中搜索文本。</a></li>
            <li><a href="/zh/cells/replace/" title="替换 Excel 文件中的值" rel="noopener">在 Excel 文件中将旧值替换为新值。</a></li>
        </ul>
        <p>压缩</p>
        <ul>
            <li><a href="/zh/cells/compress/" title="压缩 Excel 文件" rel="noopener">压缩 Excel 文件。</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>工作簿：合并、拆分</p>
        <ul>
            <li><a href="/zh/cells/merge/" title="合并多个 Excel 工作簿" rel="noopener">合并 Excel 工作簿。</a></li>
            <li><a href="/zh/cells/split/" title="将 Excel 工作簿拆分为独立文件" rel="noopener">拆分 Excel 工作簿。</a></li>
        </ul>
        <p>水印</p>
        <ul>
            <li><a href="/zh/cells/add-background-in-workbook/" title="为工作簿添加背景图" rel="noopener">为工作簿添加背景图。</a></li>
            <li><a href="/zh/cells/delete-background-in-workbook/" title="删除工作簿背景图" rel="noopener">从工作簿中删除背景图。</a></li>
            <li><a href="/zh/cells/set-background-or-watermark-for-excel-worksheet/" title="为工作表设置背景或水印" rel="noopener">为 Excel 工作表设置背景或水印。</a></li>
            <li><a href="/zh/cells/delete-background-or-watermark-of-excel-worksheet/" title="删除工作表背景或水印" rel="noopener">从 Excel 工作表中删除背景或水印。</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="2" >}}
<div class="row">
    <div class="col-md-6">
        <p>单元格字体、样式、条件格式及值</p>
        <ul>
            <li><a href="/zh/cells/get-cell-style-from-a-worksheet/" title="获取工作表中的单元格样式" rel="noopener">获取 Excel 工作表中的单元格样式。</a></li>
            <li><a href="/zh/cells/update-multiple-cells-style/" title="更新多个单元格的样式" rel="noopener">更新 Excel 工作表中多个单元格的样式。</a></li>
            <li><a href="/zh/cells/change-cell-style-in-excel-worksheet/" title="更改单个单元格的样式" rel="noopener">更新 Excel 工作表中的单元格样式。</a></li>
            <li><a href="/zh/cells/apply-rich-text-formatting-to-a-cell/" title="为单元格应用富文本格式" rel="noopener">设置 Excel 工作表中单元格的富文本格式。</a></li>
            <li><a href="/zh/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/" title="清除单元格内容与样式" rel="noopener">清除 Excel 工作表中单元格的内容与样式。</a></li>
            <li><a href="/zh/cells/working-with-conditional-formatting/" title="管理条件格式规则" rel="noopener">在 Excel 工作表中添加、删除及更新条件格式。</a></li>
            <li><a href="/zh/cells/set-value-of-a-cell-in-a-worksheet/" title="设置单元格的值" rel="noopener">设置 Excel 工作表中单元格的值。</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>行/列：插入、删除、复制、隐藏与自动调整列宽</p>
        <ul>
            <li><a href="/zh/cells/add-an-empty-row-in-a-worksheet/" title="向工作表中插入空行" rel="noopener">在 Excel 工作表中添加空行。</a></li>
            <li><a href="/zh/cells/delete-row-from-a-worksheet/" title="从工作表中删除行" rel="noopener">从 Excel 工作表中删除行。</a></li>
            <li><a href="/zh/cells/copy-rows-in-excel-worksheet/" title="在工作表内复制行" rel="noopener">在 Excel 工作表中复制行。</a></li>
            <li><a href="/zh/cells/hide-rows-in-excel-worksheet/" title="隐藏工作表中的行" rel="noopener">在 Excel 工作表中隐藏行。</a></li>
            <li><a href="/zh/cells/auto-fit-rows-in-excel-workbooks/" title="在工作簿中自动调整行高" rel="noopener">在 Excel 工作簿中自动调整行高。</a></li>
            <li><a href="/zh/cells/columns/add/" title="向工作表中插入空列" rel="noopener">在 Excel 工作表中添加空列。</a></li>
            <li><a href="/zh/cells/columns/delete/" title="从工作表中删除列" rel="noopener">从 Excel 工作表中删除列。</a></li>
            <li><a href="/zh/cells/columns/copy/" title="在工作表内复制列" rel="noopener">在 Excel 工作表中复制列。</a></li>
            <li><a href="/zh/cells/columns/hide/" title="隐藏工作表中的列" rel="noopener">在 Excel 工作表中隐藏列。</a></li>
            <li><a href="/zh/cells/columns/autofit/" title="在工作簿中自动调整列宽" rel="noopener">在 Excel 工作簿中自动调整列宽。</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="3" >}}
<div class="row">
    <div class="col-md-6">
        <p>图表</p>
        <ul>
            <li><a href="/zh/cells/add-a-chart-in-a-worksheet/" title="向工作表添加图表" rel="noopener">在 Excel 工作表中添加图表。</a></li>
            <li><a href="/zh/cells/delete-a-chart-from-a-worksheet/" title="从工作表删除图表" rel="noopener">在 Excel 工作表中删除图表。</a></li>
            <li><a href="/zh/cells/delete-all-charts-from-a-worksheet/" title="从工作表删除所有图表" rel="noopener">在 Excel 工作表中删除所有图表。</a></li>
            <li><a href="/zh/cells/convert-chart-to-image/" title="将图表转换为图片文件" rel="noopener">将图表转换为图片。</a></li>
            <li><a href="/zh/cells/hide-chart-legend-in-a-worksheet/" title="隐藏图表图例" rel="noopener">在 Excel 工作表中隐藏图表图例。</a></li>
            <li><a href="/zh/cells/update-chart-title-in-excel-worksheet/" title="更新图表标题" rel="noopener">在 Excel 工作表中更新图表标题。</a></li>
            <li><a href="/zh/cells/delete-chart-title-in-a-worksheet/" title="删除图表标题" rel="noopener">在工作表中删除图表标题。</a></li>
        </ul>
        <p>表格</p>
        <ul>
            <li><a href="/zh/cells/add-a-list-object-or-table-inside-the-worksheet/" title="向工作表添加表格（列表对象）" rel="noopener">在 Excel 工作表中添加列表对象。</a></li>
            <li><a href="/zh/cells/update-a-list-object-or-table-inside-the-worksheet/" title="更新工作表中的表格" rel="noopener">更新 Excel 工作表中的列表对象。</a></li>
            <li><a href="/zh/cells/convert-list-object-or-table-to-range/" title="将表格转换为区域" rel="noopener">将列表对象转换为区域。</a></li>
            <li><a href="/zh/cells/sort-table-data/" title="对表格数据排序" rel="noopener">对表格数据排序。</a></li>
        </ul>
        <p>OLE 对象</p>
        <ul>
            <li><a href="/zh/cells/add-oleobject-to-excel-worksheet/" title="向工作表添加 OLE 对象" rel="noopener">在 Excel 工作表中添加 OLE 对象。</a></li>
            <li><a href="/zh/cells/update-a-specific-oleobject-from-excel-worksheet/" title="更新特定 OLE 对象" rel="noopener">更新 Excel 工作表中的特定 OLE 对象。</a></li>
            <li><a href="/zh/cells/convert-oleobject-to-image/" title="将 OLE 对象转换为图片" rel="noopener">将 OLE 对象转换为图片。</a></li>
            <li><a href="/zh/cells/delete-all-oleobjects-from-excel-worksheet/" title="从工作表删除所有 OLE 对象" rel="noopener">在 Excel 工作表中删除所有 OLE 对象。</a></li>
            <li><a href="/zh/cells/delete-a-specific-oleobject-from-excel-worksheet/" title="删除特定 OLE 对象" rel="noopener">在 Excel 工作表中删除特定 OLE 对象。</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>形状</p>
        <ul>
            <li><a href="/zh/cells/add-a-shape-inside-the-worksheet/" title="向工作表添加形状" rel="noopener">在 Excel 工作表中添加形状。</a></li>
            <li><a href="/zh/cells/delete-all-shapes-inside-the-worksheet/" title="从工作表删除所有形状" rel="noopener">在 Excel 工作表中删除所有形状。</a></li>
            <li><a href="/zh/cells/delete-a-shape-by-index-inside-the-worksheet/" title="按索引删除形状" rel="noopener">在 Excel 工作表中按索引删除形状。</a></li>
        </ul>
        <p>数据透视表</p>
        <ul>
            <li><a href="/zh/cells/add-a-pivot-table-in-a-worksheet/" title="向工作表添加数据透视表" rel="noopener">在 Excel 工作表中添加数据透视表。</a></li>
            <li><a href="/zh/cells/delete-worksheet-pivot-tables/" title="从工作表删除所有数据透视表" rel="noopener">在 Excel 工作表中删除所有数据透视表。</a></li>
            <li><a href="/zh/cells/delete-worksheet-pivot-table-by-index/" title="按索引删除数据透视表" rel="noopener">在 Excel 工作表中按索引删除数据透视表。</a></li>
            <li><a href="/zh/cells/update-cell-style-for-pivot-table/" title="更新数据透视表中的单元格样式" rel="noopener">更新 Excel 工作表中数据透视表的单元格样式。</a></li>
            <li><a href="/zh/cells/update-style-for-pivot-table/" title="更新数据透视表的整体样式" rel="noopener">更新 Excel 工作表中数据透视表的样式。</a></li>
            <li><a href="/zh/cells/working-with-pivot-filters/" title="使用数据透视表筛选器" rel="noopener">在 Excel 工作表中使用数据透视筛选器。</a></li>
            <li><a href="/zh/cells/hide-pivot-field-item/" title="隐藏数据透视字段项" rel="noopener">在 Excel 工作表中隐藏数据透视字段项。</a></li>
            <li><a href="/zh/cells/move-pivot-table/" title="在工作表内移动数据透视表" rel="noopener">在 Excel 工作表中移动数据透视表。</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="4" >}}
<div class="row">
    <div class="col-md-6">
        <p>分页符</p>
        <ul>
            <li><a href="/zh/cells/insert-horizontal-page-break-inside-worksheet/" title="插入水平分页符" rel="noopener">在 Excel 工作表中插入水平分页符。</a></li>
            <li><a href="/zh/cells/insert-vertical-page-break-inside-worksheet/" title="插入垂直分页符" rel="noopener">在 Excel 工作表中插入垂直分页符。</a></li>
            <li><a href="/zh/cells/delete-horizontal-page-break-inside-worksheet/" title="删除水平分页符" rel="noopener">在 Excel 工作表中删除水平分页符。</a></li>
            <li><a href="/zh/cells/delete-vertical-page-break-inside-worksheet/" title="删除垂直分页符" rel="noopener">在 Excel 工作表中删除垂直分页符。</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>页面设置</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="5" >}}
<div class="row">
    <div class="col-md-6">
        <p>计算</p>
        <ul>
            <li><a href="/zh/cells/calculate-all-formulas-in-a-workbook/" title="计算工作簿中所有公式" rel="noopener">计算 Excel 工作簿中所有公式。</a></li>
            <li><a href="/zh/cells/calculate-cells-formula/" title="计算特定单元格的公式" rel="noopener">计算 Excel 工作簿中单元格的公式。</a></li>
            <li><a href="/zh/cells/calculate-formula-in-a-worksheet/" title="计算工作表中的公式" rel="noopener">计算 Excel 工作表中的公式。</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>名称</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="6" >}}
<div class="row">
    <div class="col-md-6">
        <p>分级显示</p>
        <ul>
            <li><a href="/zh/cells/group-rows-in-excel-worksheet/" title="在工作表中对行进行分组" rel="noopener">在 Excel 工作表中对行进行分组。</a></li>
            <li><a href="/zh/cells/ungroup-rows-in-excel-worksheet/" title="在工作表中取消行分组" rel="noopener">在 Excel 工作表中取消行分组。</a></li>
        </ul>
        <p>筛选</p>
        <ul>
            <li><a href="/zh/cells/add-a-filter-for-a-filter-column/" title="为列添加筛选器" rel="noopener">在 Excel 工作表中为列添加筛选器。</a></li>
            <li><a href="/zh/cells/delete-a-filter-for-a-filter-column/" title="删除列筛选器" rel="noopener">在 Excel 工作表中删除列筛选器。</a></li>
            <li><a href="/zh/cells/remove-a-date-filter/" title="移除日期筛选器" rel="noopener">在 Excel 工作表中移除日期筛选器。</a></li>
            <li><a href="/zh/cells/add-an-icon-filter/" title="添加图标筛选器" rel="noopener">在 Excel 工作表中添加图标筛选器。</a></li>
            <li><a href="/zh/cells/add-date-filter-in-a-worksheet/" title="添加日期筛选器" rel="noopener">在 Excel 工作表中添加日期筛选器。</a></li>
            <li><a href="/zh/cells/filter-data-by-using-an-autofilter/" title="使用自动筛选筛选数据" rel="noopener">在 Excel 工作表中使用自动筛选筛选数据。</a></li>
            <li><a href="/zh/cells/filter-the-top-10-items-in-the-list/" title="筛选列表中前 10 项" rel="noopener">在 Excel 工作表中筛选列表中前 10 项。</a></li>
            <li><a href="/zh/cells/match-all-blank-cells-in-the-list/" title="匹配所有空白单元格" rel="noopener">在 Excel 工作表中匹配列表中所有空白单元格。</a></li>
        </ul>
        <p>排序</p>
        <ul>
            <li><a href="/zh/cells/sort-worksheet-data/" title="对工作表数据排序" rel="noopener">在 Excel 工作表中对数据排序。</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>导入数据</p>
        <ul>
            <li><a href="/zh/cells/import/" title="将数据导入 Excel 文件" rel="noopener">将数据导入 Excel 文件。</a></li>
            <li><a href="/zh/cells/import-CSV-data-into-worksheet/" title="将 CSV 数据导入工作表" rel="noopener">将 CSV 数据导入 Excel 工作表。</a></li>
            <li><a href="/zh/cells/import/picture/" title="将图片导入工作表" rel="noopener">将图片导入 Excel 工作表。</a></li>
            <li><a href="/zh/cells/import/double-array/" title="将双精度数组导入工作表" rel="noopener">将双精度数组导入 Excel 工作表。</a></li>
            <li><a href="/zh/cells/import/integer-array/" title="将整型数组导入工作表" rel="noopener">将整型数组导入 Excel 工作表。</a></li>
            <li><a href="/zh/cells/import/string-array/" title="将字符串数组导入工作表" rel="noopener">将字符串数组导入 Excel 工作表。</a></li>
            <li><a href="/zh/cells/import/with-using-storage/" title="使用存储导入数据" rel="noopener">使用存储将数据导入 Excel 工作表。</a></li>
            <li><a href="/zh/cells/import/without-using-storage/" title="不使用存储导入数据" rel="noopener">不使用存储将数据导入 Excel 工作表。</a></li>
        </ul>
        <p>组装数据</p>
        <ul>
            <li><a href="/zh/cells/assembly/" title="在 Excel 文件中组装数据" rel="noopener">在 Excel 文件中组装数据。</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="7" >}}
<div class="row">
    <div class="col-md-6">
        <p>批注</p>
        <ul>
            <li><a href="/zh/cells/add-a-comment-to-a-cell-in-a-worksheet/" title="向单元格添加批注" rel="noopener">在 Excel 工作表中的单元格添加批注。</a></li>
            <li><a href="/zh/cells/update-a-comment-in-excel-workbook/" title="更新单元格批注" rel="noopener">更新 Excel 工作表中的批注。</a></li>
            <li><a href="/zh/cells/delete-all-comments-in-a-worksheet/" title="删除工作表中所有批注" rel="noopener">删除 Excel 工作表中所有批注。</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>变更</p>
        <ul>
            <li><a href="/zh/cells/protect-excel-workbooks/" title="保护 Excel 工作簿" rel="noopener">保护 Excel 工作簿。</a></li>
            <li><a href="/zh/cells/unprotect-excel-workbooks/" title="取消保护 Excel 工作簿" rel="noopener">取消保护 Excel 工作簿。</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="8" >}}
<div class="row">
    <div class="col-md-6">
        <p>窗口</p>
        <ul>
            <li><a href="/zh/cells/freeze-panes-in-excel-worksheet/" title="冻结工作表窗格" rel="noopener">在 Excel 工作表中冻结窗格。</a></li>
            <li><a href="/zh/cells/unfreeze-panes-in-excel-worksheet/" title="解冻工作表窗格" rel="noopener">在 Excel 工作表中解冻窗格。</a></li>
            <li><a href="/zh/cells/hide-excel-worksheets/" title="隐藏工作表" rel="noopener">隐藏 Excel 工作表。</a></li>
            <li><a href="/zh/cells/unhide-excel-worksheets/" title="取消隐藏工作表" rel="noopener">取消隐藏 Excel 工作表。</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>缩放</p>
        <ul>
            <li><a href="/zh/cells/set-zoom-in-excel-worksheet/" title="设置工作表缩放比例" rel="noopener">设置 Excel 工作表的缩放比例。</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}

{{< /tabs >}}