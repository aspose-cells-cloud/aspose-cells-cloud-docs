---
title: Aspose.Cells Per için Bulut SDK'sı
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/available-sdks/aspose-cells-cloud-perl/
description: Aspose.Cells Bulut, Excel'in oluşturma, dönüştürme, birleştirme, bölme, korumalı, iç nesne işlemleri vb. işlemlerini destekler
weight: 30
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, Perl
---
SDK açık kaynaklıdır ve MIT Lisansı kapsamında lisanslanmıştır. Aspose.Cells Cloud için Perl kütüphane kaynak koduna erişebilirsiniz.[Burada](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl).

# **Aspose.Cells Cloud'un Perl kütüphanesi nasıl kullanılır?**

Perl için Aspose.Cells Cloud SDK, geliştiricilerin Perl programlama dilini kullanarak Microsoft Excel dosyalarını düzenlemelerine ve işlemelerine olanak tanıyan güçlü bir kütüphanedir. Bu SDK ile, yerel makinenize ek yazılım veya bağımlılıklar yüklemeden bulutta Excel belgeleri oluşturabilir, düzenleyebilir ve dönüştürebilirsiniz.

Bu makalede, Perl için Aspose.Cells Cloud SDK'nın yeni bir Excel çalışma kitabı oluşturma, hücrelere veri ekleme ve değiştirilen çalışma kitabını buluta kaydetme gibi bazı genel görevleri gerçekleştirmek için nasıl kullanılacağını inceleyeceğiz.

## Başlarken

 Aspose.Cells Cloud SDK for Go'yu kullanmaya başlamadan önce, geliştirme ortamınızı ayarlamanız ve gerekli bağımlılıkları yüklemeniz gerekir. Bkz.[makale](https://docs.aspose.cloud/cells/quickstart/) Müşteri ID'nizi ve müşteri sırrınızı almak için Aspose web sitesini ziyaret edin.

## Aspose.Cells Cloud için Perl paketi nasıl kurulur?

Aşağıdaki komutla Perl için Aspose.Cells Cloud SDK'yı kurabilirsiniz:

```Powershell

perl -MCPAN -e shell

install AsposeCellsCloud::CellsApi

```

## Xlsx'i diğer formatlara dönüştürmek için Perl paketi nasıl kullanılır?

- Aspose.Cells Bulut Kütüphanesini İçe Aktar
 Öncelikle Aspose.Cells Cloud Perl SDK'sından gerekli paketi projenize aktararak başlayın.
- API İstemcisini Kimlik Bilgileriyle Yapılandırın
 API istemcinizi benzersiz istemci kimliğiniz ve istemci sırrınızla doğrulayın.
- Dönüştürme Parametrelerini Hazırla
 Kaynak dosya adı, istenen çıktı biçimi ve depolama klasörü yolu dahil olmak üzere dönüştürme görevi için parametreleri tanımlayın.
- Çalışma Kitabı Dönüşümünü Çalıştır
 Dönüştürme işlemini PostConvertWorkbook metodunu kullanarak çağırın ve yanıtı işleyin.

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_AvailableSDKs.pl" >}}
