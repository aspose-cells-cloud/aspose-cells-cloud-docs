---
title: "¿Cuál es la diferencia entre el procesamiento de archivos locales y el procesamiento de archivos en la nube en Aspose.Cells Cloud?"
second_title: "Documentación"
ArticleTitle: "¿Cuál es la diferencia entre el procesamiento de archivos locales y el procesamiento de archivos en la nube en Aspose.Cells Cloud?"
linktitle: "Procesamiento de archivos locales frente a procesamiento de archivos en la nube"
type: docs
url: /learn/local-file-processing-vs-cloud-file-processing/
description: "Compare el procesamiento de archivos locales y en la nube de Aspose.Cells Cloud: almacenamiento, costos, seguridad y escenarios típicos. Entienda qué enfoque se adapta mejor a su flujo de trabajo."
keywords: "Aspose.Cells Cloud, procesamiento de archivos locales, procesamiento de archivos en la nube, conversión de hojas de cálculo, API"
weight: 10
---

El procesamiento de archivos locales y el procesamiento de archivos en la nube son paradigmas distintos de gestión de datos, con diferencias significativas en infraestructura de almacenamiento de archivos, procesamiento empresarial, acceso, estructura de costos, seguridad y escenarios aplicables. Las principales diferencias entre ambos enfoques son:

**Requisitos previos:** Antes de utilizar los ejemplos, asegúrese de tener una cuenta válida de Aspose.Cells Cloud, la versión más reciente del SDK instalada, y sus credenciales de Client Id y Client Secret listas para la autenticación.

## 1. Ubicación del almacenamiento de archivos e infraestructura

- Archivos locales:

  - Los archivos se almacenan en dispositivos físicos propiedad o gestionados por el usuario, como el disco duro de una computadora personal, servidores internos o discos duros externos. **Puede apuntar directamente el cliente de Cells Cloud a un archivo ubicado en cualquier dispositivo de almacenamiento local.**
  - El cliente tiene control total y físico sobre el hardware.
  - La compra, mantenimiento, actualización y retiro de la infraestructura es responsabilidad del usuario o su organización.

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest

# Inicializar CellsApi
api = CellsApi('YourCellsCloudClientId', 'YourCellsCloudClientSecret')

# Convertir archivo Excel local a PDF
api.convert_spreadsheet(
    ConvertSpreadsheetRequest('D:\\Data\\BookSales.xlsx', "pdf"),
    local_outpath="BookSales.pdf"
)
```

**Referencia de la API – Convertir hoja de cálculo**

| Método                | Verbo HTTP | Punto de conexión    | Parámetros (clave)                                   | Respuestas                                       |
|-----------------------|------------|----------------------|-------------------------------------------------------|--------------------------------------------------|
| `convert_spreadsheet` | POST       | `/cells/convert`     | `inputFile` – ruta al archivo fuente<br>`format` – formato de destino (por ejemplo, `pdf`) | `200 OK` – conversión exitosa<br>`400 Bad Request` – parámetros inválidos<br>`401 Unauthorized` – fallo de autenticación |

- Archivos en la nube:

  - Los archivos se almacenan en centros de datos remotos operados por proveedores de servicios en la nube de terceros (almacenamiento en la nube de Aspose, Dropbox, AWS, Google Cloud, Microsoft Azure). **AWS, Dropbox, Google Cloud y Microsoft Azure pueden conectarse todos al almacenamiento en la nube de Aspose.**
  - Los clientes acceden a estos archivos a través de Internet, independientemente de la ubicación y el mantenimiento del hardware subyacente.
  - La infraestructura es responsabilidad del proveedor del servicio en la nube, y los usuarios la utilizan bajo demanda.

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import (
    UploadFileRequest,
    ExportSpreadsheetAsFormatRequest,
    SaveSpreadsheet_asRequest,
)

# Inicializar CellsApi
api = CellsApi('YourCellsCloudClientId', 'YourCellsCloudClientSecret')

# Subir archivo local al almacenamiento en la nube
api.upload_file(
    UploadFileRequest(
        "D:\\Data\\EmployeeSalesSummary.xlsx",
        "PythonSDK/EmployeeSalesSummary.xlsx"
    )
)

# Exportar archivo en la nube a un archivo en formato especificado hacia almacenamiento local
api.export_spreadsheet_as_format(
    ExportSpreadsheetAsFormatRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder="PythonSDK"
    ),
    local_outpath="D:\\DataOutput\\EmployeeSalesSummary.pdf"
)

# Definir la carpeta remota (reemplace con su nombre de carpeta real si es diferente)
RemoteFolder = "PythonSDK"

# Guardar un archivo Excel de Cells Cloud como otro formato de archivo en Cells Cloud
api.save_spreadsheet_as(
    SaveSpreadsheetAsRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder=RemoteFolder
    )
)
```

