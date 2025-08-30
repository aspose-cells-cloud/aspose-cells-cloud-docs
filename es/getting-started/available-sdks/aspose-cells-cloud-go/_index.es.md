---
title: Aspose.Cells SDK de nube para G
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/available-sdks/aspose-cells-cloud-go/
description: El SDK de nube Aspose.Cells para Go ofrece una sólida compatibilidad multiplataforma para desarrolladores de Go, lo que facilita su integración y uso en Windows, Linux o macOS. Admite Excel para crear, convertir, fusionar, dividir, proteger, realizar operaciones con objetos internos, etc.
weight: 30
kwords: Go, Excel, Office Nube, REST API, Gráfico, Tabla dinámica, Tabla, Hoja de cálculo, PDF, CSV, JSON, Markdown
---
 El SDK es de código abierto y está licenciado bajo la licencia MIT. Puede acceder al código fuente de la biblioteca Go para Aspose.Cells Cloud.[aquí](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go).

# **Cómo utilizar la biblioteca Go de Aspose.Cells Cloud**

El SDK de nube Aspose.Cells para Go es una potente biblioteca que permite a los desarrolladores manipular y procesar archivos Microsoft y Excel mediante el lenguaje de programación Go. Con este SDK, puede crear, editar y convertir documentos Excel en la nube, sin necesidad de instalar software adicional ni dependencias en su equipo local.

En este artículo, exploraremos cómo usar Aspose.Cells Cloud SDK para Go para realizar algunas tareas comunes, como crear un nuevo libro de trabajo Excel, insertar datos en celdas y guardar el libro de trabajo modificado en la nube.

## **Empezando**

 Antes de empezar a usar el SDK de nube Aspose.Cells para Go, debe configurar su entorno de desarrollo e instalar las dependencias necesarias. Consulte[el artículo](https://docs.aspose.cloud/cells/quickstart/) en el sitio web Aspose para obtener su ID de cliente y secreto de cliente.

## Cómo instalar el paquete Go para Aspose.Cells Cloud

Puede instalar el SDK de nube Aspose.Cells para Go con el comando `go get`. Abra su terminal o símbolo del sistema y ejecute el siguiente comando:

```bash
go install github.com/aspose-cells-cloud/aspose-cells-cloud-go@latest
```

Esto descargará e instalará la última versión del SDK en su espacio de trabajo de Go.

## Cómo importar la biblioteca Go a tu proyecto

```golang
package main

import (
 . "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25"
)
```

## Cómo comenzar a usar Aspose.Cells Cloud for Go, siga estos pasos

- Crea una cuenta en Aspose para Cloud y obtén el ID y el secreto de tu cliente de aplicación.
- Crea un directorio para tu proyecto y un archivo main.go dentro. Agrega el siguiente código a tu archivo main.go.

### **Código de muestra**

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_AvailableSDKs.go" >}}

- Inicialice el proyecto go.mod, obtenga las dependencias para su proyecto y ejecute la aplicación creada.

```bash
go mod init main
go mod tidy
go run main.go

```
