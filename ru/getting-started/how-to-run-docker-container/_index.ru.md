---
title: Как запустить Docker-контейнер
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: Как запустить Docker Aspose.Cells Облачный контейнер. Aspose.Cells Облако поддерживает Excel для создания, преобразования, объединения, разделения, защиты, операций с внутренними объектами и т. д.
weight: 100
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdwon, Как запустить Docker-контейнер
---
**Докер**Технология предназначена для автоматизации развертывания приложений с помощью легких контейнеров. Разработчики могут использовать**Докер-контейнер** чтобы обернуть приложение со всеми его библиотеками и зависимостями и развернуть все как один пакет.

 Aspose.Cells Команда Cloud опубликовала Docker-контейнер на[Докер-Хаб](https://hub.docker.com/r/aspose/cells-cloud) для облегчения пользователей Docker. В следующих разделах вы узнаете, как запускать команды Docker или записывать конфигурацию в файле Yaml для инструмента создания Docker.

## Конфигурация контейнера

### Требуемые объемы

|Путь монтирования в контейнере|Описание|
|:- |:- |
|C:\шрифты|Папка со шрифтами, которые будут использоваться для рендеринга документов|
|С:\данные|Папка для хранения файлов|

### Параметры

|Имя|Описание|
|:- |:- |
|ЛицензияPublicKey|Открытый ключ лицензии|
|ЛицензияPrivateKey|Закрытый ключ лицензии|


Если параметры «Лицензия» опущены, приложение будет работать в пробном режиме.


### Запустите контейнер Docker с помощью командной строки

Вы можете просто запустить следующую команду Docker после извлечения контейнера из[Докер-Хаб](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```

### Конфигурации для инструмента Docker-Compose

Вы можете записать следующие конфигурации в свой yaml-файл для инструмента Docker-Compose:

```JAVA
AsposeCellsCloud:
      image: aspose/cells-cloud
      ports: ["5000:80"]
      volumes: [
        "C:/Windows/Fonts:C:/Windows/Fonts",
        "c:/data:c:/data",
      ]
      environment:
        "LicensePublicKey": "yourKeyHere"
        "LicensePrivateKey": "yourKeyHere"
```
