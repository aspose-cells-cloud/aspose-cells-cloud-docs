---
title: ¿Cuál es la diferencia entre el procesamiento de archivos local y el procesamiento de archivos en la nube en Aspose.Cells Cloud?
second_title: Documen
ArticleTitle: What is the difference between local file processing and cloud file processing in Aspose.Cells Cloud
linktitle: Procesamiento de archivos local vs. procesamiento de archivos en la nube
type: docs
url: /es/learn/local-file-processing-vs-cloud-file-processing/
description: ¿Cuál es la diferencia entre el procesamiento de archivos local y el procesamiento de archivos en la nube? El procesamiento de archivos local y el procesamiento de archivos en la nube son dos paradigmas de gestión de datos fundamentalmente diferentes, con diferencias significativas en la infraestructura de almacenamiento, el procesamiento empresarial, el acceso, la estructura de costos, la seguridad y los escenarios aplicables.
weight: 10
kwords: Excel Nube API, REST, Hoja de cálculo, PDF, CSV, JSON, Markdown, Procesamiento de archivos local vs. Procesamiento de archivos en la nube
---
El procesamiento local de archivos y el procesamiento en la nube son paradigmas de gestión de datos diferentes, con diferencias significativas en la infraestructura de almacenamiento de archivos, el procesamiento empresarial, el acceso, la estructura de costos, la seguridad y los escenarios aplicables. Las principales diferencias entre ambos son:

## 1. Ubicación e infraestructura de almacenamiento de archivos

- Archivo local:

Los archivos se almacenan en dispositivos físicos que el usuario posee o administra, como el disco duro de una computadora personal, servidores internos o discos duros externos. El cliente de la nube Cells puede acceder directamente a estos dispositivos.
 - El cliente tiene control físico completo sobre el hardware.
 - La compra, mantenimiento, actualización y retiro de la infraestructura es responsabilidad del usuario o su organización.

```Python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest
# Initialize CellsApi
api  = CellsApi('YourCellsCloudClientId','YourCellsCloudClientSecret')
# Convert Local Excel file to PDF
api.convert_spreadsheet( ConvertSpreadsheetRequest( 'D:\\Data\\BookSales.xlsx', "pdf" ) , local_outpath = "BookSales.pdf")

```

- Archivo en la nube:

 Los archivos se almacenan en centros de datos remotos operados por proveedores externos de servicios en la nube (almacenamiento en la nube Aspose, Dropbox, AWS, Google Cloud, Microsoft Azure). AWS, Dropbox, Google Cloud y Microsoft Azure pueden conectar a usuarios al almacenamiento en la nube Aspose.
 - Los clientes acceden a estos archivos a través de Internet, independientemente de la ubicación y el mantenimiento del hardware subyacente.
 - La infraestructura es responsabilidad del proveedor de servicios en la nube y los usuarios la utilizan según demanda.

```Python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import UploadFileRequest, ExportSpreadsheetAsFormatRequest, SaveSpreadsheetAsRequest
# Initialize CellsApi
api  = CellsApi('YourCellsCloudClientId','YourCellsCloudClientSecret')
# Upload local file to cloud storage
api.upload_file( UploadFileRequest("D:\\Data\\EmployeeSalesSummary.xlsx", "PythonSDK/EmployeeSalesSummary.xlsx"))
# Export cloud file to specified format file to local storage
api.export_spreadsheet_as_format( ExportSpreadsheetAsFormatRequest( "EmployeeSalesSummary.xlsx","pdf" ,folder= "PythonSDK"  ) , local_outpath="D:\\DataOutput\\EmployeeSalesSummary.pdf" )
# Or Save an Excel file of Cells Cloud as another format file of Cells Cloud. 
api.save_spreadsheet_as( SaveSpreadsheetAsRequest (  "EmployeeSalesSummary.xlsx","pdf" ,folder= RemoteFolder ) )

```

## 2. Procesamiento empresarial

Independientemente del procesamiento de archivos local o en la nube, todo el procesamiento comercial se completa en el servidor en la nube Cells.**Por lo tanto, se requiere soporte de Internet.**.

## 3. Acceso a los datos

- Procesamiento de archivos locales:

 - El acceso normalmente está limitado al propio dispositivo.
 - La colaboración entre varias personas es difícil.
 - Inconvenientes en el cambio de equipo o ubicación.

- Procesamiento de archivos en la nube:

 - Acceda a archivos desde cualquier dispositivo (computadora, teléfono, tableta) en cualquier momento y en cualquier lugar, siempre que tenga una conexión a Internet.
 - Soporte natural para la colaboración en tiempo real de varias personas, varios usuarios pueden editar el mismo documento al mismo tiempo, el sistema maneja automáticamente el control de versiones.
 - Fuerte movilidad, soporte flexible office y trabajo remoto.
  
## 4. Estructura de costos y seguridad

- Archivo local:
  
 - Un alto gasto de capital en la etapa inicial requiere ciertos costos de soporte operativo en la etapa posterior.
 Tanto la seguridad física como la seguridad de la red están controladas por los propios usuarios.

- Archivo en la nube:

 - Baja inversión inicial, principalmente gastos operativos, pago a pedido.
 - La seguridad y la integridad son responsabilidad del proveedor de servicios en la nube.

## 5. Escenarios aplicables

- Archivo local: Las operaciones de archivo solo se pueden realizar localmente.
- Archivo en la nube: las operaciones con archivos se pueden realizar localmente o en la nube.
