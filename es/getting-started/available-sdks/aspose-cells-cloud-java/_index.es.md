---
title: "Aspose.Cells Cloud SDK for Java: Convertir, fusionar, dividir, proteger, buscar, reemplazar y más"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud SDK for Java: Convert, merge, split, protect, search, replace, and more"
linktitle: Aspose.Cells SDK de nube para Java
type: docs
url: /es/available-sdks/aspose-cells-cloud-java/
description: "Aspose.Cells Cloud SDK for Java ofrece verdadera potencia multiplataforma: una importación proporciona a los desarrolladores de Windows, Linux y macOS la misma fluidez API para crear, convertir, fusionar, dividir, proteger y manipular cada Excel objeto; no se requiere instalación Office y no se necesitan ajustes específicos de la plataforma"
weight: 30
kwords: Java SDK, Excel SDK for Java, SDK de la nube for Java, REST, Gráfico, Tabla dinámica, Objeto de tabla/lista, Convertir hoja de cálculo, PDF, CSV, JSON, Markdown, Combinar, Dividir, Proteger, Buscar, Reemplazar
---
El SDK es de código abierto y está licenciado bajo la licencia MIT. Puedes acceder a él.[el código fuente de la biblioteca Java para Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java).

# **Cómo utilizar la biblioteca Java de Aspose.Cells Cloud**

El SDK en la nube Aspose.Cells es una potente biblioteca que permite a los desarrolladores manipular y procesar archivos Microsoft y Excel mediante el lenguaje de programación Java. Con este SDK, puede crear, editar y convertir documentos Excel en la nube, sin necesidad de instalar software adicional ni dependencias en su equipo local.

En este artículo, exploraremos cómo usar Aspose.Cells Cloud SDK for Java para realizar algunas tareas comunes, como crear un nuevo libro de trabajo Excel, insertar datos en celdas y guardar el libro de trabajo modificado en la nube.

## Empezando

 Antes de empezar a usar el SDK de nube Aspose.Cells para Go, debe configurar su entorno de desarrollo e instalar las dependencias necesarias. Consulte[el artículo](https://docs.aspose.cloud/cells/quickstart/) en el sitio web Aspose para obtener su ID de cliente y secreto de cliente.

## Cómo usar Maven para agregar dependencias para Aspose.Cells Cloud

En su proyecto Maven, agregue dependencias para el SDK de nube Aspose.Cells. Incluya las siguientes dependencias en el archivo pom.xml:

**Aspose Maven Repositorio**

```java

<repositories>
    <repository>
        <id>aspose-cloud-repository</id>
        <name>Aspose Cloud Repository</name>
        <url>https://repository.aspose.cloud/repo/</url>
    </repository>
</repositories>

```

**Maven Dependencia**

```java

<dependency>
      <groupId>com.aspose</groupId>
      <artifactId>aspose-cloud-cells</artifactId>
      <version>24.5</version>
</dependency>

```

## Cómo usar el paquete Java para convertir XLSX a PDF

- Importación Aspose.Cells Biblioteca en la nube
 Comience importando el paquete necesario del SDK Aspose.Cells Cloud Java a su proyecto.
- Configurar el cliente API con credenciales
 Autentique a su cliente API con su ID de cliente único y su secreto de cliente.
- Preparar parámetros de conversión
 Defina los parámetros para la tarea de conversión, incluido el nombre del archivo de origen, el formato de salida deseado y la ruta de la carpeta de almacenamiento.
- Ejecutar conversión de libro de trabajo
 Invoque el proceso de conversión utilizando el método PostConvertWorkbook y maneje la respuesta.

### **Código de muestra**

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_AvailableSDKs.java" >}}
