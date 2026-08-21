---
title: "Agregar o eliminar la imagen de fondo de hoja de cálculo – API de Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Fondo"
type: docs
url: /worksheets/background/
keywords: "Aspose.Cells Cloud, fondo de hoja de cálculo, API de Excel, agregar imagen de fondo, eliminar fondo de hoja de cálculo, ejemplos de SDK"
description: "Aprenda cómo agregar o eliminar una imagen de fondo en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye sintaxis de solicitud, ejemplos de SDK para Java, .NET, Python, PHP y manejo de errores."
weight: 20
ArticleTitle: "Agregar o eliminar la imagen de fondo de hoja de cálculo con la API de Aspose.Cells Cloud"
---

## Trabajar con el fondo en una hoja de cálculo de Excel

**Resumen:** Un fondo de hoja de cálculo es una imagen que aparece detrás de las celdas de una hoja, útil para marcas corporativas o indicadores visuales. La API de Aspose.Cells Cloud le permite agregar o eliminar esta imagen de fondo mediante programación.

**Prerrequisitos:**  
- Token de acceso válido de Aspose.Cells Cloud (OAuth 2.0).  
- Un libro de Excel almacenado en la nube.  
- Un archivo de imagen (PNG, JPEG, BMP) para usar como fondo.

- **Agregar fondo** – Establecer una imagen de fondo en una hoja de cálculo. Consulte la guía detallada [Cómo establecer el fondo en una hoja de cálculo de Excel](/cells/worksheets/background/add/).  
- **Eliminar fondo** – Eliminar una imagen de fondo existente de una hoja de cálculo. Consulte la guía detallada [Cómo eliminar el fondo en una hoja de cálculo de Excel](/cells/worksheets/background/delete/).

Utilizar un fondo en la hoja de cálculo puede mejorar la identidad corporativa, resaltar secciones importantes o proporcionar indicadores visuales para los usuarios finales. La API de Aspose.Cells Cloud facilita configurar o borrar esta imagen de fondo directamente desde su aplicación.

### Referencia de la API

| Operación | Método HTTP | Punto de conexión | Parámetros de ruta | Cuerpo de la solicitud | Respuesta correcta |
|-----------|-------------|-------------------|-------------------|------------------------|--------------------|
| Agregar fondo | PUT | `/cells/{name}/worksheets/{sheetName}/background` | `name` – nombre del archivo del libro<br>`sheetName` – hoja de cálculo de destino | Archivo de imagen (PNG, JPEG, BMP) como multipart/form‑data | `200 OK` – fondo aplicado |
| Eliminar fondo | DELETE | `/cells/{name}/worksheets/{sheetName}/background` | `name` – nombre del archivo del libro<br>`sheetName` – hoja de cálculo de destino | *ninguno* | `200 OK` – fondo eliminado |

#### Ejemplo (SDK de Java)

```java
// Agregar una imagen de fondo
CellsApi cellsApi = new CellsApi("client_id", "client_secret");
File image = new File("ruta/a/fondo.png");
cellsApi.putWorksheetBackground("Book1.xlsx", "Sheet1", image, null);

// Eliminar la imagen de fondo
cellsApi.deleteWorksheetBackground("Book1.xlsx", "Sheet1", null);
```

#### Ejemplo (SDK de Python)

```python
import asposecellscloud
api = asposecellscloud.CellsApi(client_id="SU_ID_DE_CLIENTE", client_secret="SU_CLAVE_DE_CLIENTE")

# Agregar fondo
with open("fondo.png", "rb") as img:
    api.put_worksheet_background("Book1.xlsx", "Sheet1", img)

# Eliminar fondo
api.delete_worksheet_background("Book1.xlsx", "Sheet1")
```

Para ejemplos adicionales en otros lenguajes (C#, PHP, Ruby), consulte la documentación de los SDK.

**Temas relacionados**  
- Obtenga más información sobre la gestión general de hojas de cálculo: [Resumen de hojas de cálculo](/cells/worksheets/).  
- Aprenda cómo autenticarse con Aspose.Cells Cloud: [Guía de autenticación de la API](/cells/authentication/).  
- Explore otros elementos de hojas de cálculo, como gráficos, tablas y fórmulas: [Índice de elementos de hojas de cálculo](/cells/elements/).
---