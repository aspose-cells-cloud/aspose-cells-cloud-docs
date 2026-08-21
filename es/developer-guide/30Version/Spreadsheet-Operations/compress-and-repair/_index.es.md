---
title: "Comprimir y reparar archivos de Excel"
second_title: "Document"
type: docs
url: /es/compress-and-repair-excel-files/
linktitle: "Comprimir y reparar"
keywords: "Aspose.Cells, compresión de Excel, reparación de Excel, API en la nube, reducir tamaño de archivo de Excel, restaurar libro corrupto, comprimir archivo de Excel, reparar libro de Excel"
description: "Aprenda cómo comprimir libros grandes de Excel y reparar archivos corruptos utilizando la API de Aspose.Cells Cloud. Ejemplos paso a paso, lenguajes compatibles y mejores prácticas."
weight: 100
ArticleTitle: "Comprimir y reparar archivos de Excel – API de Aspose.Cells Cloud"
---

Comprimir un libro de Excel reduce su tamaño de archivo eliminando estilos, imágenes y cadenas compartidas no utilizadas, mientras que la reparación restablece la integridad de los libros corruptos. La API de Aspose.Cells Cloud proporciona puntos finales dedicados para ambas operaciones.

- **[Comprimir los datos en un archivo de Excel](https://docs.aspose.cloud/cells/compress-excel-files/).**
- **[Reparar archivos de Excel](https://docs.aspose.cloud/cells/repair-excel-files/).**

**API de compresión de libros**  
La operación **Comprimir** utiliza una solicitud POST sencilla. A continuación se presenta una especificación completa de solicitud y respuesta:

| Método | Punto final | Parámetros obligatorios | Cuerpo de la solicitud | Respuesta de ejemplo | Códigos de estado típicos |
|--------|-------------|-------------------------|------------------------|----------------------|---------------------------|
| POST   | `/cells/compress` | `file` (binario) – el libro que se va a comprimir; opcional `outPath` (cadena) – ruta de destino | *Ninguno* (el archivo se envía como multipart/form‑data) | `{ "compressedSize": 12456, "originalSize": 45678 }` | `200 OK`, `400 Bad Request`, `401 Unauthorized` |

**API de reparación de libros**  
La operación **Reparar** también utiliza una solicitud POST. Su especificación es la siguiente:

| Método | Punto final | Parámetros obligatorios | Cuerpo de la solicitud | Respuesta de ejemplo | Códigos de estado típicos |
|--------|-------------|-------------------------|------------------------|----------------------|---------------------------|
| POST   | `/cells/repair` | `file` (binario) – el libro corrupto; opcional `outPath` (cadena) – ubicación para guardar el libro reparado | *Ninguno* (el archivo se envía como multipart/form‑data) | `{ "isRepaired": true, "message": "Workbook repaired successfully." }` | `200 OK`, `400 Bad Request`, `415 Unsupported Media Type` |

Estas tablas proporcionan a los desarrolladores los detalles esenciales necesarios para invocar directamente las API sin necesidad de navegar hacia otro lugar.

**Recursos adicionales**  
- Consulte la guía completa **[Comprimir archivos de Excel](/compress-excel-files/)** para opciones avanzadas, como eliminar filas y columnas no utilizadas.  
- Revise la documentación **[Reparar archivos de Excel](/repair-excel-files/)** para obtener consejos de solución de problemas y explicaciones sobre códigos de error.  
- Explore operaciones relacionadas como **[Obtener información del archivo](/file-info/)** y **[Operaciones de hojas de cálculo](/spreadsheet-operations/)** para comprender mejor la API de Aspose.Cells Cloud.