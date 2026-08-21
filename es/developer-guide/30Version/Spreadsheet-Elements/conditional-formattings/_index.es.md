---
title: "Trabajo con el formato condicional de Excel"
second_title: "Document"
linktitle: "Formato condicional"
type: docs
url: /es/conditional-formattings/
aliases: [  /es/working-with-conditional-formatting/ ]
keywords: "Excel, Formato condicional, Aspose.Cells Cloud, API"
description: "La API de Aspose.Cells Cloud para Excel proporciona puntos finales para recuperar, agregar, modificar y borrar reglas de formato condicional, permitiendo un análisis visual dinámico de los datos de la hoja de cálculo."
weight: 100
ArticleTitle: "Trabajo con el formato condicional de Excel – Guía de API"
---

El formato condicional en Excel le permite resaltar celdas con un color específico, dependiendo del valor de la celda.

Use el formato condicional para explorar y analizar visualmente los datos, detectar problemas críticos, y identificar patrones y tendencias.

El formato condicional facilita el resaltado de celdas o rangos de celdas interesantes, el énfasis en valores inusuales y la visualización de datos mediante barras de datos, escalas de color y conjuntos de iconos que corresponden a variaciones específicas en los datos.

Un formato condicional cambia la apariencia de las celdas según las condiciones que especifique. Si las condiciones son verdaderas, se aplica el formato al rango de celdas; si son falsas, el rango de celdas permanece sin cambios. Existen muchas condiciones integradas, y también puede crear las suyas propias (incluyendo mediante una fórmula que se evalúe como **VERDADERO** o **FALSO**).

La API de Aspose.Cells Cloud proporciona un conjunto de puntos finales para gestionar reglas de formato condicional de forma programática. Las siguientes operaciones están disponibles:

- **Obtener formatos condicionales de una hoja de cálculo** – Recupera todas las reglas de formato condicional aplicadas a una hoja de cálculo.  
  - **Método:** `GET`  
  - **Punto final:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Parámetros:** `fileName` (cadena, obligatorio), `sheetName` (cadena, obligatorio), parámetros de consulta opcionales como `folder`, `storageName`  
  - **Ejemplo con cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings?folder=Docs&storageName=MyStorage" -H "Authorization: Bearer {access_token}"
    ```
- **Obtener formato condicional** – Devuelve una regla específica de formato condicional mediante su identificador.  
  - **Método:** `GET`  
  - **Punto final:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **Parámetros:** `index` (entero, obligatorio) identifica la posición de la regla.  
  - **Ejemplo con cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```
- **Agregar un área de celdas para la condición de formato** – Agrega un rango de celdas que será afectado por el formato condicional especificado.  
  - **Método:** `POST`  
  - **Punto final:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **Cuerpo de la solicitud (JSON):** `{ "FirstRow": 1, "FirstColumn": 1, "RowCount": 5, "ColumnCount": 3 }`  
  - **Ejemplo con cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"FirstRow":1,"FirstColumn":1,"RowCount":5,"ColumnCount":3}'
    ```
- **Agregar una condición para la condición de formato** – Define una nueva condición (por ejemplo, valor, fórmula) para una regla de formato existente.  
  - **Método:** `POST`  
  - **Punto final:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`  
  - **Cuerpo de la solicitud (JSON):** `{ "Type": "CellValue", "Operator": "GreaterThan", "Formula1": "100" }`  
  - **Ejemplo con cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"Type":"CellValue","Operator":"GreaterThan","Formula1":"100"}'
    ```
- **Agregar una condición de formato** – Crea una regla completa de formato condicional, incluyendo su tipo y estilo.  
  - **Método:** `POST`  
  - **Punto final:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Cuerpo de la solicitud (JSON):**  
    ```json
    {
      "Priority": 0,
      "Type": "HighlightCells",
      "Style": { "ForegroundColor": "FFFF0000" },
      "Condition": { "Operator": "LessThan", "Formula1": "50" },
      "CellArea": { "FirstRow": 0, "FirstColumn": 0, "RowCount": 10, "ColumnCount": 5 }
    }
    ```  
  - **Ejemplo con cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d @condition.json
    ```
- **Borrar todos los formatos condicionales** – Elimina todas las reglas de formato condicional de la hoja de cálculo de destino.  
  - **Método:** `DELETE`  
  - **Punto final:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Ejemplo con cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" -H "Authorization: Bearer {access_token}"
    ```
- **Eliminar área de celdas del formato condicional** – Borra un área de celdas previamente definida de una regla de formato condicional.  
  - **Método:** `DELETE`  
  - **Punto final:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **Ejemplo con cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" -H "Authorization: Bearer {access_token}"
    ```
- **Eliminar formato condicional** – Borra una regla completa de formato condicional de la hoja de cálculo.  
  - **Método:** `DELETE`  
  - **Punto final:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **Ejemplo con cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```

Estos ejemplos ilustran el método HTTP requerido, el patrón de URL, los parámetros clave y las cargas útiles de solicitud de ejemplo para cada operación. Si prefiere, puede utilizar el SDK correspondiente (C#, Java, Python, etc.) para obtener fragmentos de código específicos del lenguaje.