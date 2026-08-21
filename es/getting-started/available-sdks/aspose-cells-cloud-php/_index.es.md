---
title: "Aspose.Cells Cloud PHP SDK – Convertir, fusionar, dividir y proteger archivos de Excel"  
second_title: "Documento"  
ArticleTitle: "Aspose.Cells Cloud PHP SDK – Convertir, fusionar, dividir y proteger archivos de Excel"  
linktitle: "Aspose.Cells Cloud PHP SDK"  
type: docs  
url: /es/available-sdks/aspose-cells-cloud-php/
description: "Descargue el SDK de Aspose.Cells Cloud para PHP (v24.3). Aprenda cómo instalarlo mediante Composer, autenticarse, convertir XLSX a PDF/CSV, fusionar libros de trabajo, proteger hojas y más, todo sin instalar Office."  
keywords: "Aspose.Cells, Cloud, PHP, SDK, Excel, Convertir, Fusionar, Dividir, Proteger"  
weight: 30  
---  

El SDK es de código abierto y está bajo la licencia MIT. Puede acceder al código fuente de la librería PHP para Aspose.Cells Cloud <a href="https://github.com/aspose-cells-cloud/aspose-cells-cloud-php" target="_blank" rel="noopener noreferrer">aquí</a>.

# **Cómo utilizar Aspose.Cells Cloud SDK para PHP**

Aspose.Cells Cloud SDK para PHP es una potente librería que permite a los desarrolladores manipular y procesar archivos de Microsoft Excel utilizando el **lenguaje de programación PHP**. Con este SDK, puede crear, editar y convertir documentos de Excel en la nube, sin necesidad de instalar software adicional ni dependencias en su máquina local.

En este artículo, exploraremos cómo utilizar Aspose.Cells Cloud SDK para PHP para llevar a cabo tareas comunes, como crear un nuevo libro de trabajo de Excel, insertar datos en celdas y guardar el libro de trabajo modificado en la nube.

## Primeros pasos

Antes de comenzar a utilizar Aspose.Cells Cloud SDK para **PHP**, debe configurar su entorno de desarrollo e instalar las dependencias necesarias. Consulte <a href="https://docs.aspose.cloud/cells/quickstart/" target="_blank" rel="noopener noreferrer">el artículo</a> en el sitio web de Aspose para obtener su ID de cliente y secreto de cliente.

**Requisitos previos**

- PHP 7.4 o posterior  
- Composer instalado en su máquina de desarrollo  
- ID de cliente y secreto de cliente válidos de Aspose Cloud  
- Acceso a una ubicación de almacenamiento de Aspose Cloud (predeterminada o personalizada)  

## Cómo instalar el paquete PHP para Aspose.Cells Cloud

Puede instalar el SDK de Aspose.Cells Cloud para PHP. A continuación se presentan los pasos:

- Agregue Aspose.Cells Cloud como una dependencia en su archivo `composer.json`:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- Ejecute Composer update para instalar el SDK:

   ```bash
   composer install
   ```

- Incluya el cargador automático de Composer en su código PHP:

   ```php
   require 'vendor/autoload.php';
   ```

## Cómo utilizar el paquete PHP para convertir Xlsx a otros formatos

- Importar la librería Aspose.Cells Cloud  
  Comience importando el paquete necesario del SDK de Aspose.Cells Cloud para PHP en su proyecto.

- Configurar el cliente de la API con credenciales  
  Autentique su cliente de API con su ID único de cliente y secreto de cliente.

- Preparar los parámetros de conversión  
  Defina los parámetros para la tarea de conversión, incluyendo el nombre del archivo de origen, el formato de salida deseado y la ruta de la carpeta de almacenamiento.

- Ejecutar la conversión del libro de trabajo  
  invoque el proceso de conversión mediante el método `PostConvertWorkbook` y maneje la respuesta.

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}

### Referencia de la API para `PostConvertWorkbook`

| Parámetro      | Descripción                                            | Tipo   | Obligatorio |
|----------------|--------------------------------------------------------|--------|-------------|
| `file`         | Nombre del archivo de Excel de origen (p. ej., `sample.xlsx`). | string | Sí |
| `format`       | Formato de salida deseado (`pdf`, `csv`, `png`, etc.). | string | Sí |
| `storage`      | Nombre del almacenamiento o ruta de la carpeta donde se encuentra el archivo de origen. | string | No |
| `outPath`      | Ruta opcional para guardar directamente el archivo convertido en el almacenamiento. | string | No |

**Método HTTP:** POST  
**Punto de conexión:** `/cells/convert/{format}`  

**Ejemplo de respuesta (JSON)**  

```json
{
  "status": "OK",
  "url": "https://api.aspose.cloud/v3.0/cells/convert/output.pdf"
}
```

**Códigos de estado**

- `200` – Conversión exitosa.  
- `400` – Solicitud incorrecta (parámetros faltantes o no válidos).  
- `401` – Autenticación fallida.  
- `500` – Error del servidor.  
---