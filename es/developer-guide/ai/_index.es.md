---
title: "Aspose.Cells Cloud AI – Descomposición de Tareas, Traducción de Hojas de Cálculo y Texto"
second_title: "Documento"
ArticleTitle: "Mejore sus habilidades en IA: Aprenda traducción de Excel, descomposición de tareas y más"
linktitle: "IA"
type: docs
url: /es/ai/
keywords: "Aspose.Cells, Cloud AI, traducción de Excel, descomposición de tareas, REST API"
description: "Explore Aspose.Cells Cloud AI para descomponer tareas, traducir libros de Excel y archivos de texto. Incluye puntos finales REST, código de ejemplo y mejores prácticas."
weight: 20
---

Aspose.Cells Cloud AI proporciona tres servicios potentes impulsados por IA que simplifican el trabajo con datos de Excel y texto: **Descomponer Tarea del Usuario**, **Traducir Hoja de Cálculo** y **Traducir Archivo de Texto**. Estas API permiten a los desarrolladores descomponer programáticamente objetivos complejos del usuario en pasos accionables, traducir libros completos o archivos de texto plano, e integrar los resultados en aplicaciones personalizadas. Utilice los puntos finales que aparecen a continuación para comenzar rápidamente, y consulte las especificaciones detalladas de solicitud/respuesta proporcionadas para cada servicio.

- **[Descomponer Tarea del Usuario](https://docs.aspose.cloud/cells/decompose-user-task/)** – Convierta los objetivos del usuario en planes secuenciales de acción mediante Aspose.Cells Cloud AI.  
  - **Método de solicitud:** `POST`  
  - **URL del punto final:** `https://api.aspose.cloud/v4.0/cells/ai/decompose-task`  
  - **Encabezados:** `Authorization: Bearer <access_token>`, `Content-Type: application/json`  
  - **Cuerpo de la solicitud (JSON):**  
    ```json
    {
      "task": "Generar un informe trimestral de ventas con gráficos y tablas dinámicas"
    }
    ```  
  - **Respuesta:** Devuelve el archivo de hoja de cálculo que contiene la lista de tareas como archivo descargable.  
  - **Códigos de estado:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`  
  - **Requisitos previos:** Token de acceso válido con el ámbito **CellsAI**.  
  - **Ejemplo de respuesta (fragmento JSON):**  
    ```json
    {
      "fileId": "12345abcde",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/12345abcde"
    }
    ```  
  - **Notas:** El libro generado incluye una hoja llamada **TaskList** con los pasos ordenados. Límite de tasa: 100 solicitudes por minuto.

- **[Traducir Hoja de Cálculo](https://docs.aspose.cloud/cells/translate-spreadsheet/)** – Traduzca una hoja de cálculo completa mediante Aspose.Cells Cloud AI.  
  - **Método de solicitud:** `POST`  
  - **URL del punto final:** `https://api.aspose.cloud/v4.0/cells/ai/translate-spreadsheet`  
  - **Encabezados:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **Parámetros de la solicitud:**  
    - `file` – El archivo de Excel para traducir (binario).  
    - `targetLanguage` – Código de idioma ISO (por ejemplo, `fr`, `de`).  
  - **Respuesta:** Devuelve el libro traducido como archivo descargable.  
  - **Códigos de estado:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **Requisitos previos:** Token de acceso con ámbito **CellsAI** y cuota de almacenamiento suficiente.  
  - **Ejemplo de respuesta (fragmento JSON):**  
    ```json
    {
      "translatedFileId": "f9d8c7b6",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/f9d8c7b6"
    }
    ```  
  - **Notas:** Se traducen todos los valores de celda, comentarios y nombres de hojas. Límite de tasa: 100 solicitudes por minuto.

- **[Traducir Archivo de Texto](https://docs.aspose.cloud/cells/translate-text-file/)** – Traduzca un archivo de texto completo mediante Aspose.Cells Cloud AI.  
  - **Método de solicitud:** `POST`  
  - **URL del punto final:** `https://api.aspose.cloud/v4.0/cells/ai/translate-text`  
  - **Encabezados:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **Parámetros de la solicitud:**  
    - `file` – El archivo de texto para traducir (binario).  
    - `targetLanguage` – Código de idioma ISO (por ejemplo, `es`, `ja`).  
  - **Respuesta:** Devuelve el archivo de texto traducido.  
  - **Códigos de estado:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **Requisitos previos:** Token de acceso válido con ámbito **CellsAI**.  
  - **Ejemplo de respuesta (fragmento JSON):**  
    ```json
    {
      "translatedFileId": "a1b2c3d4",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/a1b2c3d4"
    }
    ```  
  - **Notas:** Admite archivos de texto plano codificados en UTF-8 de hasta 5 MB. Límite de tasa: 100 solicitudes por minuto.
---