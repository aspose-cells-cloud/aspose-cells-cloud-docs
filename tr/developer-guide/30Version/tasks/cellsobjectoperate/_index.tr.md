---
title: CellsObjectOperate Tas ile Çalışma
second_title: Documen
type: docs
url: /tr/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API Excel için çalıştır: hücreler nesnesi çalıştır görevi"
weight: 20
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, CellsObjectOperate Göreviyle Çalışma
---
Bu REST API hücre nesnesi `task`'i çalıştırır.

**İşletNesnesi**

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
| OperateObjectType| sicim|Çalışma Kitabı/Çalışma Sayfası/Sayfa Kurulumu/Cells/Grafik/Şekil/ListeNesnesi/PivotTable/Çalışma Kitabı Ayarları/Sayfa Sonu|
| NesneKonumunuİşlet| Nesne||

**NesneKonumunuİşlet**

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
| Çalışma kitabı| Nesne||
| SayfaAdı| sicim||
| Grafik Endeksi| tam sayı||
| Şekil Endeksi| tam sayı||
| HücreAdı| sicim||
| ListObjectIndex| tam sayı||


**ChartOperateParameter**

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
| Grafik Endeksi| tam sayı||
| Grafik Türü| sicim||
| Sol Üst Satır| tam sayı||
| Sol Üst Sütun| tam sayı||
| AltSağSatır| tam sayı||
| AltSağSütun| tam sayı||
| Alan| sicim||
| Dikey| sicim| doğru/yanlış|
| KategoriVerileri| sicim||
| IsAutoGetSerialName| sicim| doğru/yanlış|
| Alan| Başlık||

**ListObjectOperateParameter** 

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
| ListeNesnesi| Nesne||

**SayfaSonuİşlemParametresi**

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
| Sayfa Sonu Türü| sicim||
| Dizin| Dizin||
| Sıra| tam sayı||
| Kolon| tam sayı||
| Başlangıç İndeksi| tam sayı||
| EndIndex| tam sayı||


**SayfaKurulumuİşletmeParametresi**

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
| Sayfa Kurulumu| Nesne||


**PivotTableOperateParameter**

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
| HedefHücreAdı| sicim||
| KaynakVeri| sicim||
| TabloAdı| sicim||
| AynıKaynağıKullan| sicim| doğru/yanlış|
| PivotTableIndex| tam sayı||
| PivotFieldRows|tamsayı[]||
| PivotFieldColumns|tamsayı[]||
| PivotAlanVerileri|tamsayı[]||


**ŞekilİşletimParametresi**


|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
| Şekil| Nesne||


**Çalışma KitabıAyarlarıİşlemParametresi**


|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
| Çalışma Kitabı Ayarları| Nesne||

**Çalışma SayfasıİşletimParametresi**


|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
| İsim| sicim||
| Sayfa Türü| sicim||
| Yeniİsim| sicim||
| Taşınma Talebi| Nesne||

## DİNLENME API

|**API**|**Tip**|**Tanım**|**Kaynak Bağlantısı**|
|:- |:- |:- |:- |
|/hücreler/görev/görevçalıştır|POSTALAMAK|Görevi Çalıştır|[GöreviSonradan Çalıştır](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

