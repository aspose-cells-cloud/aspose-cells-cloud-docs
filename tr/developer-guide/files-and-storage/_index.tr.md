---
title: "Aspose.Cells Cloud API – Dosya ve Klasör Yönetimi (Yükleme, İndirme, Kopyalama, Taşıma)"
second_title: "Belge"
ArticleTitle: "Excel İçin Bulut Dosya Yönetimi – Excel Dosyası Depolama ve Akıllı Düzenleme İçin Verimli ve Güvenli Bir Çözüm"
linktitle: "Dosyalar ve Depolama"
type: docs
url: /files-and-storage/
aliases: [/working-with-files-and-storage-using-aspose-cells-cloud/]
keywords: "Aspose.Cells Cloud, dosya depolama API'si, Excel dosyası yükleme, Excel dosyası indirme, dosya kopyalama, dosya taşıma, dosya silme, klasör yönetimi, REST API, cURL örnekleri"
description: "Aspose.Cells Cloud deposunda Excel dosyalarını ve klasörlerini yönetmeye yönelik kapsamlı kılavuz. cURL örnekleri, gerekli parametreler ve kimlik doğrulama notları ile birlikte yükleme, indirme, kopyalama, taşıma, silme ve klasör işlemleri içerir."
weight: 100
---

Aspose.Cells Cloud, Aspose.Cells Cloud Depolama’da veya tercih ettiğiniz herhangi bir üçüncü taraf bulut depolama alanında saklanan dosyalarla çalışmak için kapsamlı bir dizi yardımcı işlev sağlar. Üçüncü taraf depolama kurulumu konusunda yardım için lütfen [Aspose Cloud UI Yardım Konuları](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics) sayfasına bakın.

**Aspose.Cells Cloud, dosya, klasör ve depolama işlemi API’leri sunar.**

> **Not:** Tüm API çağrıları **HTTPS** protokolünü kullanmalıdır. JWT jetonu alma hakkında ayrıntılı bilgi için [Kimlik Doğrulama Kılavuzu](/cells/authentication/) sayfasına bakın.

**Önkoşullar:** Bu API’leri kullanmak için geçerli bir Aspose Cloud hesabınızın olması, bir JWT erişim jetonu elde etmeniz ve bir depolama konumunun yapılandırılmış (Aspose Cloud Depolama veya bağlanmış bir üçüncü taraf depolama) olması gerekir.

**Son güncelleme tarihi:** 2024‑12‑01

## **Dosya Nasıl Yüklenebilir?**

### Dosya Yükleme API Bilgileri

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

İstek parametreleri aşağıda listelenmiştir:

| Parametre Adı | Tür   | Konum | Açıklama |
|---------------|-------|-------|----------|
| path          | string | path | Dosyanın yükleneceği yol, dosya adı ve uzantı dahil (örneğin `/klasör1/Rapor.xlsx`). |
| file          | file   | formData | Yüklenecek dosya. |
| storageName   | string | query | Kullanılacak depolama adı. |

**HTTP Yanıtları**

| Kod | Açıklama                              |
|-----|---------------------------------------|
| 200 | Dosya başarıyla yüklendi.             |
| 400 | Geçersiz istek – eksik veya geçersiz parametreler. |
| 401 | Yetkisiz erişim – geçersiz veya eksik JWT jetonu. |
| 404 | Depolama bulunamadı.                  |
| 500 | İç sunucu hatası.                     |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/File/UploadFile), doğrudan bir web tarayıcısından REST etkileşimlerini mümkün kılan genel olarak erişilebilir bir programlama arayüzü tanımlar.

