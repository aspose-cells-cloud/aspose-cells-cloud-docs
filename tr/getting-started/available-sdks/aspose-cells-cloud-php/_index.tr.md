---
title: Aspose.Cells PH için Bulut SDK'sı
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/available-sdks/aspose-cells-cloud-php/
description: Aspose.Cells Bulut, oluşturma, dönüştürme, birleştirme, bölme, koruma, iç nesne işlemleri vb. için Excel'i destekler
weight: 30
kwords: Excel, Office Cloud, REST API, Elektronik Tablo, PDF, CSV, Json, Markdwon, PHP
---
 SDK açık kaynaklıdır ve MIT Lisansı kapsamında lisanslanmıştır. Aspose.Cells Bulut için PHP kütüphane kaynak koduna ulaşabilirsiniz.[Burada](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

# **PHP için Aspose.Cells Cloud SDK nasıl kullanılır?**

Aspose.Cells PHP için Bulut SDK'sı, geliştiricilerin Go programlama dilini kullanarak Microsoft Excel dosyalarını değiştirmesine ve işlemesine olanak tanıyan güçlü bir kitaplıktır. Bu SDK ile, yerel makinenize ek yazılım veya bağımlılık yüklemeden, bulutta Excel belge oluşturabilir, düzenleyebilir ve dönüştürebilirsiniz.

Bu makalede, yeni bir Excel çalışma kitabı oluşturmak, hücrelere veri eklemek ve değiştirilen çalışma kitabını buluta kaydetmek gibi bazı genel görevleri gerçekleştirmek için PHP için Aspose.Cells Bulut SDK'sının nasıl kullanılacağını keşfedeceğiz.

## Başlarken

 Go için Aspose.Cells Cloud SDK'yı kullanmaya başlamadan önce geliştirme ortamınızı kurmanız ve gerekli bağımlılıkları yüklemeniz gerekir. Bakınız[makale](https://docs.aspose.cloud/cells/quickstart/) Müşteri kimliğinizi ve müşteri sırrınızı almak için Aspose web sitesini ziyaret edin.

## Aspose.Cells Cloud için PHP paketi nasıl kurulur

PHP için Aspose.Cells Cloud SDK'yı yükleyebilirsiniz. Adımlar aşağıdadır:

- Aspose.Cells Cloud'u `composer.json` dosyanıza bağımlılık olarak ekleyin:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- SDK'yı yüklemek için Composer güncellemesini çalıştırın:

   ```bash

   composer install

   ```

- Composer'ın otomatik yükleyicisini PHP kodunuza ekleyin:

   ```php

   require 'vendor/autoload.php';

   ```

## Xlsx'i PDF'e dönüştürmek için PHP paketi nasıl kullanılır?

- Aspose.Cells Bulut Kitaplığını İçe Aktar
 Gerekli paketi Aspose.Cells Cloud PHP SDK'sından projenize aktararak başlayın.
- API İstemcisini Kimlik Bilgileriyle Yapılandırma
 API istemcinizin kimliğini benzersiz istemci kimliğiniz ve istemci sırrınızla doğrulayın.
- Dönüşüm Parametrelerini Hazırlayın
 Kaynak dosya adı, istenilen çıktı formatı ve depolama klasörü yolu dahil, dönüştürme görevi için parametreleri tanımlayın.
- Çalışma Kitabı Dönüşümünü Yürüt
 PostConvertWorkbook yöntemini kullanarak dönüştürme işlemini çağırın ve yanıtı işleyin.

```PHP
<?php
require_once('vendor\autoload.php');
use \Aspose\Cells\Cloud\Api\CellsApi;
use \Aspose\Cells\Cloud\Request\PutConvertWorkbookRequest;

$cellsApi = new CellsApi(getenv("CellsCloudClientId"),getenv("CellsCloudClientSecret"),"v3.0",getenv("CellsCloudApiBaseUrl"));

$remoteFolder = "TestData/In";

$localName = "Book1.xlsx";
$remoteName = "Book1.xlsx";

$format = "csv";

$mapFiles = array ();
$mapFiles[$localName] = CellsApiTestBase::getfullfilename($localName);
CellsApiTestBase::ready(  $this->instance,$localName ,$remoteFolder . "/" . $remoteName ,  "");
 
$request = new PutConvertWorkbookRequest();
$request->setFile( $mapFiles);
$request->setFormat( $format);
$$cellsApi->putConvertWorkbook($request);
```
