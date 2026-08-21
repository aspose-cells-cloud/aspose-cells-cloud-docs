---
title: "Шифрование, расшифровка и цифровая подпись файлов Excel"
second_title: "Документ"
linktype: "Защита Excel"
type: docs
url: /ru/protect/
aliases: [  /ru/workbook/password/ ]
keywords: "Excel, защита, шифрование, расшифровка, цифровая подпись, Aspose.Cells Cloud, REST API, пароль, безопасность"
description: "Узнайте, как защищать, шифровать, расшифровывать и ставить цифровую подпись на рабочих книгах Excel с помощью Aspose.Cells Cloud REST API — примеры кода для Android, C#, Java, Python и других."
ArticleTitle: "Шифрование, расшифровка, цифровая подпись и защита файлов Excel с помощью API Aspose.Cells Cloud"
weight: 36
---

## **Защита и снятие защиты файлов Excel**

**Что такое «защита» в Aspose.Cells Cloud?**  
Операция **Protect** защищает рабочую книгу Excel, применяя пароль, который ограничивает возможность открытия, редактирования или изменения структуры файла. API также поддерживает шифрование и расшифровку рабочей книги, а также добавление цифровой подписи для проверки целостности данных.

**Справочник по API**  

| Метод HTTP | Конечная точка | Обязательные параметры запроса / тела | Пример тела запроса | Типичные ответы |
|------------|----------------|----------------------------------------|----------------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/protect` | `fileName` (путь), `password` (параметр запроса) | `{ "password": "MySecret123" }` | `200 OK` — защита применена, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error` |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/unprotect` | `fileName` (путь), `password` (параметр запроса) | N/A | `200 OK` — защита снята, коды ошибок, как указано выше |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/encrypt` | `fileName` (путь), `password` (параметр запроса) | N/A | `200 OK` — файл зашифрован |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/decrypt` | `fileName` (путь), `password` (параметр запроса) | N/A | `200 OK` — файл расшифрован |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/sign` | `fileName` (путь) | `{ "certificatePath": "/certs/mycert.pfx", "certificatePassword": "certPass" }` | `200 OK` — цифровая подпись добавлена |

**Пример кода (C#)**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Инициализация клиента API
var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY",
    BaseUrl = "https://api.aspose.cloud"
};
var api = new CellsApi(config);

// Защита рабочей книги
var protectRequest = new PostProtectWorkbookRequest(
    name: "Sample.xlsx",
    password: "MySecret123"
);
api.PostProtectWorkbook(protectRequest);
```

**Необходимые условия**  
- Активная подписка на Aspose.Cells Cloud.  
- `AppSid` и `AppKey` для аутентификации.  

**Аутентификация**  
Все запросы должны включать заголовок `Authorization` с действительным токеном JWT, полученным из точки аутентификации Aspose Cloud.

**Обработка ошибок**  
Проверьте HTTP-код состояния и объект `Error`, возвращаемый в теле ответа. Типичные ошибки включают недопустимый пароль (`400`), отсутствующий файл (`404`) и сбои аутентификации (`401`).

**Примечания**  
- Ту же самую конечную точку можно использовать для **шифрования** или **расшифровки**, изменив сегмент действия (`/encrypt`, `/decrypt`).  
- Для добавления цифровой подписи требуется действующий файл сертификата, доступный для API.

- [Шифрование файла Excel с помощью API Aspose.Cells Cloud](/cells/excel-file-encrypt/)
- [Защита файла Excel с помощью API Aspose.Cells Cloud](/cells/protect-excel-file/)
- [Добавление цифровой подписи к файлу Excel](/cells/excel-digital-signature/)
- [Защита файлов Excel — подробное руководство](/cells/protect-excel-files/)
- [Установка пароля для файла Excel](/cells/workbook/password/modify/)
- [Расшифровка файла Excel](/cells/excel-file-decrypt/)
- [Снятие защиты с файла Excel](/cells/excel-file-unprotect/)
- [Разблокировка файлов Excel](/cells/unlock-excel-files/)
- [Очистка пароля файла Excel](/cells/clear-excel-files-password/)