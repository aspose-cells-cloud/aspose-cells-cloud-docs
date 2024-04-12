---
title: OoXML保存选项
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/model/ooxmlsaveoptions/
description: Aspose.Cells 云模型规范：OoxmlSaveOptions。轻松处理 Excel 和其他电子表格文档，具有打开、生成、编辑、拆分、合并、比较和转换等功能
weight: 50
---
## **ooxml保存选项**

代表保存 ooxml 文件的选项。

|物业名称|财产种类|可空|只读|默认值|描述|
|:- |:- |:- |:- |:- |:- |
|导出单元格名称|布尔值|真的|错误的||指示是否将单元格名称导出到Excel2007 .xlsx（.xlsm、.xltx、.xltm）文件。如果输出文件可由 SQL Server DTS 访问，则该值必须为 true。将值设置为 false 将极大地提高性能并在创建大文件时减小文件大小。默认值为 false。|
|更新缩放|布尔值|真的|错误的||指示如果 PageSetup.FitToPagesWide 和 PageSetup.FitToPagesTall 属性控制工作表的缩放方式，是否在保存文件之前更新缩放系数。|
|启用Zip64|布尔值|真的|错误的||编写 zip 存档时始终使用 ZIP64 扩展名，即使不必要时也是如此。|
|嵌入OoxmlAsOleObject|布尔值|真的|错误的||指示是否将OleObject的Ooxml文件嵌入为ole对象。|
|压缩类型|细绳|真的|错误的||获取和设置 ooxml 文件的压缩类型。|
|保存格式|细绳|真的|错误的|||
|缓存文件文件夹|细绳|真的|错误的|||
|清除数据|布尔值|真的|错误的|||
|创建目录|布尔值|真的|错误的|||
|启用HTTP压缩|布尔值|真的|错误的|||
|刷新图表缓存|布尔值|真的|错误的|||
|排序名称|布尔值|真的|错误的|||
|验证合并区域|布尔值|真的|错误的|||

**父母名字** (保存选项)[保存选项]