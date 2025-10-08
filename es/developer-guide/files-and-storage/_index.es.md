---
title: Archivos y almacenamiento
second_title: Documen
type: docs
url: /es/files-and-storage/
aliases: [/working-with-files-and-storage-using-aspose-cells-cloud/]
keywords: Aspose Cells Cloud file storage, upload, download, delete, move, copy file
description: Guía completa sobre el uso de Aspose Cells Cloud para operaciones de almacenamiento de archivos, incluyendo la carga, descarga y gestión de archivos. SDK compatible con diversos lenguajes de programación como Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 100
kwords: Aspose Cells, Almacenamiento en la nube, REST API, Gestión de archivos, Excel, PDF, CSV, JSON, Markdow
---
 Aspose.Cells Cloud ofrece funciones de ayuda completas para trabajar con archivos subidos a Aspose.Cells Cloud Storage o a cualquier otro almacenamiento en la nube de su elección. Para obtener ayuda con la configuración de almacenamiento de terceros, consulte[Aspose Temas de ayuda de la interfaz de usuario en la nube](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

**Aspose.Cells Cloud ofrece una gama de API de operaciones de archivos, carpetas y almacenamiento.**

## **Cómo subir un archivo**

### Subir archivo API Información

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| camino| cadena| camino|Ruta para subir el archivo, incluyendo el nombre y la extensión (p. ej., /file.ext o /Folder 1/file.ext). Si el contenido es multiparte y la ruta no contiene el nombre del archivo, se intenta recuperarlo del parámetro filename en el encabezado Content-Disposition.|
| archivo| Archivo| datos del formulario| Archivo para cargar|
| nombreDeAlmacenamiento| cadena| consulta| Nombre de almacenamiento|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/File/UploadFile) define una interfaz de programación de acceso público, que permite interacciones REST directamente desde un navegador web.

