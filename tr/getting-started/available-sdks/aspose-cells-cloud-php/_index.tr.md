---
title: Aspose.Cells PH için Bulut SDK'sı
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/available-sdks/aspose-cells-cloud-php/
description: Aspose.Cells Bulut, Excel'in oluşturma, dönüştürme, birleştirme, bölme, korumalı, iç nesne işlemleri vb. işlemlerini destekler
weight: 30
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, PHP
---
SDK açık kaynaklıdır ve MIT Lisansı kapsamında lisanslanmıştır. Aspose.Cells Cloud için PHP kütüphane kaynak koduna erişebilirsiniz.[Burada](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

# **PHP için Aspose.Cells Cloud SDK nasıl kullanılır?**

PHP için Aspose.Cells Cloud SDK, geliştiricilerin Go programlama dilini kullanarak Microsoft Excel dosyalarını düzenlemelerine ve işlemelerine olanak tanıyan güçlü bir kütüphanedir. Bu SDK ile, yerel makinenize ek yazılım veya bağımlılıklar yüklemeden bulutta Excel belgeleri oluşturabilir, düzenleyebilir ve dönüştürebilirsiniz.

Bu makalede, PHP için Aspose.Cells Cloud SDK'nın yeni bir Excel çalışma kitabı oluşturma, hücrelere veri ekleme ve değiştirilen çalışma kitabını buluta kaydetme gibi bazı genel görevleri gerçekleştirmek için nasıl kullanılacağını inceleyeceğiz.

## Başlarken

 Aspose.Cells Cloud SDK for Go'yu kullanmaya başlamadan önce, geliştirme ortamınızı ayarlamanız ve gerekli bağımlılıkları yüklemeniz gerekir. Bkz.[makale](https://docs.aspose.cloud/cells/quickstart/) Müşteri ID'nizi ve müşteri sırrınızı almak için Aspose web sitesini ziyaret edin.

## Aspose.Cells Cloud için PHP paketi nasıl kurulur?

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

- PHP kodunuza Composer'ın otomatik yükleyicisini ekleyin:

   ```php

   require 'vendor/autoload.php';

   ```

## Xlsx'i diğer formatlara dönüştürmek için PHP paketi nasıl kullanılır?

- Aspose.Cells Bulut Kütüphanesini İçe Aktar
 Öncelikle Aspose.Cells Cloud PHP SDK'sından gerekli paketi projenize aktararak başlayın.
- API İstemcisini Kimlik Bilgileriyle Yapılandırın
 API istemcinizi benzersiz istemci kimliğiniz ve istemci sırrınızla doğrulayın.
- Dönüştürme Parametrelerini Hazırla
 Kaynak dosya adı, istenen çıktı biçimi ve depolama klasörü yolu dahil olmak üzere dönüştürme görevi için parametreleri tanımlayın.
- Çalışma Kitabı Dönüşümünü Çalıştır
 Dönüştürme işlemini PostConvertWorkbook metodunu kullanarak çağırın ve yanıtı işleyin.

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}
