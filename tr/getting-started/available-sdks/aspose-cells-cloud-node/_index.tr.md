---
title: "Aspose.Cells Cloud SDK for Node.js: Dönüştür, birleştir, böl, koru, ara, değiştir ve daha fazlası."
second_title: "Belge"
ArticleTitle: "Aspose.Cells Cloud SDK for Node.js: Dönüştür, birleştir, böl, koru, ara, değiştir ve daha fazlası."
linktype: "Aspose.Cells Cloud SDK for Node.js"
type: docs
url: /tr/available-sdks/aspose-cells-cloud-node/
description: "Aspose.Cells Cloud SDK for Node.js, gerçek platformlar arası gücünü sunar: tek bir içe aktarma, Windows, Linux ve macOS geliştiricilerine aynı akıcı API’yi sağlar; böylece her Excel nesnesini oluşturabilir, dönüştürebilir, birleştirebilir, bölebilir, koruyabilir ve işlem yapabilir—Office kurulumuna gerek yoktur ve platforma özel ayarlara da ihtiyaç duyulmaz."
weight: 30
kwords: Node.js, Node.js SDK, Node.js için Excel SDK’sı, Node.js için Bulut SDK’sı, REST, Grafik, Pivot Tablo, Tablo/Liste Nesnesi, Elektronik Tabloyu Dönüştür, PDF, CSV, JSON, Markdown, Birleştir, Böl, Koru, Ara, Değiştir
---

SDK açık kaynaklıdır ve MIT Lisansı altında lisanslanmıştır. Aspose.Cells Cloud için Node kütüphanesi kaynak koduna [buradan](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) ulaşabilirsiniz.

# **Aspose.Cells Cloud Node kütüphanesi nasıl kullanılır**

Aspose.Cells Cloud SDK for Node, geliştiricilerin Microsoft Excel dosyalarını Node programlama dili kullanarak işlemesini ve işlemesini sağlayan güçlü bir kütüphanedir. Bu SDK ile yerel makinenize ek yazılım veya bağımlılıklar kurmadan Excel belgelerini bulutta oluşturabilir, düzenleyebilir ve dönüştürebilirsiniz.

Bu makalede, Aspose.Cells Cloud SDK for Node ile bazı yaygın görevleri nasıl gerçekleştireceğimizi inceleyeceğiz: yeni bir Excel çalışma kitabının oluşturulması, hücrelere veri eklenmesi ve değiştirilen çalışma kitabının buluta kaydedilmesi gibi.

## Başlarken

Aspose.Cells Cloud SDK for Go kullanmaya başlamadan önce geliştirme ortamınızı kurmanız ve gerekli bağımlılıkları yüklemeniz gerekir. İstemci kimliğinizi ve istemci sırrınızı almak için Aspose web sitesindeki [bu makaleye](https://docs.aspose.cloud/cells/quickstart/) bakın.

## Aspose.Cells Cloud için Node paketi nasıl yüklenir

Aspose.Cells Cloud SDK for Node’u npm ile yükleyebilirsiniz. Aşağıda npm için adımlar verilmiştir:

```Powershell

npm install asposecellscloud

```

## Aspose.Cells Cloud için paket yapılandırmasında bağımlılıklar nasıl eklenir

node yapılandırma dosyası: package.json

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

## Node paketi ile Xlsx dosyasını diğer formatlara nasıl dönüştürülür

- Aspose.Cells Cloud Kütüphanesini İçe Aktarın  
  Öncelikle projenize Aspose.Cells Cloud NodeJS SDK’sından gerekli paketi içe aktarın.
- Kimlik Bilgileriyle API İstemcisi Yapılandırın  
  API istemcinizi benzersiz istemci kimliğiniz ve istemci sırrınızla doğrulayın.
- Dönüştürme Parametrelerini Hazırlayın  
  Dönüştürme görevi için kaynak dosya adı, istenen çıktı formatı ve depolama klasörü yolu dahil parametreleri tanımlayın.
- Çalışma Kitabı Dönüştürmeyi Gerçekleştirin  
  PostConvertWorkbook yöntemini kullanarak dönüştürme işlemini çağırın ve yanıtı işleyin.

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}