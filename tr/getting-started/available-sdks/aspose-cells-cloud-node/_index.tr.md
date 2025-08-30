---
title: Aspose.Cells Nod için Bulut SDK'sı
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/available-sdks/aspose-cells-cloud-node/
description: Aspose.Cells Bulut, Excel'in oluşturma, dönüştürme, birleştirme, bölme, korumalı, iç nesne işlemleri vb. işlemlerini destekler
weight: 30
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, Düğüm
---
 SDK açık kaynaklıdır ve MIT Lisansı kapsamında lisanslanmıştır. Aspose.Cells Cloud için Node kütüphanesi kaynak koduna erişebilirsiniz.[Burada](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

# **Aspose.Cells Cloud'un Node kütüphanesi nasıl kullanılır?**

Node için Aspose.Cells Cloud SDK, geliştiricilerin Node programlama dilini kullanarak Microsoft Excel dosyalarını düzenlemelerine ve işlemelerine olanak tanıyan güçlü bir kütüphanedir. Bu SDK ile, yerel makinenize ek yazılım veya bağımlılıklar yüklemeden bulutta Excel belgeleri oluşturabilir, düzenleyebilir ve dönüştürebilirsiniz.

Bu makalede, yeni bir Excel çalışma kitabı oluşturma, hücrelere veri ekleme ve değiştirilen çalışma kitabını buluta kaydetme gibi bazı genel görevleri gerçekleştirmek için Aspose.Cells Cloud SDK'nın Node için nasıl kullanılacağını inceleyeceğiz.

## Başlarken

 Aspose.Cells Cloud SDK for Go'yu kullanmaya başlamadan önce, geliştirme ortamınızı ayarlamanız ve gerekli bağımlılıkları yüklemeniz gerekir. Bkz.[makale](https://docs.aspose.cloud/cells/quickstart/) Müşteri ID'nizi ve müşteri sırrınızı almak için Aspose web sitesini ziyaret edin.

## Aspose.Cells Cloud için Node paketi nasıl kurulur?

Aspose.Cells Cloud SDK'yı Node için npm kullanarak yükleyebilirsiniz. Aşağıda npm için adımlar yer almaktadır:

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

## Xlsx'i diğer formatlara dönüştürmek için Node paketi nasıl kullanılır?

- Aspose.Cells Bulut Kütüphanesini İçe Aktar
 Öncelikle Aspose.Cells Cloud NodeJS SDK'sından gerekli paketi projenize aktarın.
- API İstemcisini Kimlik Bilgileriyle Yapılandırın
 API istemcinizi benzersiz istemci kimliğiniz ve istemci sırrınızla doğrulayın.
- Dönüştürme Parametrelerini Hazırla
 Kaynak dosya adı, istenen çıktı biçimi ve depolama klasörü yolu dahil olmak üzere dönüştürme görevi için parametreleri tanımlayın.
- Çalışma Kitabı Dönüşümünü Çalıştır
 Dönüştürme işlemini PostConvertWorkbook metodunu kullanarak çağırın ve yanıtı işleyin.

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}
