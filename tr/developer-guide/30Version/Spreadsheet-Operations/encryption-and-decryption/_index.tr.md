---
title: "Excel Dosyalarını Şifreleyin, Şifresini Çözün ve Dijital Olarak İmzalayın"
second_title: "Belge"
linktype: "Koruma"
type: docs
url: /tr/protect/
aliases: [/tr/workbook/password/]
keywords: "Excel, koruma, şifreleme, şifre çözme, dijital imza, Aspose.Cells Cloud, REST API, şifre, güvenlik"
description: "Aspose.Cells Cloud REST API ile Excel çalışma kitaplarını nasıl koruyacağınıza, şifreleyip şifresini çözeceğinize ve dijital imza ekleyeceğinize ilişkin bilgileri öğrenin – Android, C#, Java, Python ve daha fazlası için kod örnekleri."
ArticleTitle: "Aspose.Cells Cloud API kullanarak Excel Dosyalarını Şifreleyin, Şifresini Çözün, Dijital Olarak İmzalayın ve Koruyun"
weight: 36
---

## **Excel Dosyalarını Koruma ve Korumayı Kaldırma**

**Aspose.Cells Cloud’da “koruma” nedir?**  
**Koruma** işlemi, bir Excel çalışma kitabını bir parola uygulayarak korur; bu parola sayesinde dosyanın açılması, düzenlenmesi veya yapısının değiştirilmesi kısıtlanır. API ayrıca çalışma kitabının şifrelenmesini, şifresinin çözülmesini ve sahteciliğe karşı koruyucu doğrulama için dijital imza eklemeyi destekler.

**API Referansı**  

| HTTP Yöntemi | Uç Nokta | Gerekli sorgu / gövde parametreleri | Örnek istek gövdesi | Tipik yanıt kodları |
|-------------|----------|-----------------------------------|---------------------|-------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/protect` | `fileName` (yol), `password` (sorgu) | `{ "password": "MySecret123" }` | `200 OK` – koruma uygulandı, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error` |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/unprotect` | `fileName` (yol), `password` (sorgu) | Yok | `200 OK` – koruma kaldırıldı, yukarıdaki hata kodları |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/encrypt` | `fileName` (yol), `password` (sorgu) | Yok | `200 OK` – dosya şifrelendi |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/decrypt` | `fileName` (yol), `password` (sorgu) | Yok | `200 OK` – dosyanın şifresi çözüldü |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/sign` | `fileName` (yol) | `{ "certificatePath": "/certs/mycert.pfx", "certificatePassword": "certPass" }` | `200 OK` – dijital imza eklendi |

**Kod Örneği (C#)**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// API istemcisini başlat
var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY",
    BaseUrl = "https://api.aspose.cloud"
};
var api = new CellsApi(config);

// Çalışma kitabını koru
var protectRequest = new PostProtectWorkbookRequest(
    name: "Sample.xlsx",
    password: "MySecret123"
);
api.PostProtectWorkbook(protectRequest);
```

**Ön Gereksinimler**  
- Aktif bir Aspose.Cells Cloud aboneliği.  
- Kimlik doğrulama için `AppSid` ve `AppKey`.  

**Kimlik Doğrulama**  
Tüm isteklerde, Aspose Cloud kimlik doğrulama uç noktasından alınan geçerli bir JWT belirteci içeren `Authorization` başlığı yer almalıdır.

**Hata Yönetimi**  
HTTP durum kodunu ve yanıt gövdesinde döndürülen `Error` nesnesini kontrol edin. Yaygın hatalar arasında geçersiz şifre (`400`), eksik dosya (`404`) ve kimlik doğrulama hataları (`401`) yer alır.

**Notlar**  
- Aynı uç nokta, eylem segmentini değiştirerek (`/encrypt`, `/decrypt`) **şifrelemek** veya **şifresini çözmek** için kullanılabilir.  
- Dijital imzalar, API’nin erişebildiği geçerli bir sertifika dosyası gerektirir.

- [Excel dosyasını Aspose.Cells Cloud API ile şifreleyin](/tr/cells/excel-file-encrypt/)
- [Excel dosyasını Aspose.Cells Cloud API ile koruyun](/tr/cells/protect-excel-file/)
- [Excel dosyasına dijital imza ekleyin](/tr/cells/excel-digital-signature/)
- [Excel dosyalarını koruma – ayrıntılı kılavuz](/tr/cells/protect-excel-files/)
- [Excel dosyası için bir şifre belirleyin](/tr/cells/workbook/password/modify/)
- [Excel dosyasının şifresini çözün](/tr/cells/excel-file-decrypt/)
- [Excel dosyasının korumasını kaldırın](/tr/cells/excel-file-unprotect/)
- [Excel dosyalarının kilidini açın](/tr/cells/unlock-excel-files/)
- [Excel dosyasının şifresini temizleyin](/tr/cells/clear-excel-files-password/)
---