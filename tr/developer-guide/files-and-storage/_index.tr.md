---
title: Dosyalar ve Depolama
second_title: Documen
type: docs
url: /tr/files-and-storage/
aliases: [/working-with-files-and-storage-using-aspose-cells-cloud/]
keywords: Aspose Cells Cloud file storage, upload, download, delete, move, copy file
description: Aspose Cells Cloud'u dosya yükleme, indirme ve yönetme gibi dosya depolama işlemleri için kullanma konusunda kapsamlı kılavuz. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift gibi çeşitli programlama dilleri için SDK desteği
weight: 100
kwords: Aspose Cells, Bulut Depolama, REST API, Dosya Yönetimi, Excel, PDF, CSV, JSON, Markdow
---
 Aspose.Cells Cloud, Aspose.Cells Cloud Storage'a veya tercih ettiğiniz herhangi bir bulut depolama alanına yüklenen dosyalarla çalışmak için kapsamlı yardımcı işlevler sunar. Üçüncü taraf depolama kurulumu konusunda yardım için lütfen şuraya bakın:[Aspose Bulut Kullanıcı Arayüzü Yardım Konuları](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

**Aspose.Cells Bulut, çeşitli dosya, klasör ve depolama işlemi API'leri sunar.**

## **Dosya Nasıl Yüklenir**

### Dosya Yükleme API Bilgi

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| yol| sicim| yol|Dosya adı ve uzantısı dahil olmak üzere dosya yükleme yolu (örneğin, /file.ext veya /Folder 1/file.ext). İçerik çok parçalıysa ve yol dosya adını içermiyorsa, Content-Disposition başlığındaki filename parametresinden dosyayı almaya çalışır.|
| dosya| Dosya| formData| Yüklenecek dosya|
| depolamaAdı| sicim| sorgu| Depolama adı|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/File/UploadFile) web tarayıcısından doğrudan REST etkileşimlerine olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Dosya Yükleme Örneği

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, API numaralı Bulut'a cURL ile nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-d {"File":{}}
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
} 
```

{{< /tab >}}
{{< /tabs >}}

## **Bir Dosya Nasıl İndirilir**

### API Dosyasını İndirin Bilgi

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| yol| sicim| yol| Dosya yolu (örneğin, '/klasör/dosya.uzantı')|
| depolamaAdı| sicim| sorgu| Depolama adı|
| sürüm kimliği| sicim| sorgu| İndirilecek dosya sürüm kimliği|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/File/DownloadFile) web tarayıcısından doğrudan REST etkileşimlerine olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Dosya İndirme Örneği

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, API numaralı Bulut'a cURL ile nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="13" tabName13="Request" tabName14="Response" >}}
{{< tab tabNum="13" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="14" >}}

```bash
{
    Stream
}
```

{{< /tab >}}
{{< /tabs >}}

## **Bir Dosya Nasıl Silinir**

### API Dosyasını Sil Bilgi

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| yol| sicim| yol| Dosya yolu (örneğin, '/klasör/dosya.uzantı')|
| depolamaAdı| sicim| sorgu| Depolama adı|
| sürüm kimliği| sicim| sorgu| Silinecek dosya sürüm kimliği|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/File/DeleteFile) web tarayıcısından doğrudan REST etkileşimlerine olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, API numaralı Bulut'a cURL ile nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="15" tabName15="Request" tabName16="Response" >}}
{{< tab tabNum="15" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/book12.xlsx" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="16" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Bir Dosya Nasıl Kopyalanır**

### API Dosyasını Kopyala Bilgi

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| srcPath| sicim| yol| Kaynak dosya yolu (örneğin, '/klasör/dosya.ext')|
|hedefYolu| sicim| sorgu| Hedef dosya yolu|
| srcDepolamaAdı| sicim| sorgu| Kaynak depolama adı|
| hedefDepolamaAdı| sicim| sorgu| Hedef depolama adı|
| sürüm kimliği| sicim| sorgu| Kopyalanacak dosya sürüm kimliği|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/File/CopyFile) web tarayıcısından doğrudan REST etkileşimlerine olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Dosya Kopyalama Örneği

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, API numaralı Bulut'a cURL ile nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="17" tabName17="Request" tabName18="Response" >}}

{{< tab tabNum="17" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/copy/Book1.xlsx?destPath=Book2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="18" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Bir Dosya Nasıl Taşınır**

### API Dosyasını Taşı Bilgisi

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| srcPath| sicim| yol| Kaynak dosya yolu (örneğin, '/src.ext')|
|hedefYolu| sicim| sorgu| Hedef dosya yolu (örneğin, '/dest.ext')|
| srcDepolamaAdı| sicim| sorgu| Kaynak depolama adı|
| hedefDepolamaAdı| sicim| sorgu| Hedef depolama adı|
| sürüm kimliği| sicim| sorgu| Taşınacak dosya sürüm kimliği|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/File/MoveFile) web tarayıcısından doğrudan REST etkileşimlerine olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Dosya Taşıma Örneği

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, API numaralı Bulut'a cURL ile nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/move/Book2.xlsx?destPath=MoveBook2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Klasör Nasıl Oluşturulur**

### API Klasörünü Oluşturun Bilgi

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| yol| sicim| yol|Oluşturulacak klasör yolu (örneğin, 'klasör_1/klasör_2/') |
| depolamaAdı| sicim| sorgu| Depolama adı|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) web tarayıcısından doğrudan REST etkileşimlerine olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Klasör Oluşturma Örneği

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, API numaralı Bulut'a cURL ile nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="3" tabName3="Request" tabName4="Response" >}}
{{< tab tabNum="3" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/newfolder" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

## **Bir Klasördeki Dosyalara Nasıl Ulaşılır**

### Dosyaları Alın API Bilgi

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| yol| sicim| yol| Klasör yolu (örneğin, '/klasör')|
| depolamaAdı| sicim| sorgu| Depolama adı|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) web tarayıcısından doğrudan REST etkileşimlerine olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Dosyaları Alma Örneği

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, API numaralı Bulut'a cURL ile nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="5" tabName5="Request" tabName6="Response" >}}
{{< tab tabNum="5" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 0,
      "Path": "string"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

## **Bir Klasör Nasıl Silinir**

### API Klasörünü Sil Bilgileri

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| yol| sicim| yol| Klasör yolu (örneğin, '/klasör')|
| depolamaAdı| sicim| sorgu| Depolama adı|
| yinelemeli| Boolean| sorgu|YANLIŞ|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) web tarayıcısından doğrudan REST etkileşimlerine olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Klasör Silme Örneği

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, API numaralı Bulut'a cURL ile nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="7" tabName7="Request" tabName8="Response" >}}

{{< tab tabNum="7" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Bir Klasör Nasıl Kopyalanır**

### Kopya Klasörü API Bilgi

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| srcPath| sicim| yol| Kaynak klasör yolu (örneğin, '/src')|
|hedefYolu| sicim| sorgu| Hedef klasör yolu (örneğin, '/dst')|
| srcDepolamaAdı| sicim| sorgu| Kaynak depolama adı|
| hedefDepolamaAdı| sicim| sorgu| Hedef depolama adı|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) web tarayıcısından doğrudan REST etkileşimlerine olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Klasör Kopyalama Örneği

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, API numaralı Bulut'a cURL ile nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="21" tabName21="Request" tabName22="Response" >}}
{{< tab tabNum="21" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/copy/srcfolder?destPath=desfolder" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="22" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Bir Klasör Nasıl Taşınır**

### Klasörü Taşı API Bilgi

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| srcPath| sicim| yol| Taşınacak klasör yolu (örneğin, '/klasör')|
|hedefYolu| sicim| sorgu| Taşınacak hedef klasör yolu (örneğin, '/dst')|
| srcDepolamaAdı| sicim| sorgu| Kaynak depolama adı|
| hedefDepolamaAdı| sicim| sorgu| Hedef depolama adı|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) web tarayıcısından doğrudan REST etkileşimlerine olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Klasör Taşıma Örneği

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, API numaralı Bulut'a cURL ile nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="23" tabName23="Request" tabName24="Response" >}}
{{< tab tabNum="23" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/move/desfolder" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabnum="24" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Depolama Alanının Varlığı Nasıl Kontrol Edilir**

### Depolama Mevcut API Bilgi

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| depolamaAdı| sicim| yol| Depolama adı|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) web tarayıcısından doğrudan REST etkileşimlerine olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Depolama Var Örneği

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, API numaralı Bulut'a cURL ile nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="33" tabName33="Request" tabName34="Response" >}}
{{< tab tabNum="33" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="34" >}}

```bash
{
  "Exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

## **Bir Dosya veya Klasörün Var Olup Olmadığını Kontrol Etme**

### Nesne Mevcut API Bilgi

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| yol| sicim| yol| Dosya veya klasör yolu (örneğin, '/dosya.ext' veya '/klasör')|
| depolamaAdı| sicim| sorgu| Depolama adı|
| sürüm kimliği| sicim| sorgu| Dosya sürüm kimliği|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) web tarayıcısından doğrudan REST etkileşimlerine olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Nesne Var Örneği

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, API numaralı Bulut'a cURL ile nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="37" tabName37="Request" tabName38="Response" >}}
{{< tab tabNum="37" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="38" >}}

