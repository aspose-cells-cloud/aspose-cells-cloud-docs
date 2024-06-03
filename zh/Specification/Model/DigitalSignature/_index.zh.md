---
title: 数字签名
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/model/digitalsignature/
description: Aspose.Cells 云模型规范：数字签名。轻松处理 Excel 和其他电子表格文档，具有打开、生成、编辑、拆分、合并、比较和转换等功能
kwords: Excel, Office, 电子表格, Cloud REST API, 数字签名
weight: 50
---
## **电子签名**

文件中的签名。

|属性名称|财产种类|可空|只读|默认值|描述|
|:- |:- |:- |:- |:- |:- |
|评论|细绳|真的|错误的||签名的目的。|
|签到时间|细绳|真的|错误的||文件签署的时间。|
| ID|细绳|真的|错误的||指定一个 GUID，该 GUID 可以与文档内容中存储的签名行的 GUID 进行交叉引用。默认值为空（全零）Guid。|
|密码|细绳|真的|错误的||指定数字签名中实际签名的文本。默认值为空。|
|图像|大批<Byte> |真的|错误的||指定数字签名的图像。默认值为空。|
|提供者 ID|细绳|真的|错误的||指定签名提供程序的类 ID。默认值为空（全零）Guid。|
|已验证|布尔值|真的|错误的||如果此数字签名有效且文档未被篡改，则该值将为真。|
|类型|细绳|真的|错误的||XAdES 类型。默认值为 None（XAdES 关闭）。|

