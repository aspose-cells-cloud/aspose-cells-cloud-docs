---
title: Aspose.Cells Ne için Bulut SDK'sı
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/available-sdks/aspose-cells-cloud-net/
description: Aspose.Cells Bulut, oluşturma, dönüştürme, birleştirme, bölme, koruma, iç nesne işlemleri vb. için Excel'i destekler
weight: 30
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdwon, Net
---
 SDK açık kaynaklıdır ve MIT Lisansı kapsamında lisanslanmıştır. Aspose.Cells Cloud için Net kütüphane kaynak koduna erişebilirsiniz.[Burada](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet).


# **Aspose.Cells Cloud'un Net kütüphanesi nasıl kullanılır?**

Aspose.Cells Cloud SDK for Net, geliştiricilerin Net programlama dilini kullanarak Microsoft Excel dosyalarını değiştirmesine ve işlemesine olanak tanıyan güçlü bir kitaplıktır. Bu SDK ile, yerel makinenize ek yazılım veya bağımlılık yüklemeden, bulutta Excel belge oluşturabilir, düzenleyebilir ve dönüştürebilirsiniz.

Bu makalede, yeni bir Excel çalışma kitabı oluşturmak, hücrelere veri eklemek ve değiştirilen çalışma kitabını buluta kaydetmek gibi bazı genel görevleri gerçekleştirmek için Aspose.Cells Cloud SDK for Net'in nasıl kullanılacağını keşfedeceğiz.

## Başlarken

 Go için Aspose.Cells Cloud SDK'yı kullanmaya başlamadan önce geliştirme ortamınızı kurmanız ve gerekli bağımlılıkları yüklemeniz gerekir. Bakınız[makale](https://docs.aspose.cloud/cells/quickstart/) Müşteri kimliğinizi ve müşteri sırrınızı almak için Aspose web sitesini ziyaret edin.

## Aspose.Cells Bulut için Net paketi nasıl kurulur

nuget'i kullanarak Aspose.Cells Cloud SDK for Net'i yükleyebilirsiniz. nuget için adımlar aşağıdadır:

```nuget

Install-Package Aspose.Cells-Cloud

```

Dotnet'i kullanarak Aspose.Cells Cloud SDK for Net'i de kurabilirsiniz. Dotnet için adımlar aşağıdadır:

```powershell

dotnet add package Aspose.Cells-Cloud 

```

## Xlsx'i PDF'e dönüştürmek için Net paketi nasıl kullanılır?

- Aspose.Cells Bulut Kitaplığını İçe Aktar
 Gerekli paketi Aspose.Cells Cloud DotNet SDK'dan projenize aktararak başlayın.
- API İstemcisini Kimlik Bilgileriyle Yapılandırma
 API istemcinizin kimliğini benzersiz istemci kimliğiniz ve istemci sırrınızla doğrulayın.
- Dönüşüm Parametrelerini Hazırlayın
 Kaynak dosya adı, istenilen çıktı formatı ve depolama klasörü yolu dahil, dönüştürme görevi için parametreleri tanımlayın.
- Çalışma Kitabı Dönüşümünü Yürüt
 PostConvertWorkbook yöntemini kullanarak dönüştürme işlemini çağırın ve yanıtı işleyin.

### **Basit kod**

```CSharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Request;
using System;
using System.IO;
using System.Collections.Generic;

CellsApi cellsApi = new CellsApi("xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx");
string remoteFolder = "TestData/In";

string localName = "Book1.xlsx";
string remoteName = "Book1.xlsx";

this.UploadFile( localName, remoteFolder + "/" + remoteName, "");

IDictionary<string, Stream> mapFiles =new Dictionary<string,Stream>(); 
AddFileParameter(localName,mapFiles);       
var request = new PutConvertWorkbookRequest(
    file: mapFiles,
    format: format
);
this.CellsApi.PutConvertWorkbook(request);
```
