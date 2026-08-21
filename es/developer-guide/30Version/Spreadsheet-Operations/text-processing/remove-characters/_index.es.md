---
title: "Eliminar caracteres de Excel – API de Aspose.Cells Cloud (POST /cells/removecharacters)"
second_title: "Documento"
linktitle: "Eliminar caracteres"
type: docs
url: /es/excel-remove-characters/
keywords: "eliminar caracteres, Aspose.Cells, API de Excel, procesamiento de texto, nube"
description: "Aprenda a eliminar caracteres, conjuntos de caracteres o subcadenas de hojas de cálculo de Excel mediante la API de Aspose.Cells Cloud. Incluye esquema de solicitud, ejemplo de cURL, código de SDK y manejo de errores."
weight: 100
ArticleTitle: "Eliminar caracteres de Excel – API de Aspose.Cells Cloud (POST /cells/removecharacters)"
---

## Eliminar caracteres de Excel mediante la API web

Un conjunto completo de herramientas para limpiar contenido de texto dentro de celdas seleccionadas. La API elimina caracteres específicos, conjuntos predefinidos de caracteres o subcadenas, asegurando que el texto de la hoja de cálculo esté estandarizado y libre de símbolos no deseados.

**Requisitos previos**

- Una cuenta activa de Aspose Cloud.  
- Un token de acceso JWT válido obtenido según se describe en la guía de autenticación.  
- El archivo de Excel debe cargarse en el almacenamiento antes de llamar a este punto final.  
- Los formatos de archivo admitidos incluyen `.xlsx`, `.xls`, `.xlsm` y otros tipos comunes de Excel.

```http
POST https://api.aspose.cloud/v3.0/cells/removecharacters
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Descripción de la función

- **Eliminar caracteres personalizados** – Especifique los caracteres que desea eliminar. Ingrese cada carácter en el campo _Eliminar caracteres personalizados_; la API eliminará todas las ocurrencias de esos caracteres en las celdas seleccionadas.  
- **Eliminar conjuntos de caracteres** – Elija entre los conjuntos predefinidos:  
  - **Caracteres no imprimibles** – Elimina los saltos de línea y los primeros 32 caracteres no imprimibles de ASCII (0‑31), además de los códigos adicionales (127, 129, 141, 143, 144, 157).  
  - **Caracteres de texto** – Elimina todas las letras.  
  - **Caracteres numéricos** – Elimina todos los dígitos.  
  - **Símbolos** – Elimina símbolos matemáticos, geométricos, técnicos, de moneda y símbolos similares a letras como “?”, “1” y “™”.  
  - **Signos de puntuación** – Elimina todos los signos de puntuación.  
- **Eliminar una subcadena** – Elimina cualquier subcadena especificada (por ejemplo, una palabra) de las celdas seleccionadas.

### Parámetros de solicitud

| Nombre del parámetro    | Tipo  | Ubicación | Descripción                                                               |
| ----------------------- | ----- | --------- | ------------------------------------------------------------------------- |
| removeCharactersOptions | Clase | Cuerpo    | Opciones que definen qué caracteres, conjuntos de caracteres o subcadenas eliminar. |

**Esquema de `removeCharactersOptions`**

| Propiedad        | Tipo    | Obligatorio | Descripción                                                                                     |
| ---------------- | ------- | ----------- | ----------------------------------------------------------------------------------------------- |
| Range            | string  | Sí          | Notación A‑1 o nombre de rango que identifica las celdas a procesar (por ejemplo, `"A1:C10"`). |
| CustomCharacters | string  | No          | Cadena que contiene cada carácter personalizado a eliminar (por ejemplo, `"@#$"`).              |
| CharacterSet     | string  | No          | Valor de enumeración que especifica un conjunto predefinido (`"NonPrinting"`, `"Text"`, `"Numeric"`, `"Symbols"`, `"Punctuation"`). |
| Substring        | string  | No          | La subcadena exacta a eliminar (por ejemplo, `"USD"`).                                         |
| IgnoreCase       | boolean | No          | Si es `true`, la eliminación de caracteres no distingue entre mayúsculas y minúsculas.          |

**Ejemplo de cuerpo de solicitud JSON**

```json
{
  "Range": "A1:B20",
  "CustomCharacters": "@#$",
  "CharacterSet": "NonPrinting",
  "Substring": "USD",
  "IgnoreCase": true
}
```

**Solicitud de ejemplo con cURL**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/removecharacters" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "Range": "A1:B20",
           "CustomCharacters": "@#$",
           "CharacterSet": "NonPrinting",
           "Substring": "USD",
           "IgnoreCase": true
         }'
```

### **Respuesta**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nombre de archivo combinado]",
    "Filesize" : [tamaño de archivo],
    "FileContent" : "[Base64String]"
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                    |
|--------|-----------------------------|----------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante.                                 |
| 413    | Payload demasiado grande    | El archivo cargado excede el límite de tamaño.                |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                               |

## Cómo usar la API PostRemoveCharacters con SDK

### Especificación de la API PostRemoveCharacters

La <a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostRemoveCharacters" rel="noopener noreferrer">especificación completa de OpenAPI para el punto final PostRemoveCharacters</a> define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Uso de los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK: