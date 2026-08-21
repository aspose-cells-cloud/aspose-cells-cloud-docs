---
title: "Información del archivo"
second_title: "Documento"
linktitle: "Información del archivo"
type: docs
url: /es/file-info/
keywords: "archivo, información, Excel, Aspose.Cells, API en la nube, metadatos, Base64"
description: "Obtenga el nombre, tamaño y contenido en Base64 de un archivo Excel mediante la API de Aspose.Cells en la nube. Incluye sintaxis de solicitud, código de ejemplo y manejo de errores."
weight: 79
ArticleTitle: "Información del archivo – metadatos y contenido en Base64 de archivos Excel (API de Aspose.Cells en la nube)"
---

## Propiedades de FileInfo


| Nombre          | Tipo   | Descripción                                                  |
| --------------- | ------ | ------------------------------------------------------------ |
| **FileName**    | string | El nombre del archivo, incluyendo su extensión.             |
| **FileSize**    | long   | El tamaño del archivo en bytes.                              |
| **FileContent** | string | Contiene los datos sin procesar del archivo Excel codificados en Base64. |

La respuesta se devuelve en formato JSON con las mismas tres propiedades que se muestran en la tabla anterior, por ejemplo:

```json
{
  "FileName": "MyWorkbook.xlsx",
  "FileSize": 254312,
  "FileContent": "UEsDBBQABgAIAAAAIQD..."
}
```

### Errores

| Código HTTP | Significado                            | Cuándo ocurre                              |
| ----------- | -------------------------------------- | ------------------------------------------ |
| 200         | Correcto – solicitud exitosa.          | Respuesta normal.                          |
| 401         | No autorizado                          | Token de autenticación ausente o inválido. |
| 404         | No encontrado                          | El archivo especificado no existe.         |
| 500         | Error interno del servidor             | Fallo inesperado del lado del servidor.    |

Para cada error, asegúrese de que el token de autenticación sea válido (401), verifique la ruta del archivo (404) o consulte la guía general de manejo de errores para estrategias de reintento (500).

## Consulte también

- [Obtener libro de trabajo](https://docs.aspose.cloud/cells/get-workbook/es) – obtenga un objeto de libro de trabajo y sus hojas de cálculo.  
- [Descargar archivo](https://docs.aspose.cloud/cells/download-file/es) – descargue los bytes sin procesar del archivo sin codificación en Base64.  
- [Descripción general de la autenticación](https://docs.aspose.cloud/cells/authentication/es) – cómo obtener y utilizar tokens de acceso.  
---