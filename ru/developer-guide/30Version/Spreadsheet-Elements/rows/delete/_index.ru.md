---
title: "Работа с удалением строк в листе Excel"
second_title: "Документ"
linktitle: "Удаление"
type: docs
url: /rows/delete/
keywords: "Aspose.Cells, удаление строки, Excel API, REST, облачные технологии, электронная таблица, Excel, SDK"
description: "Узнайте, как удалить одну или несколько строк в листе Excel с использованием Aspose.Cells Cloud REST API. Включает примеры кода для Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby и Swift."
weight: 20
ArticleTitle: "Работа с удалением строк в листе Excel – Руководство по API Aspose.Cells Cloud"
---

## Доступные операции удаления

В следующих примерах показано, как удалить одну пустую строку или несколько строк в листе Excel с использованием Aspose.Cells Cloud REST API.

- [Как удалить пустую строку в листе Excel](/cells/rows/delete/row/)
- [Как удалить несколько строк в листе Excel](/cells/rows/delete/rows/)

**Справочник по API**

| Элемент              | Подробности |
|---------------------|---------------------------------------------------------------|
| **HTTP-метод**      | DELETE |
| **Конечная точка**  | `/cells/{fileName}/worksheets/{sheetName}/rows` |
| **Параметры пути** | `fileName` — имя файла Excel (обязательный)<br>`sheetName` — имя листа (обязательный) |
| **Параметры запроса**| `startrow` — индекс первой удаляемой строки (обязательный)<br>`totalRows` — количество удаляемых строк (обязательный)<br>`storage` — имя облачного хранилища (необязательный)<br>`folder` — путь к папке в хранилище (необязательный) |
| **Тело запроса**    | *Отсутствует* |
| **Пример ответа**   | ```json<br>{<br>  "Code": 200,<br>  "Status": "OK",<br>  "RowsDeleted": 1<br>}<br>``` |
| **Возможные коды состояния**| 200 OK — строки успешно удалены<br>400 Bad Request — неверные параметры<br>401 Unauthorized — ошибка аутентификации<br>404 Not Found — файл или лист не найдены<br>500 Internal Server Error — внутренняя ошибка сервера |

**См. также**

- [Добавление строки](/cells/rows/add/)
- [Получение строки](/cells/rows/get/)
- [Копирование строки](/cells/rows/copy/)
- [Скрытие строки](/cells/rows/hide/)
- [Обзор работы со строками](/cells/rows/)