**Referencia de la API – Operaciones con archivos en la nube**

| Método                        | Verbo HTTP | Punto de conexión           | Parámetros (clave)                                                                                   | Respuestas                                      |
|-------------------------------|------------|-----------------------------|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| `upload_file`                 | PUT        | `/cells/storage/file`       | `localPath` – ruta del archivo local<br>`remotePath` – destino en almacenamiento en la nube          | `200 OK` – subida exitosa<br>`401 Unauthorized` |
| `export_spreadsheet_as_format` | POST       | `/cells/{name}/export`      | `name` – nombre del archivo en la nube<br>`format` – formato de destino (por ejemplo, `pdf`)<br>`folder` – carpeta opcional | `200 OK` – exportación exitosa<br>`400 Bad Request` |
| `save_spreadsheet_as`         | POST       | `/cells/{name}/saveas`      | `name` – nombre del archivo en la nube<br>`format` – formato de destino<br>`folder` – carpeta de destino | `200 OK` – guardado exitoso<br>`401 Unauthorized` |

## 2. Procesamiento empresarial

Independientemente de si se trata de procesamiento de archivos locales o en la nube, todo el procesamiento empresarial se completa en el servidor de Cells Cloud, **por lo tanto se requiere soporte de Internet**.

## 3. Acceso a los datos

- Procesamiento de archivos locales:

  - El acceso suele estar limitado al propio dispositivo.
  - La colaboración multiusuario es difícil.
  - Inconveniencia al cambiar de equipo o ubicación.

- Procesamiento de archivos en la nube:

  - Acceda a los archivos desde cualquier dispositivo (computadora, teléfono, tableta) en cualquier momento y lugar, siempre que cuente con conexión a Internet.
  - Soporte natural para colaboración en tiempo real multiusuario; múltiples usuarios pueden editar el mismo documento simultáneamente, y el sistema gestiona automáticamente el control de versiones.
  - Alta movilidad, soporte flexible para oficina y trabajo remoto.

## 4. Estructura de costos y seguridad

- Archivos locales:

  - Requiere una inversión elevada en etapas iniciales. Esto origina costos adicionales para el soporte operativo posterior.
  - La seguridad física y la seguridad de red son controladas por los propios usuarios.

- Archivos en la nube:

  - Baja inversión inicial, principalmente gastos operativos, con modelo de pago por uso.
  - La seguridad e integridad son responsabilidad del proveedor del servicio en la nube.

## 5. Escenarios aplicables

- Archivos locales: Las operaciones con archivos solo pueden realizarse localmente.  
- Archivos en la nube: Las operaciones con archivos pueden realizarse localmente o en la nube.  

**Notas / Limitaciones:** La API admite archivos de hasta 200 MB para el procesamiento en la nube, y solo pueden convertirse los formatos indicados en la documentación. La latencia de red puede afectar el tiempo de procesamiento para hojas de cálculo grandes.

_Ultima actualización: 30 de julio de 2026_