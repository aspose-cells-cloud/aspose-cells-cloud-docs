---
title: "API de división de texto – Segmentar celdas de Excel en columnas | Aspose.Cells Cloud"
second_title: "Documento"
ArticleTitle: "Divisor de texto de Excel – Segmentar contenido de celdas en múltiples columnas | Aspose.Cells Cloud"
linktitle: "División de texto"
type: docs
url: /split-text/
keywords: "Aspose, Cells, API de división de texto, Excel, delimitador, segmentación de texto, API en la nube"
description: "Divida fácilmente el texto de las celdas de Excel en columnas o filas independientes utilizando Aspose.Cells Cloud. Admite delimitadores personalizados, máscaras, saltos de línea y la opción de conservar o no los delimitadores. Comience en minutos con curl o SDK."
weight: 100
---

Segmente el texto de las celdas de Excel en múltiples columnas utilizando reglas personalizadas de segmentación. Divida el contenido por delimitador y genere el resultado en rangos especificados mediante la API web de división de texto de Aspose.Cells Cloud.

## **Introducción**: División de texto

La API de segmentación de texto divide el contenido de las celdas en varias celdas según delimitadores, patrones o saltos de línea especificados, y escribe los resultados en un rango de destino. Admite métodos flexibles de división, salida en direcciones especificadas (columnas o filas) y opciones para conservar los delimitadores: ideal para analizar datos concatenados, contenido tipo CSV o texto multilínea en formatos estructurados.

- **Dividir celda por carácter específico** – divida el contenido de la celda en varias celdas seleccionando cualquier carácter como delimitador (coma, espacio, punto y coma, etc.).
- **Dividir celdas por cadena** – separe celdas mediante cualquier combinación de caracteres que especifique.
- **Dividir texto por máscara** – utilice comodines para dividir el texto según un patrón determinado, ofreciendo un método aún más flexible y potente para dividir texto.
- **Dividir contenido de celda por salto de línea** – genere una presentación más organizada dividiendo por saltos de línea.
- **Dividir celdas en columnas o filas** – elija si los resultados de la división se escriben en columnas o filas consecutivas.
- **Eliminar o conservar delimitadores** – decida si los delimitadores se eliminan o se conservan al principio o al final de las celdas resultantes.

## **API SplitText**

**Requisitos previos**: Para utilizar esta API necesita un token de acceso válido de Aspose Cloud, y el libro que se va a procesar debe cargarse en el almacenamiento de Aspose Cloud o suministrarse directamente en la solicitud. La API admite formatos de hojas de cálculo comunes como XLSX, XLS, ODS y CSV.

### API web

