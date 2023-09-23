---
title: Aspose.Cells Clou aracılığıyla dosya nasıl korunur?
type: docs
url: /tr/how-to-protect-file
description: Dosya Aspose.Cells Bulut aracılığıyla nasıl korunur?
weight: 10
---
## giriiş

Aspose.Cells Cloud API, elektronik tablo dosyalarının oluşturulması, düzenlenmesi ve dönüştürülmesi için hazırlanmış güçlü bir bulut tabanlı çözümdür. Bu makalede, tipik kullanım durumları ve örnek kod da dahil olmak üzere, dosya koruması için Aspose.Cells Bulut API'i kullanma sürecinde size yol göstereceğiz.

## Genel Bakış

Aspose.Cells Bulut API, Excel veya elektronik tablo dosyalarını korumak için birden fazla güçlü API sağlar. Aspose.Cells Bulut API'i kullanarak, Excel veya diğer elektronik tablo dosyalarını zahmetsizce koruyarak çok çeşitli gereksinimleri karşılayabilirsiniz.


Dosya koruması için genellikle çeşitli çevrimiçi ortamlarla uyumlu çok sayıda API mevcuttur. Aşağıda bu API'lerin ayrıntılı bir açıklaması bulunmaktadır:

- **[Parola koruması uygulayarak MS Excel ve OpenDocument Elektronik Tablosunun güvenliğini sağlayın.](https://reference.aspose.cloud/cells/#/Workbook/PostEncryptWorkbook)** . Bu API'i nasıl arayacağınız konusunda rehberlik için lütfen şu adrese bakın:[geliştirme kılavuzu](https://docs.aspose.cloud/cells/workbook/encrypt/).
- **[MS Excel'i ve OpenDocument Elektronik Tablosunu koruyun.](https://reference.aspose.cloud/cells/#/Workbook/PostProtectWorkbook)** . Bu API'i nasıl arayacağınız konusunda rehberlik için lütfen şu adrese bakın:[geliştirme kılavuzu](https://docs.aspose.cloud/cells/workbook/protect/).
- **[MS Excel'i ve OpenDocument Elektronik Tablosunu bulut depolama kullanmadan koruyun.](https://reference.aspose.cloud/cells/#/LightCells/PostProtect)** . Bu API'i nasıl arayacağınız konusunda rehberlik için lütfen şu adrese bakın:[geliştirme kılavuzu](https://docs.aspose.cloud/cells/protect/without-using-storage/).
- **[MS Excel ve OpenDocument Elektronik Tablo dijital imzası.](https://reference.aspose.cloud/cells/#/Workbook/PostDigitalSignature)** . Bu API'i nasıl arayacağınız konusunda rehberlik için lütfen şu adrese bakın:[geliştirme kılavuzu](https://docs.aspose.cloud/cells/workbook/digital-signature/).
- **[Dosyaları toplu koruma](https://reference.aspose.cloud/cells/#/Batch/PostBatchProtect)** . Bu API'i nasıl arayacağınız konusunda rehberlik için lütfen şu adrese bakın:[geliştirme kılavuzu](https://docs.aspose.cloud/cells/batch/protect/).


# Excel dosyasını veya başka bir e-tabloyu Aspose.Cells Bulut aracılığıyla nasıl koruyabilirim?

 Aspose.Cells Bulut API şunları sağlar:[birden fazla SDK](https://github.com/aspose-cells-cloud)farklı programlama dilleri için. Tercih ettiğiniz programlama diliyle uyumlu SDK'yı seçin ve kurulum ve başlatma için birlikte gelen belgeleri izleyin. Alternatif olarak, kendi SDK'nızı aşağıdakilere göre oluşturabilirsiniz:[API referans](https://reference.aspose.cloud/cells/). Bu bölümde dosya birleştirme işlemini detaylandırmak için örnek olarak C#'i kullanacağız.


## Kayıt ve API Anahtarının Alınması

 Başlamadan önce yapmanız gerekenler[Aspose Bulut hesabını kaydedin](https://id.containerize.com/signup) Ve[kimlik doğrulama için API anahtarını edinin](https://dashboard.aspose.cloud/applications). Resmi Aspose Cloud web sitesine giriş yaparak ücretsiz bir hesap oluşturabilir ve kimlik doğrulama amacıyla API anahtarını alabilirsiniz.

 Daha ayrıntılı işlemler için lütfen aşağıdaki belgelere bakın:[Cells Cloud ile Hızlı Başlangıç](https://docs.aspose.cloud/cells/quickstart/)


## Aspose.Cells Bulut SDK'sını Yükleme ve Başlatma

Aspose.Cells-Cloud NuGet paketini .NET projenize kurun, NuGet Paket Yönetici Konsolunu veya Visual Studio’deki NuGet Paket Yöneticisini kullanabilirsiniz.
Paket Yönetici Konsolu'nu kullanarak paketi şu şekilde yükleyebilirsiniz:

```Powershell

Install-Package Aspose.Cells-Cloud

```
CellsApi sınıfının yeni bir örneğini oluşturur ve onu istemci kimliğiniz ve istemci sırrınızla başlatır. Yukarıda belirtilen kod pasajının ayrıntıları aşağıda verilmiştir:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

KENDİNİZİ değiştirdiğinizden emin olun_API_ANAHTAR, SİZİN_UYGULAMA_SID ve SİZİN_UYGULAMA_Gerçek API anahtarınızı, uygulama SID'nizi ve uygulama anahtarınızı içeren KEY.

## API İsteğini oluşturun ve API'i arayın.

Bu, PostProtectRequest'in yeni bir örneğini oluşturur ve onu istediğiniz dosyalar ve koruma Çalışma Kitabı isteğiyle başlatır. Daha sonra bu koruma isteğiyle korumayı API çağırır. Koruma işlevi, genişletilmiş sorgu parametrelerini de destekler. Yukarıda belirtilen kod pasajının ayrıntıları aşağıda verilmiştir:


```CSharp

using System.Collections.Generic;

PostProtectRequest request = new PostProtectRequest();

IDictionary<string, System.IO.Stream> mapFiles =new Dictionary<string, System.IO.Stream>(); 
mapFiles.Add("Book1.xlsx", File.OpenRead(@"c:\testdata\Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead(@"c:\testdata\Book2.xlsx"));
request.Files = mapFiles;

request.protectWorkbookRequst = new ProtectWorkbookRequst {
    AwaysOpenReadOnly = true ,
    EncryptWithPassword = "123456",
    ProtectCurrentSheet = new Protection { 
        AllowDeletingColumn =true
    }
};


cellsInstance.PostProtect(request);

```


## Kullanım Durumları

**korumak** Excel dosyası veya Aspose.Cells Cloud API'in başka bir elektronik tablo özelliği, çeşitli pratik kullanım durumlarında faydalıdır. İşte bazı yaygın senaryolar:

-  Eklemek**çoklu dijital imza dosyaları**yerel Excel dosyaları veya başka bir elektronik tablo dosyası için.
-  Eklemek**şifre koruması**yerel Excel dosyaları veya başka bir elektronik tablo dosyası için.
-  Ayarlamak**Her Zaman Açık Salt Okunur** Kolay paylaşım için.
- **Birden fazla dosyayı bir html dosyasında birleştirme** Web sayfalarında görüntülemek ve gömmek için.

## Çözüm

Aspose.Cells Cloud API ile korumalı Excel dosyalarını veya başka bir elektronik tablo dosyasını kolayca gerçekleştirebilirsiniz. Basit API aramaları yaparak ve uygun koruma seçeneklerini ayarlayarak, çeşitli dosya birleştirilmiş gereksinimleri verimli bir şekilde karşılayabilirsiniz. Üretkenliği artırmak ve geliştirme süresinden tasarruf etmek için Aspose.Cells Bulut API'i uygulamalarınıza entegre edin.

 Lütfen yukarıdaki örnek kodun yalnızca tanıtım amaçlı olduğunu ve onu pratikte kullanırken onu geçerli kimlik doğrulama bilgileri ve dosya yollarıyla değiştirmeniz gerekeceğini unutmayın. Ayrıca Aspose.Cells Cloud API, elektronik tablo oluşturma, düzenleme, işleme ve veri işleme gibi birçok başka özellik sunar. Ayrıntılı API belgelerini ve örnek kodu şu adreste bulabilirsiniz:[resmi Aspose web sitesinin geliştirici kılavuzu](/developer-guide/).

Bu makalenin dosya birleştirme için Aspose.Cells Cloud API'i nasıl kullanacağınızı anlamanıza yardımcı olacağını umuyoruz. Uygulamanızda iyi şanslar!