```bash
{
  "Exists": true,
  "IsFolder": false
}
```

{{< /tab >}}
{{< /tabs >}}

## **Disk Kullanımı Nasıl Alınır**

### Disk Kullanım Bilgilerini Alın API

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/disc
```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| depolamaAdı| sicim| sorgu| Depolama adı|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) web tarayıcısından doğrudan REST etkileşimlerine olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Disk Kullanım Örneği Alın

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, API numaralı Bulut'a cURL ile nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="40" tabName40="Request" tabName41="Response" >}}

{{< tab tabNum="40" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/disc" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="41" >}}

```bash
{
  "UsedSize": 0,
  "TotalSize": 0
}
```

{{< /tab >}}
{{< /tabs >}}

## **Dosya Sürümleri Nasıl Alınır**

### API Dosya Sürümlerini Alın

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| yol| sicim| yol| Dosya yolu (örneğin, '/file.ext')|
| depolamaAdı| sicim| sorgu| Depolama adı|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) web tarayıcısından doğrudan REST etkileşimlerine olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Dosya Sürümlerini Alma Örneği

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, API numaralı Bulut'a cURL ile nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="46" tabName46="Request" tabName47="Response" >}}
{{< tab tabNum="46" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabnum="47" >}}

```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 0,
      "Path": "string",
      "VersionId": "string",
      "IsLatest": true
    }
  ]
} 
```

{{< /tab >}}
{{< /tabs >}}
