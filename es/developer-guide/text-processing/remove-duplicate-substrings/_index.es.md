---
title: "API de Web de Aspose.Cells Cloud para eliminar subcadenas duplicadas: deduplicar texto repetido en Excel"
second_title: "Documento"
ArticleTitle: "Eliminador de subcadenas duplicadas en Excel: limpiar texto repetido en celdas"
linktitle: "Eliminar subcadenas duplicadas"
type: docs
url: /remove-duplicate-substrings/
keywords: "Aspose.Cells, subcadenas duplicadas, API de Excel, limpieza de texto, nube"
description: "Elimine subcadenas duplicadas de celdas de Excel mediante la API de Aspose.Cells Cloud, preservando el formato y la validación."
weight: 100
---

Elimine subcadenas duplicadas de celdas de Excel con detección inteligente. Mantenga el formato original intacto mientras elimina el texto redundante mediante la API de deduplicación de Aspose.Cells.

## **Introducción**: Elimine caracteres no deseados con precisión

La API de limpieza de subcadenas repetidas elimina subcadenas duplicadas dentro de celdas individuales de un rango de Excel, preservando el formato de celda, la validación de datos y otras estructuras del libro. Procesa cada celda de forma independiente, conservando únicamente la primera ocurrencia de cada subcadena duplicada.

### **Opciones de fuente de datos**

| Campo      | Tipo   | Obligatorio | Descripción                                      |
| ---------- | ------ | ----------- | ------------------------------------------------ |
| `workbook` | archivo | Sí         | Archivo de libro de Excel (.xlsx, .xlsm)        |
| `range`    | cadena | Sí         | Rango objetivo a procesar (p. ej., "A1:D100", "Hoja1!A:D") |

### **Opciones de delimitador**

| Campo                               | Tipo    | Valor predeterminado | Descripción                                                                                                                                              |
| ----------------------------------- | ------- | -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `delimiters`                        | cadena  | `"preset"`           | Opciones: `preset`, `custom`, `comma`, `semicolon`, `space`, `tab`, `line-break` o una cadena de delimitador personalizado (varios caracteres se tratan como compuesto) |
| `treatConsecutiveDelimitersAsOne`  | booleano | `false`              | Agrupar delimitadores adyacentes en un único separador                                                                                                  |
| `caseSensitive`                    | booleano | `false`              | Determina si la comparación distingue mayúsculas y minúsculas. Si es `false`, se ignoran las mayúsculas durante la detección de duplicados.           |

## **API RemoveDuplicateSubstrings**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parámetros de solicitud de la API **RemoveDuplicateSubstrings**

| Nombre del parámetro            | Tipo    | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                                                                                       |
| :------------------------------ | :------ | :-------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet                     | Archivo | FormData                                | Archivo de hoja de cálculo que se va a procesar. Los formatos compatibles incluyen XLSX, XLS, ODS, CSV, etc.                                                                      |
| delimiters                      | Cadena  | Consulta                                | Especifica uno o más caracteres delimitadores utilizados para dividir el contenido de la celda en subcadenas para la detección y eliminación de duplicados. Pueden especificarse varios delimitadores (p. ej., `",;"`). |
| treatConsecutiveDelimitersAsOne | Booleano | Consulta                                | Si se establece en `true`, los caracteres delimitadores consecutivos se tratan como un único separador. Si es `false`, cada delimitador se procesa individualmente.                |
| caseSensitive                   | Booleano | Consulta                                | Si es `true`, la detección de duplicados considera mayúsculas y minúsculas (p. ej., "Texto" ≠ "texto"). Si es `false`, se ignoran las mayúsculas durante la comparación de duplicados. |
| worksheet                       | Cadena  | Consulta                                | _(Opcional)_ Nombre de la hoja de cálculo donde se aplicará la eliminación de subcadenas duplicadas. Si se omite, la operación se aplica a la primera hoja de cálculo.             |
| range                           | Cadena  | Consulta                                | _(Opcional)_ Rango de celdas donde se aplicará la eliminación de subcadenas duplicadas (p. ej., `"A1:C10"`). Si se omite, la operación se aplica a todas las celdas utilizadas en la hoja especificada. |
| outPath                         | Cadena  | Consulta                                | _(Opcional)_ Ruta de carpeta en el almacenamiento en la nube donde se guardará el libro procesado. Si se omite, el archivo se guarda en la carpeta de origen.                     |
| outStorageName                  | Cadena  | Consulta                                | Nombre del almacenamiento en la nube donde se guardará el archivo de salida.                                                                                                      |
| region                          | Cadena  | Consulta                                | _(Opcional)_ Establece la configuración regional para el procesamiento de texto, lo que puede afectar la interpretación de delimitadores y las reglas de distinción entre mayúsculas y minúsculas para ciertos idiomas (p. ej., `"es-ES"`, `"en-US"`). |
| password                        | Cadena  | Consulta                                | _(Opcional)_ Si la hoja de cálculo cargada está protegida con contraseña, proporcione la contraseña para abrir y procesar el archivo.                                              |

