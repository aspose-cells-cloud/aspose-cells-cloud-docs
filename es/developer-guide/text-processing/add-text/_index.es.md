---
title: "API de Aspose.Cells Cloud para agregar texto: Agregar texto a múltiples celdas de Excel a la vez – Insertar prefijos, sufijos y etiquetas"
second_title: "Documento"
ArticleTitle: "Inserción masiva de texto para Excel: Agregar prefijos, sufijos y texto personalizado a celdas – Guía paso a paso"
linktitle: "AddText"
type: docs
url: /add-text/
keywords: "API de Aspose Cells, agregar texto a Excel, inserción masiva de texto, prefijo y sufijo en Excel, reemplazo de texto en hojas de cálculo, automatización de Excel, API de hojas de cálculo en la nube"
description: "Inserte prefijos, sufijos o etiquetas personalizadas en muchas celdas de Excel con una sola llamada mediante Aspose.Cells Cloud. Elija insertar al inicio, al final, antes o después de cualquier texto. Admite rangos, hojas de cálculo y manejo de celdas vacías."
weight: 100
---

Inserte texto en múltiples celdas de Excel en una sola operación. Agregue prefijos, sufijos, etiquetas o caracteres personalizados al principio, al final o antes/después de un texto específico dentro de las celdas mediante la API de Aspose.Cells.

## Descripción general

Inserción masiva en una sola llamada de prefijos, sufijos o cadenas ancladas en cada celda de un rango objetivo: sin fórmulas ni columnas auxiliares.

- Inserte texto personalizado en **cualquier posición** dentro de cada celda

| Valor            | Descripción                                                                                   |
| ---------------- | --------------------------------------------------------------------------------------------- |
| `None`           | Reemplazar el contenido original                                                              |
| `AtTheBeginning` | Insertar al inicio (prefijo)                                                                  |
| `AtTheEnd`       | Insertar al final (sufijo)                                                                    |
| `BeforeText`     | Insertar **antes** de la primera ocurrencia de `selectText`; omitir si no se encuentra        |
| `AfterText`      | Insertar **después** de la primera ocurrencia de `selectText`; omitir si no se encuentra      |

- Cuatro modos de ubicación: prefijo, sufijo, antes/después de una subcadena.
- Omitir celdas vacías para evitar desorden.
- La API solo modifica valores de tipo **texto**; los números, valores booleanos y fórmulas se convierten primero a texto.
- **Celdas vacías**
  - `skipEmptyCells = true` → se omiten las celdas vacías.
  - `skipEmptyCells = false` → se llena la celda vacía con el texto a insertar (la celda se convierte en tipo texto).

- **Ancla no encontrada**: Cuando `position = BeforeText | AfterText` y `selectText` **no existe**, el valor de la celda permanece sin cambios.

### **API web**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/add/text
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parámetros de solicitud de la API **AddText**

| Nombre del parámetro | Tipo    | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción                                                                                                                                              | Obligatorio |
| :------------------- | :------ | :---------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------- |
| Spreadsheet          | Archivo | FormData                            | El archivo de hoja de cálculo que se procesará. Los formatos admitidos incluyen XLSX, XLS, ODS, CSV, etc.                                               | Sí          |
| text                 | Cadena  | Consulta                            | El contenido de texto que se agregará a las celdas especificadas en la hoja de cálculo.                                                                  | Sí          |
| position             | Cadena  | Consulta                            | Especifica dónde insertar el texto en relación con el contenido existente de la celda. Opciones: `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`, `None`. | Sí          |
| selectText           | Cadena  | Consulta                            | _(Opcional)_ Si se proporciona, el texto se agregará solo en las celdas que contengan exactamente esta subcadena. Se usa junto con el parámetro `position`. | No          |
| skipEmptyCells       | Booleano | Consulta                            | Si es `true`, se omiten las celdas vacías; si es `false`, se agrega texto a las celdas vacías.                                                           | No          |
| worksheet            | Cadena  | Consulta                            | _(Opcional)_ El nombre de la hoja de cálculo donde se agregará el texto. Si se omite, la operación se aplica a la primera hoja de cálculo de forma predeterminada. | No          |
| range                | Cadena  | Consulta                            | _(Opcional)_ El rango de celdas donde se agregará el texto (por ejemplo, `"A1:C10"`). Si se omite, la operación se aplica a todas las celdas usadas en la hoja especificada. | No          |
| outPath              | Cadena  | Consulta                            | _(Opcional)_ La ruta de la carpeta en el almacenamiento en la nube donde se guardará el libro procesado. Si se omite, el archivo se guarda en la carpeta original. | No          |
| outStorageName       | Cadena  | Consulta                            | El nombre del almacenamiento en la nube donde se guardará el archivo de salida.                                                                         | No          |
| region               | Cadena  | Consulta                            | _(Opcional)_ Establece la configuración regional para formatear números, fechas y monedas en el archivo de salida (por ejemplo, `"en-US"`, `"zh-CN"`, `"de-DE"`). | No          |
| password             | Cadena  | Consulta                            | _(Opcional)_ Si el libro cargado está protegido con contraseña, proporcione la contraseña para abrir y procesar el archivo.                             | No          |

