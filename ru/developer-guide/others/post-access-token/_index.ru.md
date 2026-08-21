---
---
title: "Aspose.Cells Cloud Web API — POST /access token"
second_title: "Документ"
ArticleTitle: "Получение токена доступа с помощью Client ID и Secret"
linktitle: "POST /access token"
type: docs
url: /post-access-token/
keywords: "Aspose.Cells, облако, токен доступа, OAuth2, API, аутентификация, REST, Excel, Office Cloud"
description: "Получите токен доступа OAuth2 для Aspose.Cells Cloud, вызвав конечную точку POST /cells/connect/token с вашим Client ID и secret."
weight: 100
---

Получите токен доступа с помощью API Cells Cloud Get Token, используя Client ID и secret.

## API POST /access token

Перед вызовом конечной точки убедитесь, что у вас есть:

* Зарегистрированная учетная запись Aspose Cloud.  
* **Client ID** и **Client Secret**, сгенерированные в портале Aspose Cloud.  

### Web API

```
POST https://api.aspose.cloud/v4.0/cells/connect/token
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип   | Расположение              | Описание                                            |
| ------------- | ----- | ------------------------- | --------------------------------------------------- |
| grant_type    | string | тело (form‑url‑encoded)   | Фиксированное значение `client_credentials`, необходимое для OAuth. |
| client_id     | string | тело (form‑url‑encoded)   | Идентификатор клиента, выданный вам.                |
| client_secret | string | тело (form‑url‑encoded)   | Секретный ключ, связанный с Client ID.              |

**Пример запроса (cURL)**  

```bash
curl -X POST "https://api.aspose.cloud/v4.0/cells/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET"
```

### Ответ

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                           |
|-----|-----------------------------|----------------------------------------------------|
| 200 | OK (ОК)                    | Фильтр успешно применен; ответ содержит детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован) | Неверный или отсутствующий JWT-токен.              |
| 413 | Payload Too Large (Слишком большой payload) | Загруженный файл превышает лимит размера.         |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                    |

**Пример обработки ошибок**

```json
{
  "error": "invalid_client",
  "error_description": "Ошибка аутентификации клиента."
}
```

## Как использовать API Get public key с SDK

### Спецификация OpenAPI

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) определяет публично доступное программное интерфейсное описание, позволяющее выполнять REST-взаимодействия непосредственно из веб-браузера.

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ начать работу. SDK абстрагирует низкоуровневые HTTP-детали, позволяя получить токен доступа для Cells с минимальным количеством кода.

Ознакомьтесь с [репозиторием на GitHub](https://github.com/aspose-cells-cloud), чтобы увидеть полный список SDK Aspose.Cells Cloud. SDK берет на себя обработку низкоуровневых деталей, позволяя вам сосредоточиться на задачах вашего проекта.

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с помощью различных SDK:
---