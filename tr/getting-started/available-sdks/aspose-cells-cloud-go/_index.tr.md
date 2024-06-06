---
title: Aspose.Cells G için Bulut SDK'sı
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/available-sdks/aspose-cells-cloud-go/
description: Aspose.Cells Go için Bulut SDK'sı, Go geliştiricilerine güçlü platformlar arası destek sağlayarak Windows, Linux veya macOS için entegrasyonu ve kullanımı kolaylaştırır. Oluşturma, dönüştürme, birleştirme, bölme, koruma, iç nesne işlemleri vb. için Excel'i destekler.
weight: 30
kwords: Go, Excel, Office Cloud, REST API, Grafik, Pivot Tablo, Tablo, Elektronik Tablo, PDF, CSV, Json, Markdown
---
 SDK açık kaynaklıdır ve MIT Lisansı kapsamında lisanslanmıştır. Aspose.Cells Cloud için Go kütüphanesi kaynak koduna erişebilirsiniz.[Burada](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go).

# **Aspose.Cells Cloud'un Go kütüphanesi nasıl kullanılır?**

Aspose.Cells Go için Bulut SDK'sı, geliştiricilerin Go programlama dilini kullanarak Microsoft Excel dosyalarını değiştirmesine ve işlemesine olanak tanıyan güçlü bir kitaplıktır. Bu SDK ile, yerel makinenize ek yazılım veya bağımlılık yüklemeden, bulutta Excel belge oluşturabilir, düzenleyebilir ve dönüştürebilirsiniz.

Bu makalede, yeni bir Excel çalışma kitabı oluşturmak, hücrelere veri eklemek ve değiştirilen çalışma kitabını buluta kaydetmek gibi bazı genel görevleri gerçekleştirmek için Aspose.Cells Go Bulut SDK'sının nasıl kullanılacağını keşfedeceğiz.

## **Başlarken**

 Go için Aspose.Cells Cloud SDK'yı kullanmaya başlamadan önce geliştirme ortamınızı kurmanız ve gerekli bağımlılıkları yüklemeniz gerekir. Bakınız[makale](https://docs.aspose.cloud/cells/quickstart/) Müşteri kimliğinizi ve müşteri sırrınızı almak için Aspose web sitesini ziyaret edin.

## Aspose.Cells Cloud için Go paketi nasıl kurulur

`go get` komutunu kullanarak Aspose.Cells Cloud SDK for Go'yu yükleyebilirsiniz. Terminalinizi veya komut isteminizi açın ve aşağıdaki komutu çalıştırın:

```bash
go get -u github.com/aspose-cells-cloud/aspose-cells-cloud-go
```

Bu, SDK'nın en son sürümünü Go çalışma alanınıza indirip yükleyecektir.


## Go kütüphanesini projenize nasıl aktarabilirsiniz?


```golang
package main

import (
	asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
```

## Xlsx'i PDF'e dönüştürmek için Go paketi nasıl kullanılır?

- Aspose.Cells Bulut Kitaplığını İçe Aktar
Gerekli paketi Aspose.Cells Cloud Go SDK'dan projenize aktararak başlayın.
- API İstemcisini Kimlik Bilgileriyle Yapılandırma
 API istemcinizin kimliğini benzersiz istemci kimliğiniz ve istemci sırrınızla doğrulayın.
- Dönüşüm Parametrelerini Hazırlayın
 Kaynak dosya adı, istenilen çıktı formatı ve depolama klasörü yolu dahil, dönüştürme görevi için parametreleri tanımlayın.
- Çalışma Kitabı Dönüşümünü Yürüt
 PostConvertWorkbook yöntemini kullanarak dönüştürme işlemini çağırın ve yanıtı işleyin.

### **Basit kod**

```golang
package main

import (
	"os"
	asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
func main() {
	instance := asposecellscloud.NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"), "https://api.aspose.cloud", "v3.0")
    remoteFolder := "TestData/In"

    localName := "Book1.xlsx"
    remoteName := "Book1.xlsx"

    format := "pdf"

    var mapFiles map[string]string       
    mapFiles = make(map[string]string)
    mapFiles[localName]=  localName 

    request := new (asposecellscloud.PutConvertWorkbookRequest)
    request.File =         mapFiles    
    request.Format =         format    
    _, httpResponse, err := instance.PutConvertWorkbook(request)
    if err != nil {
      print(err)
    } else if httpResponse.StatusCode < 200 || httpResponse.StatusCode > 299 {
      print("Test fail")
    }
}

```