**Ejemplo con cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/add/text?text=Report&position=AtTheBeginning&skipEmptyCells=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/workbook.xlsx" \
  -F "outPath=output/workbook_modified.xlsx"
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

### Códigos de error

| Código | Descripción |
| ------ | ----------- |
| **400** Solicitud incorrecta | URI de la API de Aspose.Cells Cloud inválido o parámetros obligatorios faltantes. |
| **401** No autorizado | Token de acceso inválido o ID y secreto del cliente inválidos. |
| **404** No encontrado | El archivo de hoja de cálculo no es accesible. |
| **500** Error del servidor | La hoja de cálculo encontró una anomalía al obtener los datos de cálculo. |

## ¿Dónde debemos usar la API de Add Text para hojas de cálculo?

- **Etiquetado dinámico de informes**: Agregue títulos dinámicos, etiquetas de fecha u observaciones a estados financieros y reportes de ventas generados automáticamente.
- **Marcas de agua por lotes**: Agregue logotipos de empresa, marcas de agua de confidencialidad o información de versión a un lote de archivos de Excel.
- **Relleno de datos de plantillas**: Rellene automáticamente nombres de clientes, montos y otro texto en posiciones designadas de plantillas de contratos o facturas.
- **Etiquetado por clasificación de datos**: Agregue automáticamente etiquetas de clasificación o etiquetas de estado (por ejemplo, “Pendiente de revisión”, “Aprobado”) a filas de datos según los resultados del análisis.
- **Anotación de calidad de datos**: Agregue notas para datos problemáticos durante la limpieza de datos.
- **Formato de texto por lotes**: Agregue uniformemente prefijos o sufijos a nombres de productos o clientes.

## ¿Por qué debería usar la API de Add Text para hojas de cálculo?

- **Adición masiva de texto**: Agregue texto a cientos de celdas o archivos a la vez, ahorrando hasta un 95 % del tiempo en comparación con el trabajo manual.
- **Control preciso de la posición**: Admite la inserción precisa de texto en seis posiciones, incluyendo el inicio, el final o antes/después de un texto específico dentro de una celda.
- **Manejo inteligente condicional**: Decida si agregar texto según si la celda está vacía o contiene texto específico.
- **Soporte para estrategia de múltiples posiciones**:
  - `AtTheBeginning`: Agregue el mismo texto antes del contenido de todas las celdas seleccionadas.
  - `AtTheEnd`: Agregue texto después del contenido de todas las celdas seleccionadas.
  - `BeforeText` / `AfterText`: Agregue texto solo antes o después de las celdas que contienen texto específico.
  - `None`: Reemplace el contenido original.
- **Control preciso del rango**: Permite especificar hojas de cálculo o rangos de celdas particulares para las operaciones.
- **Opción de omitir condicionalmente**: Admite omitir celdas vacías para evitar adiciones innecesarias de texto.
- **Amigable para desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y viene con documentación completa. En comparación con la construcción de soluciones personalizadas de renderizado de gráficos, esto reduce significativamente la carga de desarrollo.
- **Rentable**: Puede agregar texto en una celda sin cargar primero el libro, lo que ahorra espacio de almacenamiento y reduce costos.

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/AddText) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de Aspose.Cells Cloud

Usar el SDK es la mejor manera de acelerar el desarrollo. El SDK maneja los detalles subyacentes, lo que le permite simplemente implementar la inserción de texto en celdas con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código ilustran cómo realizar llamadas a los servicios web de Aspose.Cells mediante varios SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddText.go" >}}
{{</tab>}}
{{< /tabs >}}
---