### Ejemplo de carga de archivo

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la nube API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-d {"File":{}}
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
} 
```

{{< /tab >}}
{{< /tabs >}}

## **Cómo descargar un archivo**

### Descargar Archivo API Información

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| camino| cadena| camino| Ruta del archivo (por ejemplo, '/carpeta/archivo.ext')|
| nombreDeAlmacenamiento| cadena| consulta| Nombre de almacenamiento|
| ID de versión| cadena| consulta| ID de la versión del archivo para descargar|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/File/DownloadFile) define una interfaz de programación de acceso público, que permite interacciones REST directamente desde un navegador web.

### Ejemplo de archivo de descarga

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la nube API con cURL.

{{< tabs tabTotal="2" tabID="13" tabName13="Request" tabName14="Response" >}}
{{< tab tabNum="13" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="14" >}}

```bash
{
    Stream
}
```

{{< /tab >}}
{{< /tabs >}}

## **Cómo eliminar un archivo**

### Eliminar archivo API Información

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| camino| cadena| camino| Ruta del archivo (por ejemplo, '/carpeta/archivo.ext')|
| nombreDeAlmacenamiento| cadena| consulta| Nombre de almacenamiento|
| ID de versión| cadena| consulta| ID de la versión del archivo a eliminar|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/File/DeleteFile) define una interfaz de programación de acceso público, que permite interacciones REST directamente desde un navegador web.

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la nube API con cURL.

{{< tabs tabTotal="2" tabID="15" tabName15="Request" tabName16="Response" >}}
{{< tab tabNum="15" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/book12.xlsx" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="16" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Cómo copiar un archivo**

### Copiar Archivo API Información

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| ruta de origen| cadena| camino| Ruta del archivo de origen (por ejemplo, '/carpeta/archivo.ext')|
|ruta de destino| cadena| consulta| Ruta del archivo de destino|
| nombreDeAlmacenamientoOrigen| cadena| consulta| Nombre del almacenamiento de origen|
| nombreDeAlmacenamientoDeDestino| cadena| consulta| Nombre del almacenamiento de destino|
| ID de versión| cadena| consulta| ID de la versión del archivo a copiar|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/File/CopyFile) define una interfaz de programación de acceso público, que permite interacciones REST directamente desde un navegador web.

### Ejemplo de copia de archivo

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la nube API con cURL.

{{< tabs tabTotal="2" tabID="17" tabName17="Request" tabName18="Response" >}}

{{< tab tabNum="17" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/copy/Book1.xlsx?destPath=Book2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="18" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Cómo mover un archivo**

### Mover archivo API Información

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| ruta de origen| cadena| camino| Ruta del archivo de origen (por ejemplo, '/src.ext')|
|ruta de destino| cadena| consulta| Ruta del archivo de destino (por ejemplo, '/dest.ext')|
| nombreDeAlmacenamientoOrigen| cadena| consulta| Nombre del almacenamiento de origen|
| nombreDeAlmacenamientoDeDestino| cadena| consulta| Nombre del almacenamiento de destino|
| ID de versión| cadena| consulta| ID de la versión del archivo a mover|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/File/MoveFile) define una interfaz de programación de acceso público, que permite interacciones REST directamente desde un navegador web.

### Ejemplo de mover archivo

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la nube API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/move/Book2.xlsx?destPath=MoveBook2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Cómo crear una carpeta**

### Crear carpeta API Información

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| camino| cadena| camino|Ruta de la carpeta a crear (por ejemplo, 'carpeta_1/carpeta_2/') |
| nombreDeAlmacenamiento| cadena| consulta| Nombre de almacenamiento|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) define una interfaz de programación de acceso público, que permite interacciones REST directamente desde un navegador web.

### Ejemplo de creación de carpeta

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la nube API con cURL.

{{< tabs tabTotal="2" tabID="3" tabName3="Request" tabName4="Response" >}}
{{< tab tabNum="3" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/newfolder" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

## **Cómo obtener archivos en una carpeta**

### Obtener archivos API Información

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| camino| cadena| camino| Ruta de la carpeta (por ejemplo, '/carpeta')|
| nombreDeAlmacenamiento| cadena| consulta| Nombre de almacenamiento|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) define una interfaz de programación de acceso público, que permite interacciones REST directamente desde un navegador web.

### Ejemplo de obtención de archivos

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la nube API con cURL.

{{< tabs tabTotal="2" tabID="5" tabName5="Request" tabName6="Response" >}}
{{< tab tabNum="5" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 0,
      "Path": "string"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

## **Cómo eliminar una carpeta**

### Eliminar carpeta API Información

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| camino| cadena| camino| Ruta de la carpeta (por ejemplo, '/carpeta')|
| nombreDeAlmacenamiento| cadena| consulta| Nombre de almacenamiento|
| recursivo| booleano| consulta|FALSO|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) define una interfaz de programación de acceso público, que permite interacciones REST directamente desde un navegador web.

### Ejemplo de eliminar carpeta

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la nube API con cURL.

{{< tabs tabTotal="2" tabID="7" tabName7="Request" tabName8="Response" >}}

{{< tab tabNum="7" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Cómo copiar una carpeta**

### Copiar Carpeta API Información

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| ruta de origen| cadena| camino| Ruta de la carpeta de origen (por ejemplo, '/src')|
|ruta de destino| cadena| consulta| Ruta de la carpeta de destino (por ejemplo, '/dst')|
| nombreDeAlmacenamientoOrigen| cadena| consulta| Nombre del almacenamiento de origen|
| nombreDeAlmacenamientoDeDestino| cadena| consulta| Nombre del almacenamiento de destino|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) define una interfaz de programación de acceso público, que permite interacciones REST directamente desde un navegador web.

### Ejemplo de copia de carpeta

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la nube API con cURL.

{{< tabs tabTotal="2" tabID="21" tabName21="Request" tabName22="Response" >}}
{{< tab tabNum="21" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/copy/srcfolder?destPath=desfolder" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="22" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Cómo mover una carpeta**

### Mover carpeta API Información

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| ruta de origen| cadena| camino| Ruta de la carpeta a mover (por ejemplo, '/carpeta')|
|ruta de destino| cadena| consulta| Ruta de la carpeta de destino a la que moverse (por ejemplo, '/dst')|
| nombreDeAlmacenamientoOrigen| cadena| consulta| Nombre del almacenamiento de origen|
| nombreDeAlmacenamientoDeDestino| cadena| consulta| Nombre del almacenamiento de destino|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) define una interfaz de programación de acceso público, que permite interacciones REST directamente desde un navegador web.

### Ejemplo de mover carpeta

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la nube API con cURL.

{{< tabs tabTotal="2" tabID="23" tabName23="Request" tabName24="Response" >}}
{{< tab tabNum="23" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/move/desfolder" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabnum="24" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Cómo comprobar si existe almacenamiento**

### Existe almacenamiento API Información

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| nombreDeAlmacenamiento| cadena| camino| Nombre de almacenamiento|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) define una interfaz de programación de acceso público, que permite interacciones REST directamente desde un navegador web.

### Ejemplo de existencia de almacenamiento

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la nube API con cURL.

{{< tabs tabTotal="2" tabID="33" tabName33="Request" tabName34="Response" >}}
{{< tab tabNum="33" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="34" >}}

```bash
{
  "Exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

## **Cómo comprobar si existe un archivo o una carpeta**

### El objeto existe API Información

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| camino| cadena| camino| Ruta de archivo o carpeta (por ejemplo, '/file.ext' o '/folder')|
| nombreDeAlmacenamiento| cadena| consulta| Nombre de almacenamiento|
| ID de versión| cadena| consulta| ID de la versión del archivo|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) define una interfaz de programación de acceso público, que permite interacciones REST directamente desde un navegador web.

### Ejemplo de objeto existente

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la nube API con cURL.

{{< tabs tabTotal="2" tabID="37" tabName37="Request" tabName38="Response" >}}
{{< tab tabNum="37" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="38" >}}

```bash
{
  "Exists": true,
  "IsFolder": false
}
```

{{< /tab >}}
{{< /tabs >}}

## **Cómo obtener el uso del disco**

### Obtener información sobre el uso del disco API

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/disc
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| nombreDeAlmacenamiento| cadena| consulta| Nombre de almacenamiento|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) define una interfaz de programación de acceso público, que permite interacciones REST directamente desde un navegador web.

### Obtener ejemplo de uso del disco

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la nube API con cURL.

{{< tabs tabTotal="2" tabID="40" tabName40="Request" tabName41="Response" >}}

{{< tab tabNum="40" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/disc" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="41" >}}

```bash
{
  "UsedSize": 0,
  "TotalSize": 0
}
```

{{< /tab >}}
{{< /tabs >}}

## **Cómo obtener versiones de archivos**

### Obtener información de las versiones del archivo API

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| camino| cadena| camino| Ruta del archivo (por ejemplo, '/file.ext')|
| nombreDeAlmacenamiento| cadena| consulta| Nombre de almacenamiento|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) define una interfaz de programación de acceso público, que permite interacciones REST directamente desde un navegador web.

### Ejemplo de obtención de versiones de archivos

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la nube API con cURL.

{{< tabs tabTotal="2" tabID="46" tabName46="Request" tabName47="Response" >}}
{{< tab tabNum="46" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabnum="47" >}}

```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 0,
      "Path": "string",
      "VersionId": "string",
      "IsLatest": true
    }
  ]
} 
```

{{< /tab >}}
{{< /tabs >}}
