---
title: Aspose.Cells Облачный SDK для Jav
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/available-sdks/aspose-cells-cloud-java/
description: Aspose.Cells Облако поддерживает Excel для создания, преобразования, слияния, разделения, защиты, внутренних операций с объектами и т. д.
weight: 30
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Java
---
SDK имеет открытый исходный код и распространяется по лицензии MIT. Вы можете получить доступ к исходному коду библиотеки Java для облачного сервиса Aspose.Cells.[здесь](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java).

# **Как использовать библиотеку Java облака Aspose.Cells**

Облачный SDK Aspose.Cells for Java — это мощная библиотека, позволяющая разработчикам обрабатывать файлы Microsoft Excel с помощью языка программирования Java. С помощью этого SDK вы можете создавать, редактировать и конвертировать документы Excel в облаке, не устанавливая дополнительное программное обеспечение или зависимости на локальный компьютер.

В этой статье мы рассмотрим, как использовать Aspose.Cells Cloud SDK for Java для выполнения некоторых распространенных задач, таких как создание новой книги Excel, вставка данных в ячейки и сохранение измененной книги в облаке.

## Начиная

 Прежде чем начать использовать Cloud SDK Aspose.Cells для Go, необходимо настроить среду разработки и установить необходимые зависимости. См.[статья](https://docs.aspose.cloud/cells/quickstart/) на сайте Aspose, чтобы получить свой идентификатор клиента и секретный код клиента.

## Как использовать Maven для добавления зависимостей для облака Aspose.Cells

В вашем проекте Maven добавьте зависимости для Cloud SDK Aspose.Cells. Включите следующие зависимости в файл pom.xml:

**Aspose Maven Репозиторий**

```java

<repositories>
    <repository>
        <id>aspose-cloud-repository</id>
        <name>Aspose Cloud Repository</name>
        <url>https://repository.aspose.cloud/repo/</url>
    </repository>
</repositories>

```

**Maven Зависимость**

```java

<dependency>
      <groupId>com.aspose</groupId>
      <artifactId>aspose-cloud-cells</artifactId>
      <version>24.5</version>
</dependency>

```

## Как использовать пакет Java для преобразования Xlsx в PDF

- Импорт Aspose.Cells Облачная библиотека
 Начните с импорта необходимого пакета из Aspose.Cells Cloud Java SDK в ваш проект.
- Настройте клиента API с учетными данными
 Авторизуйте своего клиента API, используя свой уникальный идентификатор клиента и секретный код клиента.
- Подготовить параметры преобразования
 Определите параметры задачи преобразования, включая имя исходного файла, желаемый выходной формат и путь к папке хранения.
- Выполнить преобразование рабочей книги
 Вызовите процесс преобразования с помощью метода PostConvertWorkbook и обработайте ответ.

### **Пример кода**

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_AvailableSDKs.java" >}}
