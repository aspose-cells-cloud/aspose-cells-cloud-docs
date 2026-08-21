---
title: "Opciones de guardado"
second_title: "Documento"
linktitle: "Opciones de guardado"
type: docs
url: /es/save-options/
keywords: "Aspose.Cells Cloud, SaveOptions, Excel, Libro de trabajo, API REST, Formatos de archivo, PDF, CSV, JSON, Compresión HTTP, Caché de gráficos, Rutas con nombre, Creación de directorios"
description: "Describe las propiedades de SaveOptions de la API REST de Aspose.Cells Cloud, permitiendo a los desarrolladores configurar el comportamiento de guardado de libros de trabajo en múltiples formatos de archivo y opciones, tales como compresión HTTP, actualización de la caché de gráficos y creación automática de directorios."
weight: 79
ArticleTitle: "Opciones de guardado – Documentación de la API REST de Aspose.Cells Cloud"
---

# Propiedades de SaveOptions

SaveOptions le permite controlar cómo se guarda un libro de trabajo al utilizar la API REST de Aspose.Cells Cloud. Al configurar estas opciones, puede habilitar la compresión HTTP, especificar el formato de salida, gestionar el almacenamiento temporal y controlar comportamientos adicionales, como la actualización de la caché de gráficos y la creación automática de directorios.

**Prerrequisitos**  
- Una sesión autenticada de Aspose.Cells Cloud (OAuth 2.0 o JWT).  
- El libro de trabajo de destino debe haberse cargado o creado previamente mediante la API antes de guardarlo.

| Nombre                    | Tipo       | Descripción                                                                                      | Notas      |
| ------------------------- | ---------- | ------------------------------------------------------------------------------------------------ | ---------- |
| **EnableHTTPCompression** | **bool?**  | Habilita la compresión HTTP para la respuesta.                                                  | [opcional] |
| **SaveFormat**            | **string** | Especifica el formato de archivo de destino para guardar el libro de trabajo.                   | [opcional] |
| **ClearData**             | **bool?**  | Vacía el libro de trabajo tras guardarlo.                                                        | [opcional] |
| **CachedFileFolder**      | **string** | La carpeta de archivos temporales utilizada para almacenar grandes volúmenes de datos.           | [opcional] |
| **ValidateMergedAreas**   | **bool?**  | Indica si se deben validar las áreas fusionadas antes de guardar el archivo. El valor predeterminado es false. | [opcional] |
| **RefreshChartCache**     | **bool?**  | Actualiza los datos de la caché de gráficos antes de guardar.                                   | [opcional] |
| **CreateDirectory**       | **bool?**  | Si es true y el directorio no existe, se creará automáticamente antes de guardar el archivo.   | [opcional] |
| **SortNames**             | **bool?**  | Ordena alfabéticamente las rutas con nombre al guardar.                                         | [opcional] |

**Solicitud**  
- **Método:** `POST` (o `PUT`, según la operación)  
- **Punto de conexión:** `/cells/workbook/save`  
- **Encabezados:**  
  - `Authorization: Bearer <access_token>`  
  - `Content-Type: application/json`  
- **Cuerpo:** Representación JSON del modelo `SaveOptions` (tabla anterior), combinada con los datos o la referencia del libro de trabajo.

**Ejemplo de respuesta**  
```json
{
  "status": "OK",
  "downloadUrl": "https://api.aspose.cloud/v3.0/cells/workbook/save/result.xlsx",
  "message": "Libro de trabajo guardado correctamente."
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                              |
|--------|-----------------------------|----------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante.                           |
| 413    | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño permitido. |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                         |

**Notas / Comentarios**  
- Cuando **CreateDirectory** se establece en `true`, la API creará automáticamente la carpeta de destino si aún no existe.  
- Habilitar **EnableHTTPCompression** puede reducir el tamaño de la carga útil para libros de trabajo grandes, pero el cliente debe admitir la decodificación gzip/deflate.  
- **RefreshChartCache** debe utilizarse cuando los gráficos dependan de datos dinámicos que podrían haber cambiado desde que se generó el libro de trabajo.  
---