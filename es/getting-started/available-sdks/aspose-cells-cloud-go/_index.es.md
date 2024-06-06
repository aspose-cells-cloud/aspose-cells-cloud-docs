---
title: Aspose.Cells SDK de nube para G
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/available-sdks/aspose-cells-cloud-go/
description: Aspose.Cells Cloud SDK para Go proporciona un sólido soporte multiplataforma para los desarrolladores de Go, lo que facilita su integración y uso para Windows, Linux o macOS. Admite Excel para crear, convertir, fusionar, dividir, proteger, operaciones de objetos internos, etc.
weight: 30
kwords: Ir, Excel, Office Nube, REST API, Gráfico, Tabla dinámica, Tabla, Hoja de cálculo, PDF, CSV, Json, Markdown
---
 El SDK es de código abierto y tiene la licencia MIT. Puede acceder al código fuente de la biblioteca Go para Aspose.Cells Cloud[aquí](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go).

# **Cómo utilizar la biblioteca Go de Aspose.Cells Cloud**

Aspose.Cells Cloud SDK para Go es una potente biblioteca que permite a los desarrolladores manipular y procesar archivos Microsoft Excel utilizando el lenguaje de programación Go. Con este SDK, puede crear, editar y convertir Excel documentos en la nube, sin instalar software adicional ni dependencias en su máquina local.

En este artículo, exploraremos cómo usar Aspose.Cells Cloud SDK for Go para realizar algunas tareas comunes, como crear un nuevo libro de trabajo Excel, insertar datos en celdas y guardar el libro modificado en la nube.

## **Empezando**

 Antes de poder comenzar a utilizar el SDK de nube Aspose.Cells para Go, debe configurar su entorno de desarrollo e instalar las dependencias necesarias. Referirse a[el artículo](https://docs.aspose.cloud/cells/quickstart/) en el sitio web Aspose para obtener su ID de cliente y su secreto de cliente.

## Cómo instalar el paquete Go para Aspose.Cells Cloud

Puede instalar Aspose.Cells Cloud SDK para Go usando el comando `go get`. Abra su terminal o símbolo del sistema y ejecute el siguiente comando:

```bash
go get -u github.com/aspose-cells-cloud/aspose-cells-cloud-go
```

Esto descargará e instalará la última versión del SDK en su espacio de trabajo de Go.


## Cómo importar la biblioteca Go a su proyecto


```golang
package main

import (
	asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
```

## Cómo utilizar el paquete Go para convertir Xlsx a PDF

- Importar Aspose.Cells Biblioteca en la nube
Comience importando el paquete necesario desde el SDK de Cloud Go Aspose.Cells a su proyecto.
- Configurar el cliente API con credenciales
 Autentique su cliente API con su ID de cliente único y su secreto de cliente.
- Preparar parámetros de conversión
 Defina los parámetros para la tarea de conversión, incluido el nombre del archivo fuente, el formato de salida deseado y la ruta de la carpeta de almacenamiento.
- Ejecutar conversión de libro de trabajo
 Invoque el proceso de conversión utilizando el método PostConvertWorkbook y maneje la respuesta.

### **Código de muestra**

```golang
package main

import (
	"os"
	asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
func main() {
	instance := asposecellscloud.NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"), "https://api.aspose.cloud", "v3.0")
    remoteFolder := "TestData/In"

    localName := "Book1.xlsx"
    remoteName := "Book1.xlsx"

    format := "pdf"

    var mapFiles map[string]string       
    mapFiles = make(map[string]string)
    mapFiles[localName]=  localName 

    request := new (asposecellscloud.PutConvertWorkbookRequest)
    request.File =         mapFiles    
    request.Format =         format    
    _, httpResponse, err := instance.PutConvertWorkbook(request)
    if err != nil {
      print(err)
    } else if httpResponse.StatusCode < 200 || httpResponse.StatusCode > 299 {
      print("Test fail")
    }
}

```
