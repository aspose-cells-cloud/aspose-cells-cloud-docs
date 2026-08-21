---
title: "Cómo agregar filas a una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Agregar"
type: docs
url: /es/rows/add/
keywords: "Aspose.Cells, agregar filas, API de Excel, REST, C#, Java, Python, Node.js"
description: "Guía paso a paso para agregar una o varias filas a una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud, con ejemplos de código en C#, Java, Python y Node.js."
weight: 20
ArticleTitle: "Agregar filas a una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud – Guía paso a paso"
---

## Cómo agregar filas a una hoja de cálculo de Excel

Este artículo explica cómo insertar una fila vacía única o varias filas en una hoja de cálculo existente utilizando la API REST de Aspose.Cells Cloud. Asegúrese de tener una clave de API válida y el SDK correspondiente instalado antes de continuar.

**Requisitos previos**  
- [ ] Cuenta de Aspose.Cells Cloud con una suscripción activa.  
- [ ] Clave de API/Token de acceso generado desde el panel de control de Aspose Cloud.  
- [ ] Uno de los SDK admitidos (C#, Java, Python, Node.js) instalado y configurado.  

**Referencia de la API**  
- **Método HTTP:** `POST`  
- **Punto de conexión:** `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/rows`  
- **Parámetros obligatorios en la ruta:**  
  - `fileName` – Nombre del archivo de Excel almacenado en la nube.  
  - `sheetName` – Nombre de la hoja de cálculo donde se agregarán las filas.  
- **Parámetros de consulta:**  
  - `startrow` – Índice de fila en base cero donde comienza la inserción.  
  - `totalRows` – Número de filas a insertar.  
  - `folder` – (Opcional) Ruta de la carpeta en la nube donde se encuentra el archivo.  
  - `storage` – (Opcional) Nombre del almacenamiento si se utiliza uno distinto del predeterminado.  
- **Cuerpo de la solicitud (ejemplo en JSON):**  

  ```json
  {
    "startrow": 5,
    "totalRows": 3
  }
  ```

  **Ejemplo con cURL**

  ```bash
  curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/rows?startrow=5&totalRows=3&folder=MyFolder&storage=MyStorage" \
      -H "Authorization: Bearer {access_token}" \
      -H "Content-Type: application/json" \
      -d '{"startrow":5,"totalRows":3}'
  ```

- **Respuesta correcta (HTTP 200):** Devuelve la información actualizada de la hoja de cálculo, incluido el nuevo número de filas.  

  ```json
  {
    "Code": 200,
    "Status": "OK",
    "Worksheet": {
      "Name": "Sheet1",
      "RowsCount": 30
    }
  }
  ```

- **Ejemplo de respuesta de error (HTTP 400):**  

  ```json
  {
    "Code": 400,
    "Status": "Bad Request",
    "Message": "El parámetro startrow no es válido. Debe ser un entero no negativo."
  }
  ```

- **Códigos de estado:**  

  | Código | Significado                                |
  |--------|--------------------------------------------|
  | 200    | Filas agregadas correctamente             |
  | 400    | Parámetros inválidos o JSON mal formado   |
  | 401    | Fallo en la autenticación                  |
  | 404    | Archivo o hoja de cálculo no encontrados  |
  | 500    | Error del servidor                         |

A continuación, se incluyen enlaces rápidos a los ejemplos detallados para agregar filas:

- [Cómo agregar una fila vacía en una hoja de cálculo de Excel](/cells/rows/add/row/)
- [Cómo agregar varias filas en una hoja de cálculo de Excel](/cells/rows/add/rows/)
---