### Dosya Yükleme Örneği

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile bir dosya nasıl yükleneceğini göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}
{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/Rapor.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt jetonu>" \
  -F "File=@Rapor.xlsx"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```json
{
  "Uploaded": [
    "MyFolder/Rapor.xlsx"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*Not: Yükleme için maksimum dosya boyutu 100 MB’dir. Oran sınırlamaları uygulanabilir.*

## **Dosya Nasıl İndirilebilir?**

### Dosya İndirme API Bilgileri

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

İstek parametreleri aşağıda listelenmiştir:

| Parametre Adı | Tür   | Konum | Açıklama |
|---------------|-------|-------|----------|
| path          | string | path | Dosya yolu (örneğin `/klasör/Rapor.xlsx`). |
| storageName   | string | query | Kullanılacak depolama adı. |
| versionId     | string | query | İndirilecek dosya sürümünün tanımlayıcısı (isteğe bağlı). |

**HTTP Yanıtları**

| Kod | Açıklama                              |
|-----|---------------------------------------|
| 200 | Dosya indirildi; ikili akış döndürüldü. |
| 400 | Geçersiz istek – geçersiz parametreler. |
| 401 | Yetkisiz erişim – eksik veya geçersiz JWT. |
| 404 | Dosya bulunamadı.                     |
| 500 | İç sunucu hatası.                     |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/File/DownloadFile), doğrudan bir web tarayıcısından REST etkileşimlerini mümkün kılan genel olarak erişilebilir bir programlama arayüzü tanımlar.

### Dosya İndirme Örneği

{{< tabs tabTotal="2" tabID="13" tabName13="İstek" tabName14="Yanıt" >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/Rapor.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt jetonu>"
```

{{< /tab >}}
{{< tab tabNum="14" >}}

```json
{
  "Stream": "<ikili veri>"
}
```

{{< /tab >}}
{{< /tabs >}}

*Not: Yanıt, dosyanın ikili akışını içerir. cURL kullanırken çıktıyı bir dosyaya kaydedin (`-o dosyaadı.xlsx`).*

## **Dosya Nasıl Silinebilir?**

### Dosya Silme API Bilgileri

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

İstek parametreleri aşağıda listelenmiştir:

| Parametre Adı | Tür   | Konum | Açıklama |
|---------------|-------|-------|----------|
| path          | string | path | Dosya yolu (örneğin `/klasör/Rapor.xlsx`). |
| storageName   | string | query | Kullanılacak depolama adı. |
| versionId     | string | query | Silinecek dosya sürümünün tanımlayıcısı (isteğe bağlı). |

**HTTP Yanıtları**

| Kod | Açıklama                              |
|-----|---------------------------------------|
| 200 | Dosya başarıyla silindi.              |
| 400 | Geçersiz istek – eksik veya geçersiz parametreler. |
| 401 | Yetkisiz erişim – geçersiz JWT jetonu. |
| 404 | Dosya bulunamadı.                     |
| 500 | İç sunucu hatası.                     |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/File/DeleteFile), doğrudan bir web tarayıcısından REST etkileşimlerini mümkün kılan genel olarak erişilebilir bir programlama arayüzü tanımlar.

### Dosya Silme Örneği

{{< tabs tabTotal="2" tabID="15" tabName15="İstek" tabName16="Yanıt" >}}
{{< tab tabNum="15" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/EskiRapor.xlsx" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt jetonu>"
```

{{< /tab >}}
{{< tab tabNum="16" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Not: Dosya silme işlemi kalıcıdır; gerekirse yedek aldığınızdan emin olun.*

## **Dosya Nasıl Kopyalanabilir?**

### Dosya Kopyalama API Bilgileri

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

İstek parametreleri aşağıda listelenmiştir:

| Parametre Adı    | Tür   | Konum | Açıklama |
|------------------|-------|-------|----------|
| srcPath          | string | path | Kaynak dosya yolu (örneğin `/klasör/Kaynak.xlsx`). |
| destPath         | string | query | Hedef dosya yolu (örneğin `/klasör/Hedef.xlsx`). |
| srcStorageName   | string | query | Kaynak depolama adı (isteğe bağlı). |
| destStorageName  | string | query | Hedef depolama adı (isteğe bağlı). |
| versionId        | string | query | Kopyalanacak dosya sürümü tanımlayıcısı (isteğe bağlı). |

**HTTP Yanıtları**

| Kod | Açıklama                              |
|-----|---------------------------------------|
| 200 | Dosya başarıyla kopyalandı.           |
| 400 | Geçersiz istek – geçersiz parametreler. |
| 401 | Yetkisiz erişim – eksik veya geçersiz JWT. |
| 404 | Kaynak dosya bulunamadı.              |
| 500 | İç sunucu hatası.                     |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/File/CopyFile), doğrudan bir web tarayıcısından REST etkileşimlerini mümkün kılan genel olarak erişilebilir bir programlama arayüzü tanımlar.

### Dosya Kopyalama Örneği

{{< tabs tabTotal="2" tabID="17" tabName17="İstek" tabName18="Yanıt" >}}
{{< tab tabNum="17" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/copy/MyFolder/Rapor.xlsx?destPath=MyFolder/RaporKopya.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt jetonu>"
```

{{< /tab >}}
{{< tab tabNum="18" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Not: Kopyalama işlemi kaynak dosyayı kaldırmaz.*

## **Dosya Nasıl Taşınabilir?**

### Dosya Taşıma API Bilgileri

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

İstek parametreleri aşağıda listelenmiştir:

| Parametre Adı    | Tür   | Konum | Açıklama |
|------------------|-------|-------|----------|
| srcPath          | string | path | Kaynak dosya yolu (örneğin `/klasör/Kaynak.xlsx`). |
| destPath         | string | query | Hedef dosya yolu (örneğin `/klasör/Hedef.xlsx`). |
| srcStorageName   | string | query | Kaynak depolama adı (isteğe bağlı). |
| destStorageName  | string | query | Hedef depolama adı (isteğe bağlı). |
| versionId        | string | query | Taşınacak dosya sürümü tanımlayıcısı (isteğe bağlı). |

**HTTP Yanıtları**

| Kod | Açıklama                              |
|-----|---------------------------------------|
| 200 | Dosya başarıyla taşındı.              |
| 400 | Geçersiz istek – geçersiz parametreler. |
| 401 | Yetkisiz erişim – eksik veya geçersiz JWT. |
| 404 | Kaynak dosya bulunamadı.              |
| 500 | İç sunucu hatası.                     |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/File/MoveFile), doğrudan bir web tarayıcısından REST etkileşimlerini mümkün kılan genel olarak erişilebilir bir programlama arayüzü tanımlar.

### Dosya Taşıma Örneği

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/move/MyFolder/Rapor.xlsx?destPath=MyFolder/RaporTasinmis.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt jetonu>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Not: Dosya taşıma işlemi dosyanın sürüm geçmişi bilgisini korur.*

## **Klasör Nasıl Oluşturulur?**

### Klasör Oluşturma API Bilgileri

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

İstek parametreleri aşağıda listelenmiştir:

| Parametre Adı | Tür   | Konum | Açıklama |
|---------------|-------|-------|----------|
| path          | string | path | Oluşturulacak klasör yolu (örneğin `klasör1/klasör2/`). |
| storageName   | string | query | Kullanılacak depolama adı. |

**HTTP Yanıtları**

| Kod | Açıklama                              |
|-----|---------------------------------------|
| 200 | Klasör başarıyla oluşturuldu.         |
| 400 | Geçersiz istek – geçersiz yol veya parametreler. |
| 401 | Yetkisiz erişim – eksik veya geçersiz JWT. |
| 500 | İç sunucu hatası.                     |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder), doğrudan bir web tarayıcısından REST etkileşimlerini mümkün kılan genel olarak erişilebilir bir programlama arayüzü tanımlar.

### Klasör Oluşturma Örneği

{{< tabs tabTotal="2" tabID="3" tabName3="İstek" tabName4="Yanıt" >}}
{{< tab tabNum="3" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/yeniklasör" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt jetonu>"
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```json
{
  "Uploaded": [
    "yeniklasör"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*Not: Klasör yolları büyük/küçük harfe duyarlıdır.*

## **Bir Klasördeki Dosyalar Nasıl Listelenir?**

### Dosyaları Listeleme API Bilgileri

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

İstek parametreleri aşağıda listelenmiştir:

| Parametre Adı | Tür   | Konum | Açıklama |
|---------------|-------|-------|----------|
| path          | string | path | Klasör yolu (örneğin `/klasör`). |
| storageName   | string | query | Kullanılacak depolama adı. |

**HTTP Yanıtları**

| Kod | Açıklama                              |
|-----|---------------------------------------|
| 200 | Dosya ve alt klasör listesi döndürüldü. |
| 400 | Geçersiz istek – geçersiz yol.        |
| 401 | Yetkisiz erişim – eksik veya geçersiz JWT. |
| 404 | Klasör bulunamadı.                    |
| 500 | İç sunucu hatası.                     |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList), doğrudan bir web tarayıcısından REST etkileşimlerini mümkün kılan genel olarak erişilebilir bir programlama arayüzü tanımlar.

### Dosyaları Listeleme Örneği

{{< tabs tabTotal="2" tabID="5" tabName5="İstek" tabName6="Yanıt" >}}
{{< tab tabNum="5" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt jetonu>"
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```json
{
  "Value": [
    {
      "Name": "Rapor.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 102400,
      "Path": "/desfolder/Rapor.xlsx"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

*Not: Yanıt, belirtilen yoldaki hem dosyaları hem de alt klasörleri listeler.*

## **Klasör Nasıl Silinebilir?**

### Klasör Silme API Bilgileri

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

İstek parametreleri aşağıda listelenmiştir:

| Parametre Adı | Tür    | Konum | Açıklama |
|---------------|--------|-------|----------|
| path          | string | path | Klasör yolu (örneğin `/klasör`). |
| storageName   | string | query | Kullanılacak depolama adı. |
| recursive     | boolean | query | Klasörü özyinelemeli olarak silmek için `true` olarak ayarlayın. |

**HTTP Yanıtları**

| Kod | Açıklama                              |
|-----|---------------------------------------|
| 200 | Klasör başarıyla silindi.             |
| 400 | Geçersiz istek – geçersiz parametreler. |
| 401 | Yetkisiz erişim – eksik veya geçersiz JWT. |
| 404 | Klasör bulunamadı.                    |
| 500 | İç sunucu hatası.                     |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder), doğrudan bir web tarayıcısından REST etkileşimlerini mümkün kılan genel olarak erişilebilir bir programlama arayüzü tanımlar.

### Klasör Silme Örneği

{{< tabs tabTotal="2" tabID="7" tabName7="İstek" tabName8="Yanıt" >}}
{{< tab tabNum="7" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt jetonu>"
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Not: `recursive=true` ayarıyla bir klasörün silinmesi, tüm içeriğini kalıcı olarak siler.*

## **Klasör Nasıl Kopyalanabilir?**

### Klasör Kopyalama API Bilgileri

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

İstek parametreleri aşağıda listelenmiştir:

| Parametre Adı    | Tür   | Konum | Açıklama |
|------------------|-------|-------|----------|
| srcPath          | string | path | Kaynak klasör yolu (örneğin `/kaynak`). |
| destPath         | string | query | Hedef klasör yolu (örneğin `/hedef`). |
| srcStorageName   | string | query | Kaynak depolama adı (isteğe bağlı). |
| destStorageName  | string | query | Hedef depolama adı (isteğe bağlı). |

**HTTP Yanıtları**

| Kod | Açıklama                              |
|-----|---------------------------------------|
| 200 | Klasör başarıyla kopyalandı.          |
| 400 | Geçersiz istek – geçersiz parametreler. |
| 401 | Yetkisiz erişim – eksik veya geçersiz JWT. |
| 404 | Kaynak klasör bulunamadı.             |
| 500 | İç sunucu hatası.                     |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder), doğrudan bir web tarayıcısından REST etkileşimlerini mümkün kılan genel olarak erişilebilir bir programlama arayüzü tanımlar.

### Klasör Kopyalama Örneği

{{< tabs tabTotal="2" tabID="21" tabName21="İstek" tabName22="Yanıt" >}}
{{< tab tabNum="21" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/copy/kaynakklasör?destPath=hedefklasör" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt jetonu>"
```

{{< /tab >}}
{{< tab tabNum="22" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Not: Kopyalama işlemi, kaynakla aynı içeriğe sahip yeni bir klasör oluşturur.*

## **Klasör Nasıl Taşınabilir?**

### Klasör Taşıma API Bilgileri

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

İstek parametreleri aşağıda listelenmiştir:

| Parametre Adı    | Tür   | Konum | Açıklama |
|------------------|-------|-------|----------|
| srcPath          | string | path | Kaynak klasör yolu (örneğin `/klasör`). |
| destPath         | string | query | Hedef klasör yolu (örneğin `/hedef`). |
| srcStorageName   | string | query | Kaynak depolama adı (isteğe bağlı). |
| destStorageName  | string | query | Hedef depolama adı (isteğe bağlı). |

**HTTP Yanıtları**

| Kod | Açıklama                              |
|-----|---------------------------------------|
| 200 | Klasör başarıyla taşındı.             |
| 400 | Geçersiz istek – geçersiz parametreler. |
| 401 | Yetkisiz erişim – eksik veya geçersiz JWT. |
| 404 | Kaynak klasör bulunamadı.             |
| 500 | İç sunucu hatası.                     |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder), doğrudan bir web tarayıcısından REST etkileşimlerini mümkün kılan genel olarak erişilebilir bir programlama arayüzü tanımlar.

### Klasör Taşıma Örneği

{{< tabs tabTotal="2" tabID="23" tabName23="İstek" tabName24="Yanıt" >}}
{{< tab tabNum="23" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/move/desfolder?destPath=hedefklasör" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt jetonu>"
```

{{< /tab >}}
{{< tab tabNum="24" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Not: Klasör taşıma işlemi, klasörün iç yapısını ve dosya sürümlerini korur.*

## **Depolama Var mı Kontrolü Nasıl Yapılır?**

### Depolama Varlık Kontrolü API Bilgileri

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

İstek parametreleri aşağıda listelenmiştir:

| Parametre Adı | Tür   | Konum | Açıklama |
|---------------|-------|-------|----------|
| storageName   | string | path | Kontrol edilecek depolama adı. |

**HTTP Yanıtları**

| Kod | Açıklama                              |
|-----|---------------------------------------|
| 200 | Depolama varlık durumu döndürüldü (`true` veya `false`). |
| 401 | Yetkisiz erişim – eksik veya geçersiz JWT. |
| 404 | Depolama bulunamadı.                  |
| 500 | İç sunucu hatası.                     |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Storage/StorageExists), doğrudan bir web tarayıcısından REST etkileşimlerini mümkün kılan genel olarak erişilebilir bir programlama arayüzü tanımlar.

### Depolama Varlık Kontrolü Örneği

{{< tabs tabTotal="2" tabID="33" tabName33="İstek" tabName34="Yanıt" >}}
{{< tab tabNum="33" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/MyStorage/exist" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt jetonu>"
```

{{< /tab >}}
{{< tab tabNum="34" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

## **Dosya veya Klasör Var mı Kontrolü Nasıl Yapılır?**

### Nesne Varlık Kontrolü API Bilgileri

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

İstek parametreleri aşağıda listelenmiştir:

| Parametre Adı | Tür   | Konum | Açıklama |
|---------------|-------|-------|----------|
| path          | string | path | Dosya veya klasör yolu (örneğin `/dosya.xlsx` veya `/klasör`). |
| storageName   | string | query | Kontrol edilecek depolama adı. |
| versionId     | string | query | Dosya sürümü tanımlayıcısı (isteğe bağlı). |

**HTTP Yanıtları**

| Kod | Açıklama                              |
|-----|---------------------------------------|
| 200 | Varlık bilgisi döndürüldü.            |
| 401 | Yetkisiz erişim – eksik veya geçersiz JWT. |
| 404 | Dosya veya klasör bulunamadı.         |
| 500 | İç sunucu hatası.                     |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists), doğrudan bir web tarayıcısından REST etkileşimlerini mümkün kılan genel olarak erişilebilir bir programlama arayüzü tanımlar.

### Nesne Varlık Kontrolü Örneği

{{< tabs tabTotal="2" tabID="37" tabName37="İstek" tabName38="Yanıt" >}}
{{< tab tabNum="37" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt jetonu>"
```

{{< /tab >}}
{{< tab tabNum="38" >}}

```json
{
  "Exists": true,
  "IsFolder": false
}
```

{{< /tab >}}
{{< /tabs >}}

## **Disk Kullanımı Nasıl Görüntülenir?**

### Disk Kullanımı Görüntüleme API Bilgileri

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/disc
```

İstek parametreleri aşağıda listelenmiştir:

| Parametre Adı | Tür   | Konum | Açıklama |
|---------------|-------|-------|----------|
| storageName   | string | query | Sorgulanacak depolama adı. |

**HTTP Yanıtları**

| Kod | Açıklama                              |
|-----|---------------------------------------|
| 200 | Disk kullanımı bilgisi döndürüldü.    |
| 401 | Yetkisiz erişim – eksik veya geçersiz JWT. |
| 500 | İç sunucu hatası.                     |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage), doğrudan bir web tarayıcısından REST etkileşimlerini mümkün kılan genel olarak erişilebilir bir programlama arayüzü tanımlar.

### Disk Kullanımı Görüntüleme Örneği

{{< tabs tabTotal="2" tabID="40" tabName40="İstek" tabName41="Yanıt" >}}
{{< tab tabNum="40" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/disc?storageName=MyStorage" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt jetonu>"
```

{{< /tab >}}
{{< tab tabNum="41" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 987654321
}
```

{{< /tab >}}
{{< /tabs >}}

## **Dosya Sürümleri Nasıl Görüntülenir?**

### Dosya Sürümlerini Görüntüleme API Bilgileri

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

İstek parametreleri aşağıda listelenmiştir:

| Parametre Adı | Tür   | Konum | Açıklama |
|---------------|-------|-------|----------|
| path          | string | path | Dosya yolu (örneğin `/dosya.xlsx`). |
| storageName   | string | query | Sorgulanacak depolama adı. |

**HTTP Yanıtları**

| Kod | Açıklama                              |
|-----|---------------------------------------|
| 200 | Dosya sürüm listesi döndürüldü.       |
| 401 | Yetkisiz erişim – eksik veya geçersiz JWT. |
| 404 | Dosya bulunamadı.                     |
| 500 | İç sunucu hatası.                     |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions), doğrudan bir web tarayıcısından REST etkileşimlerini mümkün kılan genel olarak erişilebilir bir programlama arayüzü tanımlar.

### Dosya Sürümlerini Görüntüleme Örneği

{{< tabs tabTotal="2" tabID="46" tabName46="İstek" tabName47="Yanıt" >}}
{{< tab tabNum="46" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/version/Rapor.xlsx?storageName=MyStorage" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt jetonu>"
```

{{< /tab >}}
{{< tab tabNum="47" >}}

```json
{
  "Value": [
    {
      "Name": "Rapor.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 102400,
      "Path": "/Rapor.xlsx",
      "VersionId": "1",
      "IsLatest": true
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}