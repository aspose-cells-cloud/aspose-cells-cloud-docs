---
title: CellsObjectOperate Tas ile Çalışmak
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API, Excel için çalışır: hücreler nesnesi çalıştırma görevi"
weight: 20
kwords: Excel, Office Cloud, REST API, Elektronik Tablo, PDF, CSV, Json, Markdwon, CellsObjectOperate Göreviyle Çalışma
---
Bu REST API, hücre nesnesi `task`'i çalıştırır.

**OperateObject**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| OperateObjectType| sicim| Çalışma Kitabı/Çalışma Sayfası/PageSetup/Cells/Grafik/Şekil/ListObject/PivotTable/WorkbookSettings/PageBreak|
| OperateObjectPosition| Nesne||

**OperateObjectPosition**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| Çalışma kitabı| Nesne||
| SayfaAdı| sicim||
| GrafikIndex| tamsayı||
| ŞekilIndex| tamsayı||
| HücreAdı| sicim||
| ListObjectIndex| tamsayı||


**ChartOperateParameter**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| GrafikIndex| tamsayı||
|Grafik tipi| sicim||
| ÜstSolSatır| tamsayı||
| ÜstSol Sütun| tamsayı||
| AltSağSatır| tamsayı||
| Alt Sağ Sütun| tamsayı||
| Alan| sicim||
| Dikey| sicim| doğru yanlış|
| KategoriVeri| sicim||
| IsAutoGetSerialName| sicim| doğru yanlış|
| Alan| Başlık||

**ListObjectOperateParameter** 

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| ListeObject| Nesne||

**PageBreakOperateParametre**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| Sayfa Sonu Türü| sicim||
| Dizin| Dizin||
| Sıra| tamsayı||
| Kolon| tamsayı||
| Dizini başlat| tamsayı||
| EndIndex| tamsayı||


**PageSetupOperateParameter**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| Sayfa ayarı| Nesne||


**PivotTableOperateParametresi**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| DestHücreAdı| sicim||
| KaynakVerileri| sicim||
| Tablo ismi| sicim||
| Aynı Kaynağı Kullan| sicim| doğru yanlış|
| PivotTableIndex| tamsayı||
| PivotFieldSatırlar|tamsayı[]||
| PivotFieldSütunlar|tamsayı[]||
| PivotFieldData|tamsayı[]||


**ShapeOperateParametre**


|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| Şekil| Nesne||


**Çalışma KitabıAyarlarıOperateParametresi**


|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| Çalışma KitabıAyarları| Nesne||

**Çalışma SayfasıOperateParametre**


|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| İsim| sicim||
| Sayfa Türü| sicim||
| Yeni isim| sicim||
| Taşıma Talebi| Nesne||

## DİNLENME API

|**API**|**Tip**|**Tanım**|**Kaynak Bağlantısı**|
|:- |:- |:- |:- |
|/hücreler/görev/çalıştırma görevi|POSTALAMAK|Görevi Çalıştır|[Çalıştırma SonrasıGörev](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

