---
title: "Aspose.Cells Cloud Web API — Получение состояния Aspose.Cells Cloud"
second_title: "Документ"
ArticleTitle: "Получение состояния Aspose.Cells Cloud"
linktitle: "Получение состояния Aspose.Cells Cloud"
type: docs
url: /ru/get-aspose-cells-cloud-status/
keywords: "Aspose.Cells, Cloud API, проверка работоспособности, Excel, REST"
description: "Мониторинг состояния работоспособности службы Aspose.Cells Cloud в режиме реального времени."
weight: 100
---

Получение состояния работоспособности службы Aspose.Cells Cloud в режиме реального времени.

**Необходимые условия:** Для вызова этого API необходимо получить токен доступа Bearer, используя учетные данные клиента Aspose Cloud. Включите токен в заголовок `Authorization` в формате `Bearer {access_token}`.

## **Получение состояния Aspose.Cells Cloud**

### **Web API**

Конечная точка использует метод HTTP **GET** и не требует тела запроса.

```
GET https://api.aspose.cloud/v4.0/cells
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Параметры запроса:**

| Имя параметра | Тип   | Путь/Строка запроса/Тело HTTP-запроса | Описание                                |
| ------------- | ----- | ------------------------------------- | --------------------------------------- |
| Authorization | Строка | Заголовок                             | Bearer-токен для аутентификации (обязательный). |
| format        | Строка | Параметр запроса                      | Желаемый формат ответа, например `json`. |

### **Ответ**

```json
{
  "status": "OK",
  "service": "Aspose.Cells Cloud",
  "timestamp": "2026-07-06T12:34:56Z"
}
```

**Схема ответа**

| Поле      | Тип                | Описание                               |
| --------- | ------------------ | -------------------------------------- |
| status    | string             | Состояние сервиса (`OK`, `Degraded` и т.д.). |
| service   | string             | Имя сервиса.                           |
| timestamp | string (ISO‑8601)  | Время выполнения проверки состояния.   |

API возвращает стандартный JSON-ответ, содержащий текущее состояние работоспособности службы Aspose.Cells Cloud.

**Коды HTTP-статуса**

- **200 OK** — Сервис работоспособен, ответ содержит информацию о состоянии.
- **401 Unauthorized** — Отсутствует или недействителен токен аутентификации.
- **503 Service Unavailable** — Сервис временно недоступен (например, в режиме обслуживания или при возникновении проблем).

## Как использовать API получения состояния Aspose.Cells Cloud с помощью SDK

### Спецификация OpenAPI

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/CellsStatusController/GetAsposeCellsCloudStatus) определяет общедоступное программное интерфейсное описание, позволяющее выполнять REST-взаимодействия непосредственно из веб-браузера.

### Использование SDK Aspose.Cells Cloud

Использование SDK упрощает интеграцию и снижает объем шаблонного кода. SDK обрабатывает все низкоуровневые детали, позволяя получить состояние работы Aspose.Cells Cloud с минимальными усилиями. Ознакомьтесь со [страницей репозитория на GitHub](https://github.com/aspose-cells-cloud), чтобы увидеть полный список SDK Aspose.Cells Cloud.