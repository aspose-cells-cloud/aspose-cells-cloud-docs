---
title: CellsObjectOperate Tas ile Çalışma
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API için Excel çalıştır: hücreler nesnesi çalıştırma görevi"
weight: 20
---
Bu REST API, `task` numaralı hücre nesnesini çalıştırır.

**Nesneyi Çalıştır**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| OperateObjectType| sicim| Çalışma Kitabı/Çalışma Sayfası/PageSetup/Cells/Chart/Shape/ListObject/PivotTable/WorkbookSettings/PageBreak|
| Nesne Konumunu Çalıştır| Nesne||

**Nesne Konumunu Çalıştır**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| Çalışma kitabı| Nesne||
| SayfaAdı| sicim||
| ChartIndex| tamsayı||
| şekil indeksi| tamsayı||
| HücreAdı| sicim||
| ListObjectIndex| tamsayı||


**GrafikİşletParametresi**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| ChartIndex| tamsayı||
| Grafik tipi| sicim||
| ÜstSolSatır| tamsayı||
|Sol Üst Sütun| tamsayı||
| AltSağSatır| tamsayı||
| AltSağSütun| tamsayı||
| Alan| sicim||
| Dikey mi| sicim| doğru yanlış|
| KategoriVerileri| sicim||
| IsAutoGetSeriAdı| sicim| doğru yanlış|
| Alan| Başlık||

**ListObjectOperateParameter** 

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| Nesne Listesi| Nesne||

**SayfaBreakİşletParametresi**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| SayfaBreakTürü| sicim||
| dizin| dizin||
| Sıra| tamsayı||
| Kolon| tamsayı||
| Dizini başlat| tamsayı||
| EndIndex| tamsayı||


**SayfaKurulumİşletParametresi**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| Sayfa ayarı| Nesne||


**PivotTableİşletParametresi**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| Hedef HücreAdı| sicim||
| KaynakVeri| sicim||
| Tablo ismi| sicim||
| UseSameSource| sicim| doğru yanlış|
| Özet Tablo Dizini| tamsayı||
| PivotAlanSatırları|tamsayı[]||
| Özet Alan Sütunları|tamsayı[]||
|PivotAlanVerileri|tamsayı[]||


**ShapeOperateParameter**


|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| Şekil| Nesne||


**WorkbookSettingsOperateParameter**


|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| Çalışma Kitabı Ayarları| Nesne||

**Çalışma SayfasıİşletParametresi**


|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| İsim| sicim||
| Sayfa Türü| sicim||
| Yeni isim| sicim||
| Taşınma Talebi| Nesne||

## DİNLENME API

|**API**|**Tip**|**Tanım**|**Kaynak Bağlantısı**|
|:- |:- |:- |:- |
|/hücreler/görev/görev çalıştırma|POSTALAMAK|Görevi Çalıştır|[Çalıştırma Görevi Sonrası](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

