﻿---
title: 使用 CellsObjectOperate 任务
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: Cells.Cloud API 为 Excel 操作：单元格对象操作任务
weight: 20
kwords: Excel, Office 云, REST API, 电子表格, PDF, CSV, Json, Markdwon, 使用 CellsObjectOperate 任务
---
此 REST API 操作单元格对象 `task`。

**操作对象**

|参数名称|类型|描述|
|:- |:- |:- |
|操作对象类型|细绳|工作簿/工作表/页面设置/Cells/图表/形状/列表对象/数据透视表/工作簿设置/分页符|
|操作对象位置|目的||

**操作对象位置**

|参数名称|类型|描述|
|:- |:- |:- |
|工作簿|目的||
|工作表名称|细绳||
|图表索引|整数||
|形状指数|整数||
|小区名称|细绳||
|列表对象索引|整数||


**图表操作参数**

|参数名称|类型|描述|
|:- |:- |:- |
|图表索引|整数||
|图表类型|细绳||
|左上行|整数||
|左上列|整数||
|右下行|整数||
|右下栏|整数||
|区域|细绳||
|垂直|细绳|真假|
|类别数据|细绳||
|是否自动获取串行名称|细绳|真假|
|区域|标题||

**列出对象操作参数** 

|参数名称|类型|描述|
|:- |:- |:- |
|列表对象|目的||

**分页操作参数**

|参数名称|类型|描述|
|:- |:- |:- |
|分页符类型|细绳||
|指数|指数||
|排|整数||
|柱子|整数||
|起始索引|整数||
|结束索引|整数||


**页面设置操作参数**

|参数名称|类型|描述|
|:- |:- |:- |
|页面设置|目的||


**数据透视表操作参数**

|参数名称|类型|描述|
|:- |:- |:- |
|目的单元名称|细绳||
|源数据|细绳||
|表名|细绳||
|使用相同来源|细绳|真假|
|数据透视表索引|整数||
|数据透视字段行|整数[]||
|数据透视字段列|整数[]||
|数据透视字段数据|整数[]||


**形状操作参数**


|参数名称|类型|描述|
|:- |:- |:- |
|形状|目的||


**工作簿设置操作参数**


|参数名称|类型|描述|
|:- |:- |:- |
|工作簿设置|目的||

**工作表操作参数**


|参数名称|类型|描述|
|:- |:- |:- |
|姓名|细绳||
|图纸类型|细绳||
|新名字|细绳||
|搬家请求|目的||

## 休息 API

|**API**|**类型**|**描述**|**资源链接**|
|:- |:- |:- |:- |
|/单元格/任务/运行任务|邮政|运行任务|[运行后任务](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

