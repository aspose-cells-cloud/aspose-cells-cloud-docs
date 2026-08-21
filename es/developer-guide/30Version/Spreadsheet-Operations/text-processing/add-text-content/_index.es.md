---
title: "Agregar texto a Excel: Insertar datos de forma eficiente con la API de hojas de cálculo basada en la nube"
second_title: "Documentos"
linktype: "Agregar texto"
type: docs
url: /es/excel-add-text/
keywords: "Excel, Aspose.Cells, agregar texto, API de hojas de cálculo, API REST, Office Cloud, inserción de texto, API de Excel"
description: "Agrega texto a una ubicación específica en una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud."
weight: 100
---

Agrega contenido de texto a una ubicación específica dentro de una hoja de cálculo. Requiere un objeto que defina el texto a agregar y la ubicación donde debe insertarse.

## **API de Excel: PostAddTextContent**

```
POST http://api.aspose.cloud/v3.0/cells/addtext
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en tokens JWT</a>.


### **Descripción de la función**

Este método agrega de forma segura nuevo texto a celdas especificadas, admitiendo múltiples modos de inserción y manejo de formatos.

- **Agregar texto al inicio de las celdas seleccionadas**  
  Inserta texto al principio de todas las celdas seleccionadas, garantizando coherencia en la entrada de datos. Ideal para agregar identificadores o etiquetas comunes, como códigos de productos, categorías o prefijos.

- **Insertar caracteres antes o después de un texto específico**  
  Coloca caracteres antes o después del texto objetivo en las celdas seleccionadas, lo que le permite crear contenido estructurado y organizado fácilmente.

- **Añadir el mismo texto al final de cada celda seleccionada**  
  Agrega texto idéntico al final de varias celdas en una sola operación, simplificando la entrada de datos y garantizando una apariencia uniforme.

- **Insertar texto antes o después de un número específico de caracteres**  
  Inserta texto después de una cantidad definida de caracteres desde el inicio o el final de cada celda en el rango objetivo. Los casos de uso típicos incluyen formatear códigos, marcas de tiempo o delimitadores personalizados.

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo  | Ubicación | Descripción                                                                 |
| --------------------- | ----- | --------- | --------------------------------------------------------------------------- |
| addTextOptions        | Clase | Cuerpo    | Especifica el contenido de texto y la posición donde debe agregarse el texto. |

### **Respuesta**

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante. |
| 413    | Payload demasiado grande    | El archivo cargado supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

## Cómo usar la API PostAddTextContent con SDK

### Especificación de la API PostAddTextContent

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/TextProcessingController/PostAddTextContent) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Uso de los SDK de Aspose.Cells Cloud

Usar un SDK es la forma más eficiente de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostAddTextContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostAddTextContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostAddTextContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostAddTextContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostAddTextContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostAddTextContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostAddTextContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostAddTextContent.go" >}}
{{</ tab>}}
{{< /tabs >}}

---