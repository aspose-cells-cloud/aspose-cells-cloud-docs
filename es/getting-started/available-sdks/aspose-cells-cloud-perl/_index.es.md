---
title: Aspose.Cells SDK de nube para por
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/available-sdks/aspose-cells-cloud-perl/
description: Aspose.Cells La nube admite Excel para crear, convertir, fusionar, dividir, proteger, operaciones de objetos internos, etc.
weight: 30
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdwon, Perl
---
 El SDK es de código abierto y tiene la licencia MIT. Puede acceder al código fuente de la biblioteca Perl para Aspose.Cells Cloud[aquí](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl).


# **Cómo utilizar la biblioteca Perl de Aspose.Cells Cloud**

Aspose.Cells Cloud SDK para Perl es una potente biblioteca que permite a los desarrolladores manipular y procesar archivos Microsoft Excel utilizando el lenguaje de programación Perl. Con este SDK, puede crear, editar y convertir Excel documentos en la nube, sin instalar software adicional ni dependencias en su máquina local.

En este artículo, exploraremos cómo usar Aspose.Cells Cloud SDK para Perl para realizar algunas tareas comunes, como crear un nuevo libro de trabajo Excel, insertar datos en celdas y guardar el libro de trabajo modificado en la nube.

## Empezando

 Antes de poder comenzar a utilizar el SDK de nube Aspose.Cells para Go, debe configurar su entorno de desarrollo e instalar las dependencias necesarias. Referirse a[el artículo](https://docs.aspose.cloud/cells/quickstart/) en el sitio web Aspose para obtener su ID de cliente y su secreto de cliente.

## Cómo instalar el paquete Perl para Aspose.Cells Cloud

Puede instalar Aspose.Cells Cloud SDK para Perl con el siguiente comando:

```Powershell

perl -MCPAN -e shell

install AsposeCellsCloud::CellsApi

```

## Cómo utilizar el paquete Perl para convertir Xlsx a PDF

- Importar Aspose.Cells Biblioteca en la nube
 Comience importando el paquete necesario del SDK Aspose.Cells Cloud Perl a su proyecto.
- Configurar el cliente API con credenciales
 Autentique su cliente API con su ID de cliente único y su secreto de cliente.
- Preparar parámetros de conversión
 Defina los parámetros para la tarea de conversión, incluido el nombre del archivo fuente, el formato de salida deseado y la ruta de la carpeta de almacenamiento.
- Ejecutar conversión de libro de trabajo
 Invoque el proceso de conversión utilizando el método PostConvertWorkbook y maneje la respuesta.

```Perl
use lib 'lib';
use strict;
use warnings;
use File::Slurp;
use MIME::Base64;
use AsposeCellsCloud::CellsApi;

my $config = AsposeCellsCloud::Configuration->new( client_id => $ENV{'CellsCloudClientId'}, client_secret => $ENV{'CellsCloudClientSecret'});
my $instance = AsposeCellsCloud::CellsApi->new(AsposeCellsCloud::ApiClient->new( $config));

my $remoteFolder = 'TestData/In';
  
my $localName = 'Book1.xlsx';
my $remoteName = 'Book1.xlsx';

my $upload_file_request = AsposeCellsCloud::Request::UploadFileRequest->new( 'UploadFiles'=>{ $localName => $localName  }  ,'path'=>$remoteFolder . '/' . $remoteName );
 
my $format = 'csv';

my $mapFiles = {};           

 $mapFiles->{$localName}= "TestData/".$localName ;

my $request = AsposeCellsCloud::Request::PutConvertWorkbookRequest->new();
$request->{file} =  $mapFiles;
$request->{format} =  $format;
$instance->put_convert_workbook(request=> $request);
```