**Ejemplo de solicitud (cURL)**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings?delimiters=comma&caseSensitive=false" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx" \
     -F "range=A1:D100"
```

### **Respuesta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### **Códigos de estado**

| Código | Significado                             | Descripción                                                                                     |
|--------|-----------------------------------------|-------------------------------------------------------------------------------------------------|
| 200    | Correcto                                | La solicitud se realizó correctamente y se devuelve el libro procesado.                        |
| 202    | Aceptado                                | La solicitud se acepta para procesamiento asíncrono.                                            |
| 400    | Solicitud incorrecta                    | La solicitud tiene un formato incorrecto o contiene parámetros no válidos.                      |
| 401    | No autorizado                           | La autenticación falló o el token es inexistente o no válido.                                   |
| 404    | No encontrado                           | No se pudo encontrar el libro de cálculo o recurso especificado.                                |
| 500    | Error interno del servidor              | Se produjo un error inesperado en el lado del servidor.                                         |

## ¿Dónde se debe utilizar la API de eliminación de subcadenas duplicadas?

- **Escenarios de limpieza y estandarización de datos**: Limpiar etiquetas como `"VIP,Premium,VIP,Gold"` → `"VIP,Premium,Gold"`.
- **Datos técnicos y operativos**: Limpiar entradas de registro con códigos de error repetidos, eliminar identificadores duplicados de contenedores o estantes, etc.
- **Gestión de contenido y medios**: Deduplicar etiquetas de habilidades, eliminar entradas de certificación redundantes.

## ¿Por qué debería utilizar la API de eliminación de subcadenas duplicadas?

- **Automatice tareas manuales**: Elimine ediciones tediosas y reduzca errores humanos.  
- **Preserve la integridad de los datos**: Los colores, fuentes, bordes y formatos condicionales de las celdas permanecen sin cambios; las listas desplegables y las reglas de validación se conservan.  
- **Procesamiento flexible**: Adaptable a cualquier delimitador, con control opcional sobre distinción entre mayúsculas y minúsculas y protección de encabezados.  
- **Amigable para desarrolladores**: Aspose.Cells Cloud proporciona SDK en múltiples lenguajes, lo que permite un desarrollo rápido con documentación completa.  
- ** rentable**: La operación se realiza en la nube, evitando la necesidad de almacenar archivos intermedios localmente.  

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstrings) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de Aspose.Cells Cloud

Utilizar los SDK es la mejor forma de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, permitiéndole implementar simplemente la eliminación de subcadenas duplicadas en celdas con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersWithFirstNCharacters.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersWithFirstNCharacters.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersWithFirstNCharacters.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersWithFirstNCharacters.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersWithFirstNCharacters.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersWithFirstNCharacters.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersWithFirstNCharacters.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersWithFirstNCharacters.go" >}}
{{</tab>}}
{{< /tabs >}}
---