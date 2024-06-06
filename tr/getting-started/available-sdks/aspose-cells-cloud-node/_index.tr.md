---
title: Aspose.Cells Nod için Bulut SDK'sı
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/available-sdks/aspose-cells-cloud-node/
description: Aspose.Cells Bulut, oluşturma, dönüştürme, birleştirme, bölme, koruma, iç nesne işlemleri vb. için Excel'i destekler
weight: 30
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdwon, Düğüm
---
 SDK açık kaynaklıdır ve MIT Lisansı kapsamında lisanslanmıştır. Aspose.Cells Cloud için Node kütüphanesi kaynak koduna erişebilirsiniz.[Burada](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).


# **Aspose.Cells Cloud'un Düğüm kitaplığı nasıl kullanılır?**

Aspose.Cells Node için Bulut SDK'sı, geliştiricilerin Node programlama dilini kullanarak Microsoft Excel dosyalarını değiştirmesine ve işlemesine olanak tanıyan güçlü bir kitaplıktır. Bu SDK ile, yerel makinenize ek yazılım veya bağımlılık yüklemeden, bulutta Excel belge oluşturabilir, düzenleyebilir ve dönüştürebilirsiniz.


Bu makalede, yeni bir Excel çalışma kitabı oluşturmak, hücrelere veri eklemek ve değiştirilen çalışma kitabını buluta kaydetmek gibi bazı genel görevleri gerçekleştirmek için Düğüm için Aspose.Cells Bulut SDK'sının nasıl kullanılacağını keşfedeceğiz.

## Başlarken

 Go için Aspose.Cells Cloud SDK'yı kullanmaya başlamadan önce geliştirme ortamınızı kurmanız ve gerekli bağımlılıkları yüklemeniz gerekir. Bakınız[makale](https://docs.aspose.cloud/cells/quickstart/) Müşteri kimliğinizi ve müşteri sırrınızı almak için Aspose web sitesini ziyaret edin.

## Aspose.Cells Bulut için Düğüm paketi nasıl kurulur

Npm kullanarak Node için Aspose.Cells Cloud SDK'yı yükleyebilirsiniz. Aşağıda npm için adımlar verilmiştir:


```Powershell

npm install asposecellscloud

```

## Aspose.Cells Cloud için paket yapılandırmasına bağımlılıklar nasıl eklenir?

düğüm yapılandırma dosyası: package.json

```Node

{
    "requires": true,
    "lockfileVersion": 1,
    "dependencies": {
        "@types/jest": "^26.0.24",
        "@types/request": "^2.48.7",
        "asposecellscloud": "24.4",
        "axios": "^1.5.1",
        "JSON": "^1.0.0",
        "mocha": "^10.2.0",
        "request": "^2.88.2",
        "request-debug": "^0.2.0"
    }
}

```

## Xlsx'i PDF'e dönüştürmek için Düğüm paketi nasıl kullanılır?

- Aspose.Cells Bulut Kitaplığını İçe Aktar
 Gerekli paketi Aspose.Cells Cloud NodeJS SDK'sından projenize aktararak başlayın.
- API İstemcisini Kimlik Bilgileriyle Yapılandırma
 API istemcinizin kimliğini benzersiz istemci kimliğiniz ve istemci sırrınızla doğrulayın.
- Dönüşüm Parametrelerini Hazırlayın
 Kaynak dosya adı, istenilen çıktı formatı ve depolama klasörü yolu dahil, dönüştürme görevi için parametreleri tanımlayın.
- Çalışma Kitabı Dönüşümünü Yürüt
 PostConvertWorkbook yöntemini kullanarak dönüştürme işlemini çağırın ve yanıtı işleyin.

```javascript
var fs = require('fs');
var path = require('path');
const _ = require('asposecellscloud');

const cellsApi = new CellsApi(process.env.CellsCloudClientId, process.env.CellsCloudClientSecret,"v3.0",process.env.CellsCloudApiBaseUrl);

var remoteFolder = "TestData/In"
  
var localName = "Book1.xlsx"
var remoteName = "Book1.xlsx"

var localNameRequest = new  model.UploadFileRequest();
localNameRequest.uploadFiles ={localName:fs.createReadStream(localPath  + localName)};
localNameRequest.path = remoteFolder + "/" + remoteName ;
localNameRequest.storageName ="";
cellsApi.uploadFile(localNameRequest );
 
var format = "csv"

var mapFiles = {};           

 mapFiles[localName]= fs.createReadStream(localPath  +localName) ;

var request = new model.PutConvertWorkbookRequest();
request.file =  mapFiles;
request.format =  format;
return cellsApi.putConvertWorkbook(request).then((result) => {
    expect(result.response.statusCode).to.equal(200);
});
```