```http
POST https://api.aspose.cloud/v4.0/cells/content/split/text
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parámetros de solicitud de la API **splitText**

| Nombre del parámetro             | Tipo    | Ubicación   | ¿Requerido? | Valor predeterminado | Descripción                                                                                                                                         |
| -------------------------------- | ------- | ----------- | ----------- | -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet                      | File    | FormData    | Sí          | —                    | Archivo de hoja de cálculo que se va a procesar. Los formatos admitidos incluyen XLSX, XLS, ODS, CSV, etc.                                          |
| delimiters                       | String  | Query       | No          | —                    | Uno o más caracteres delimitadores utilizados para dividir el texto dentro de las celdas (por ejemplo, `","`, `";"`, `Space`, `LineBreak`, `Tab`, `Pipe`, `Custom`). |
| keepDelimitersInResultingCells   | Boolean | Query       | No          | false                | Si es `true`, los caracteres delimitadores se conservan en las celdas divididas resultantes.                                                       |
| keepDelimitersPosition           | String  | Query       | No          | None                 | Dónde conservar los delimitadores si `keepDelimitersInResultingCells` es `true`. Opciones: `None`, `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`. |
| howToSplit                       | String  | Query       | No          | SplitToColumns       | Método de segmentación de texto. Opciones: `None`, `SplitToColumns`, `SplitToRows`.                                                                |
| outPositionRange                 | String  | Query       | Sí          | —                    | Rango de destino donde se escribirán los resultados de la división (por ejemplo, `"D1:F10"`).                                                       |
| worksheet                        | String  | Query       | No          | —                    | Nombre de la hoja de cálculo donde se aplicará la división de texto. Si se omite, se utiliza la primera hoja.                                      |
| range                            | String  | Query       | No          | —                    | Rango de celdas de origen al que se aplicará la operación de división (por ejemplo, `"A1:A10"`). Si se omite, se procesan todas las celdas usadas en la hoja. |
| outPath                          | String  | Query       | No          | —                    | Ruta de la carpeta en el almacenamiento en la nube donde se guardará el libro procesado. Si se omite, el archivo se guarda en la carpeta de origen. |
| outStorageName                   | String  | Query       | No          | —                    | Nombre del almacenamiento en la nube donde se guardará el archivo de salida.                                                                       |
| region                           | String  | Query       | No          | —                    | Configuración regional para la segmentación de texto, que puede afectar la interpretación de los delimitadores y la codificación de caracteres (por ejemplo, `"en-US"`, `"ja-JP"`). |
| password                         | String  | Query       | No          | —                    | Contraseña para abrir una hoja de cálculo protegida con contraseña.                                                                                |

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

### Códigos de error

- **400 Bad Request (Solicitud incorrecta)** – URI de la API de Aspose.Cells Cloud no válido o parámetros mal formados.
- **401 Unauthorized (No autorizado)** – Token de acceso ausente o no válido (o client-id/secret).
- **404 Not Found (No encontrado)** – No se pudo acceder al archivo de hoja de cálculo especificado.
- **500 Server Error (Error del servidor)** – Se produjo una anomalias interna de procesamiento en la hoja de cálculo.

## ¿Dónde debemos utilizar la API de división de texto?

### **Limpieza de importación de archivos CSV y de texto**

Al importar datos de sistemas externos, los campos a menudo se concatenan en celdas únicas:

- **Importaciones de datos de ERP/CRM** – divida `"John Doe;johndoe@email.com;555-1234"` en columnas separadas de nombre, correo electrónico y teléfono.
- **Exportaciones de base de datos** – analice claves combinadas como `"ORD-2024-001|Premium|Express"` en ID de pedido, nivel y método de envío.
- **Análisis de archivos de registro** – descomponga registros semiestructurados como `"2024-01-15 10:30:00|ERROR|ConnectionTimeout"` para su filtrado.

### **Migración de sistemas heredados**

- Los sistemas antiguos vuelcan campos de valores múltiples en celdas únicas; divídalos para que coincidan con los esquemas de bases de datos nuevas.
- Convierta exportaciones de archivos planos en tablas de Excel normalizadas, listas para Power BI o Tableau.

### **Limpieza y estandarización de datos**

- **Normalización de delimitadores** – convierta delimitadores mixtos (`"A,B;C|D"`) en un formato uniforme utilizando la división con múltiples delimitadores.
- **Limpieza de espacios en blanco** – divida por espacios para identificar y eliminar espacios extra entre palabras.
- **Datos financieros** – divida códigos de transacción combinados como `"DEP-CHK-3847"` en tipo de transacción, fuente y referencia.
- **Registros médicos** – analice datos de pacientes como `"Smith,Jane_F_1985"` en apellido, nombre, género y año de nacimiento.

## ¿Por qué debería utilizar la API de división de texto?

- **Caracteres específicos** – divida por cualquier carácter único (coma, punto y coma, tabulador, espacio).
- **Combinaciones de cadenas** – utilice delimitadores multicharacter como `||`, `->` o separadores personalizados.
- **Saltos de línea** – analice instantáneamente celdas multilínea en filas independientes (direcciones, comentarios, descripciones).
- **Delimitadores personalizados** – defina cualquier combinación de caracteres como delimitador para formatos de datos propietarios.
- **Fácil de usar para desarrolladores** – Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y viene acompañado de una documentación completa. En comparación con la creación de soluciones personalizadas, esto reduce significativamente la carga de desarrollo.
- **Rentable** – puede eliminar caracteres duplicados sin cargar primero el libro, lo que ahorra espacio de almacenamiento y reduce costos.

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/SplitText) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar el SDK es la mejor manera de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, lo que le permite implementar simplemente la división de texto para celdas con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver la lista completa de SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código ilustran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitText.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitText.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitText.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitText.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitText.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitText.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitText.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitText.go" >}}  
{{</tab>}}  
{{< /tabs >}}
---