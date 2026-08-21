---
---
title: Eliminar todos los objetos OLE en una hoja de cálculo de Excel
description: Aprenda cómo eliminar todos los objetos OLE de una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye el punto de conexión, parámetros, ejemplos de solicitud/respuesta, fragmentos de SDK, autenticación, manejo de errores y preguntas frecuentes.
keywords: Aspose.Cells Cloud, eliminar objetos OLE, API de Excel, API REST, limpiar OLE en hoja de cálculo, SDK en la nube
api_version: v3.0
last_updated: 2024-11-01
weight: 60
---

# Eliminar todos los objetos OLE en una hoja de cálculo de Excel

**OleObjects – Clear** elimina **todos** los objetos OLE (Object Linking and Embedding, o Enlace e inserción de objetos) de una hoja de cálculo especificada, dejando los datos de las celdas intactos. Esta operación es útil para limpiar hojas de cálculo heredadas o preparar un libro para su redistribución.

---

## Requisitos previos

- Un **token de acceso JWT válido de Aspose Cloud** (OAuth 2.0).  
- El libro de trabajo objetivo debe estar almacenado en el almacenamiento de Aspose Cloud (o debe especificar la `folder`/`storageName` donde se encuentra).  
- Versión de la API **v3.0** o superior.  

> **Nota:** La operación es *idempotente*; llamarla cuando no existen objetos OLE aún devuelve un resultado correcto `200 OK`.

---

## Solicitud HTTP

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### Parámetros de ruta

| Nombre      | Tipo   | Obligatorio | Descripción                          |
|-------------|--------|-------------|--------------------------------------|
| `name`      | string | ✔️          | Nombre del archivo del libro de trabajo. |
| `sheetName` | string | ✔️          | Nombre de la hoja de cálculo.        |

### Parámetros de consulta

| Nombre        | Tipo   | Obligatorio | Descripción                                      |
|---------------|--------|-------------|--------------------------------------------------|
| `folder`      | string | opcional    | Carpeta que contiene el libro de trabajo.        |
| `storageName` | string | opcional    | Nombre del almacenamiento donde se encuentra el libro de trabajo. |

**Cabeceras**

| Cabecera             | Valor                         |
|----------------------|------------------------------|
| `Authorization`      | `Bearer <jwt token>` |
| `Accept`             | `application/json` |
| `Content-Type`       | `application/json` |

---

## Ejemplo de solicitud (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects?folder=Samples&storageName=MyStorage" \
     -X DELETE \
     -H "Authorization: Bearer <jwt token>" \
     -H "Accept: application/json" \
     -H "Content-Type: application/json"
```

*Reemplace `<jwt token>` por un token de acceso válido y ajuste `folder`/`storageName` según sea necesario.*

---

## Respuesta correcta

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                   |
|--------|-----------------------------|---------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o faltante.                               |
| 413    | Carga útil demasiado grande | El archivo cargado supera el límite de tamaño.               |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                              |
---

## Ejemplos de SDK

Los siguientes fragmentos de código muestran cómo invocar **DeleteWorksheetOleObjects** con los SDK oficiales de Aspose.Cells Cloud. Reemplace los valores de marcador de posición (`<YOUR_TOKEN>`, `<FILE_NAME>`, etc.) con sus propios datos.

| Idioma | Ejemplo |
|--------|---------|
| **C#** | <details><summary>Mostrar ejemplo en C#</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar config = new Configuration { AccessToken = "<YOUR_TOKEN>", BasePath = "https://api.aspose.cloud" };\nvar api = new OleObjectsApi(config);\napi.DeleteWorksheetOleObjects(name: "Sample.xlsx", sheetName: "Sheet1", folder: "Samples", storageName: null);\n```</details> |
| **Java** | <details><summary>Mostrar ejemplo en Java</summary>```java\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.client.ApiClient;\nimport com.aspose.cells.cloud.client.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_TOKEN>");\nconfig.setBasePath("https://api.aspose.cloud");\nOleObjectsApi api = new OleObjectsApi(new ApiClient(config));\napi.deleteWorksheetOleObjects("Sample.xlsx", "Sheet1", "Samples", null);\n```</details> |
| **Python** | <details><summary>Mostrar ejemplo en Python</summary>```python\nfrom asposecellscloud import ApiClient, Configuration, OleObjectsApi\n\nconfig = Configuration()\nconfig.access_token = '<YOUR_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\nclient = ApiClient(configuration=config)\napi = OleObjectsApi(client)\napi.delete_worksheet_ole_objects(name='Sample.xlsx', sheet_name='Sheet1', folder='Samples')\n```</details> |
| **Node.js** | <details><summary>Mostrar ejemplo en Node.js</summary>```javascript\nconst { OleObjectsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({ accessToken: '<YOUR_TOKEN>', basePath: 'https://api.aspose.cloud' });\nlet api = new OleObjectsApi(config);\napi.deleteWorksheetOleObjects('Sample.xlsx', 'Sheet1', { folder: 'Samples' })\n  .then(() => console.log('Todos los objetos OLE eliminados'))\n  .catch(err => console.error(err));\n```</details> |
| **Go** | <details><summary>Mostrar ejemplo en Go</summary>```go\npackage main\nimport (\n    "context"\n    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = "<YOUR_TOKEN>"\n    cfg.Host = "https://api.aspose.cloud"\n    api := asposecellscloud.NewOleObjectsApi(cfg)\n    _, err := api.DeleteWorksheetOleObjects(context.Background(), "Sample.xlsx", "Sheet1", map[string]interface{}{ "folder": "Samples" })\n    if err != nil { panic(err) }\n    println("Todos los objetos OLE eliminados")\n}\n```</details> |

