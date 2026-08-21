---
title: "Скрытие легенды диаграммы в рабочей книге Excel – Aspose.Cells Cloud API"
type: docs
url: /charts/legend/hide/
aliases: [/hide-chart-legend-in-a-worksheet/]
weight: 110
keywords: "Aspose.Cells, Excel, скрытие легенды диаграммы, REST API, облачное SDK, легенда диаграммы"
description: "Узнайте, как скрыть легенду диаграммы в рабочей книге Excel с помощью Aspose.Cells Cloud REST API. Включает HTTPS-эндпоинт, необходимую аутентификацию, синтаксис запроса, детали ответа, обработку ошибок и примеры SDK."
---

Этот REST API скрывает легенду диаграммы. **Легенда диаграммы** — это прямоугольная область, содержащая идентификаторы рядов данных, отображаемых на диаграмме.

API требует действительного JWT-токена Aspose Cloud, рабочая книга должна быть загружена в облачное хранилище Aspose Cloud, а используемая версия API — **v3.0**.

## Безопасность и аутентификация  
Aspose.Cells Cloud API защищены и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### Параметры запроса

| Имя параметра   | Тип    | Расположение | Описание                         |
| --------------- | ------ | ------------ | -------------------------------- |
| **name**        | string | path         | Имя рабочей книги.               |
| **sheetName**   | string | path         | Имя рабочего листа.              |
| **chartIndex**  | integer| path         | Индекс диаграммы.                |
| **folder**      | string | query        | Папка рабочей книги (необязательно). |
| **storageName** | string | query        | Имя хранилища (необязательно).   |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartLegend) определяет данный публично доступный программный интерфейс.

Вы можете легко вызывать API с помощью утилиты командной строки cURL. Пример ниже демонстрирует запрос на скрытие легенды диаграммы с индексом 0 в файле _Sample_Test_Book.xls_.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Ответы

| HTTP-статус                   | Описание                                              | Пример JSON                                                   |
| ----------------------------- | ----------------------------------------------------- | ------------------------------------------------------------- |
| **200 OK**                    | Легенда успешно скрыта.                               | `{ "Code": 200, "Status": "OK" }`                             |
| **401 Unauthorized**          | Отсутствует или недействителен JWT-токен.            | `{ "Code": 401, "Message": "Invalid access token." }`         |
| **404 Not Found**             | Рабочая книга, рабочий лист или диаграмма не найдены.| `{ "Code": 404, "Message": "Chart not found." }`              |
| **500 Internal Server Error** | Непредвиденная ошибка сервера.                        | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## Часто задаваемые вопросы

**В:** _Как скрыть легенду диаграммы с помощью Aspose.Cells Cloud?_  
**О:** Отправьте `DELETE`-запрос по адресу `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend`, указав действительный JWT-токен в заголовке `Authorization`. Ответ `200 OK` означает успешное выполнение.

**В:** _Какая аутентификация требуется для API скрытия легенды диаграммы?_  
**О:** Укажите заголовок `Authorization: Bearer <jwt token>`. Получите токен с помощью OAuth-процедуры Aspose Cloud.

**В:** _Какой ответ об ошибке будет возвращён, если индекс диаграммы недопустим?_  
**О:** Сервис вернёт `404 Not Found` с телом JSON, содержащим `Code: 404` и сообщение о том, что диаграмма не найдена.

**В:** _Можно ли использовать HTTP вместо HTTPS?_  
**О:** Нет. Все эндпоинты Aspose Cloud требуют HTTPS для обеспечения безопасности.

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-HideChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_legend_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "HideChartLegendInWorkSheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-HideChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
**Скоро** – пример Swift SDK будет добавлен в ближайшее время.  
{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-HideChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3eb15aa10e3d2cd8931e60f8d001fd1c" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "name": "Скрытие легенды диаграммы в рабочей книге Excel – Aspose.Cells Cloud API",
  "description": "Пошаговое руководство по скрытию легенды диаграммы в рабочей книге Excel с помощью Aspose.Cells Cloud REST API. Включает HTTPS-эндпоинт, аутентификацию, синтаксис запроса, детали ответа, обработку ошибок и примеры SDK.",
  "breadcrumb": {
    "@type": "BreadcrumbList",
    "itemListElement": [
      { "@type": "ListItem", "position": 1, "name": "Главная", "item": "https://docs.aspose.cloud/" },
      { "@type": "ListItem", "position": 2, "name": "Cells", "item": "https://docs.aspose.cloud/cells/" },
      { "@type": "ListItem", "position": 3, "name": "Диаграммы", "item": "https://docs.aspose.cloud/cells/charts/" },
      { "@type": "ListItem", "position": 4, "name": "Скрытие легенды диаграммы", "item": "https://docs.aspose.cloud/cells/charts/legend/hide/" }
    ]
  },
  "about": "Скрытие легенды диаграммы с помощью Aspose.Cells Cloud API"
}
</script>