---
title: "Inicio con la API en la nube de Aspose.Cells: Procesar archivos de Excel en 3 pasos sencillos"
second_title: "Documento"
ArticleTitle: "Inicio con Aspose.Cells Cloud"
linktype: "Inicio"
type: docs
url: /es/getting-started/
description: "Aprenda cómo cargar, convertir y descargar archivos de Excel utilizando la API REST de Aspose.Cells Cloud en tres pasos sencillos. Incluye ejemplos de código cURL."
weight: 10
keywords: "Aspose.Cells Cloud, API de Excel, conversión de hojas de cálculo, Excel a PDF, hoja de cálculo en la nube, API de Aspose.Cells Cloud"
---

- [Visión general](/es/cells/overview/)
- [Guía de inicio rápido](/es/cells/quickstart/)
- [SDK disponibles](/es/cells/available-sdks/)
- [Plataformas compatibles](/es/cells/supported-platforms/)
- [Formatos de archivo admitidos](/es/cells/supported-file-formats/)
- [Evaluar Aspose.Cells Cloud](/es/cells/evaluate-aspose-cells/)
- [Plan de precios](/es/cells/pricing-plan/)
- [Soporte técnico](/es/cells/technical-support/)
- [Cómo ejecutar un contenedor Docker](/es/cells/how-to-run-docker-container/)

**Guía de inicio**

Antes de comenzar, asegúrese de tener una **clave de API de Aspose Cloud válida** y un **nombre de almacenamiento**. Estas credenciales son necesarias para todas las llamadas posteriores a la API.

**Paso 1: Cargar un archivo de Excel**  
Cargue su libro de trabajo de origen en el almacenamiento de Aspose Cloud.

```curl
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/{path}" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/octet-stream" \
     --data-binary @sample.xlsx
```

*Cuerpo de la solicitud*: El archivo se envía como un flujo binario (`application/octet‑stream`).  
*Parámetros requeridos*:

- `path` – ruta de almacenamiento donde se guardará el archivo (por ejemplo, `folder/sample.xlsx`).

**Paso 2: Convertir el libro de trabajo a PDF**  
Envíe una solicitud de conversión una vez que el archivo esté almacenado.

```curl
curl -X POST "https://api.aspose.cloud/v4.0/cells/{name}/saveas?format=pdf&outPath={outputPath}" \
     -H "Authorization: Bearer {access_token}"
```

*Parámetros requeridos*:

- `name` – nombre del libro de trabajo cargado (por ejemplo, `sample.xlsx`).
- `format` – formato de destino (`pdf`).
- `outputPath` – ruta de almacenamiento para el archivo convertido (por ejemplo, `folder/result.pdf`).

*Payload de respuesta de ejemplo* (JSON):

```json
{
  "status": "OK",
  "outputPath": "folder/result.pdf"
}
```

**Paso 3: Descargar el PDF convertido**  
Recuperar el PDF resultante desde el almacenamiento.

```curl
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/{outputPath}" \
     -H "Authorization: Bearer {access_token}" \
     -o result.pdf
```

*Parámetros requeridos*:

- `outputPath` – ruta del PDF generado en el paso anterior.

**Resumen de solicitud / respuesta de ejemplo**

| Operación | Método HTTP | Endpoint (ejemplo) | Parámetros | Estado de éxito |
|-----------|-------------|--------------------|------------|----------------|
| Cargar    | PUT         | /cells/storage/file/{path} | `path` (ubicación de almacenamiento) | 200 OK |
| Convertir | POST        | /cells/{name}/saveas?format=pdf&outPath={outputPath} | `name`, `format`, `outPath` | 200 OK |
| Descargar | GET         | /cells/storage/file/{outputPath} | `outputPath` | 200 OK |

**Códigos de error comunes**

- **400 Solicitud incorrecta**: Faltan parámetros o estos son inválidos.  
- **401 No autorizado**: Token de acceso inválido o faltante.  
- **404 No encontrado**: El archivo o la ruta especificados no existen.  
- **500 Error interno del servidor**: Error inesperado del servidor; reintente o contacte con soporte técnico.  
---