*Los archivos fuente completos para todos los idiomas admitidos están disponibles en el [repositorio de GitHub de Aspose.Cells Cloud](https://github.com/aspose-cells-cloud).*

---

## Errores y manejo

- **Idempotencia** – Eliminar objetos OLE en una hoja de cálculo que ya no tiene ninguno sigue devolviendo `200 OK`.  
- **Expiración del token** – Si recibe `401 No autorizado`, obtenga un nuevo token JWT e inténtelo de nuevo.  
- **Nombre de hoja de cálculo no válido** – Asegúrese de que el nombre de la hoja coincida exactamente con la capitalización usada en el libro de trabajo; de lo contrario, se devolverá un `400 Solicitud incorrecta`.  

Implemente lógica de reintento con retroceso exponencial para errores `500` transitorios.

---

## Preguntas frecuentes

**P1: ¿Debo especificar los parámetros `folder` y `storageName`?**  
**R:** No. Si se omiten, Aspose Cloud asume el almacenamiento predeterminado y la carpeta raíz.

**P2: ¿Puedo eliminar objetos OLE solo de una celda específica?**  
**R:** Este punto de conexión elimina **todos** los objetos OLE en la hoja de cálculo. Para eliminar un solo objeto, utilice la operación *Eliminar un objeto OLE específico*.

**P3: ¿Qué ocurre si el libro de trabajo está bloqueado para edición?**  
**R:** La API devolverá un `400 Solicitud incorrecta` con un mensaje que indica que el archivo está bloqueado. Asegúrese de que el archivo no esté abierto en otro lugar antes de llamar al punto de conexión.

**P4: ¿Existe un límite de tamaño para el libro de trabajo?**  
**R:** El servicio sigue los límites generales de tamaño de archivo de Aspose Cloud (actualmente hasta 2 GB por archivo). Los archivos más grandes podrían necesitar dividirse o procesarse en fragmentos.

---

## Prácticas recomendadas

- **Rendimiento** – Use los atributos `async` o `defer` al cargar scripts de terceros en su sitio de documentación para reducir el tiempo de carga inicial de la página.  
- **Seguridad** – Agregue `rel="noopener noreferrer"` a cualquier enlace externo que se abra en una nueva pestaña.  
- **Accesibilidad** – Los iconos decorativos (por ejemplo, flechas hacia abajo en barras laterales) deben tener `alt=""` y `role="presentation"` para cumplir con los estándares WCAG AA.  
- **Consistencia** – Mantenga los formatos de fecha en ISO‑8601 (`YYYY‑MM‑DD`) para evitar artefactos de codificación.  

---

## Operaciones relacionadas

- **Agregar objeto OLE** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`  
- **Eliminar un objeto OLE específico** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  

Utilice los enlaces de navegación al final de la página para moverse entre las acciones relacionadas de la API.