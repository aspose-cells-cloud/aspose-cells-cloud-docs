---
title: Fichiers et stockage
second_title: Documen
type: docs
url: /fr/files-and-storage/
aliases: [/working-with-files-and-storage-using-aspose-cells-cloud/]
keywords: Aspose Cells Cloud file storage, upload, download, delete, move, copy file
description: Guide complet sur l'utilisation du Cloud Aspose Cells pour le stockage de fichiers, notamment le téléchargement et la gestion. Le SDK prend en charge divers langages de programmation tels qu'Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 100
kwords: Aspose Cells, Stockage cloud, REST API, Gestion de fichiers, Excel, PDF, CSV, JSON, Markdow
---
 Aspose.Cells Cloud propose des fonctions d'assistance complètes pour gérer les fichiers transférés vers Aspose.Cells Cloud Storage ou tout autre stockage cloud de votre choix. Pour obtenir de l'aide sur la configuration d'un stockage tiers, veuillez consulter[Aspose Rubriques d'aide de l'interface utilisateur Cloud](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

**Aspose.Cells Cloud propose une gamme d'API d'opérations de fichiers, de dossiers et de stockage.**

## **Comment télécharger un fichier**

### Télécharger le fichier API Informations

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| chemin| chaîne| chemin|Chemin d'accès au fichier à télécharger, incluant son nom et son extension (par exemple, /fichier.ext ou /Dossier 1/fichier.ext). Si le contenu est en plusieurs parties et que le chemin d'accès ne contient pas le nom du fichier, il tente de le récupérer à partir du paramètre filename de l'en-tête Content-Disposition.|
| déposer| Déposer| données de formulaire| Fichier à télécharger|
| nom de stockage| chaîne| requête| Nom de stockage|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/File/UploadFile) définit une interface de programmation accessible au public, permettant des interactions REST directement à partir d'un navigateur Web.

### Exemple de téléchargement de fichier

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

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

## **Comment télécharger un fichier**

### Télécharger le fichier API Informations

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| chemin| chaîne| chemin| Chemin du fichier (par exemple, '/folder/file.ext')|
| nom de stockage| chaîne| requête| Nom de stockage|
| versionId| chaîne| requête| ID de la version du fichier à télécharger|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/File/DownloadFile) définit une interface de programmation accessible au public, permettant des interactions REST directement à partir d'un navigateur Web.

### Télécharger un exemple de fichier

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

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

## **Comment supprimer un fichier**

### Supprimer le fichier API Informations

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| chemin| chaîne| chemin| Chemin du fichier (par exemple, '/folder/file.ext')|
| nom de stockage| chaîne| requête| Nom de stockage|
| versionId| chaîne| requête| ID de la version du fichier à supprimer|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/File/DeleteFile) définit une interface de programmation accessible au public, permettant des interactions REST directement à partir d'un navigateur Web.

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

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

## **Comment copier un fichier**

### Copier le fichier API Informations

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| chemin source| chaîne| chemin| Chemin du fichier source (par exemple, '/folder/file.ext')|
|chemin de destination| chaîne| requête| Chemin du fichier de destination|
| srcStorageName| chaîne| requête| Nom du stockage source|
| destStorageName| chaîne| requête| Nom du stockage de destination|
| versionId| chaîne| requête| ID de la version du fichier à copier|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/File/CopyFile) définit une interface de programmation accessible au public, permettant des interactions REST directement à partir d'un navigateur Web.

### Exemple de copie de fichier

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

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

## **Comment déplacer un fichier**

### Déplacer le fichier API Informations

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| chemin source| chaîne| chemin| Chemin du fichier source (par exemple, '/src.ext')|
|chemin de destination| chaîne| requête| Chemin du fichier de destination (par exemple, '/dest.ext')|
| srcStorageName| chaîne| requête| Nom du stockage source|
| destStorageName| chaîne| requête| Nom du stockage de destination|
| versionId| chaîne| requête| ID de la version du fichier à déplacer|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/File/MoveFile) définit une interface de programmation accessible au public, permettant des interactions REST directement à partir d'un navigateur Web.

### Exemple de déplacement de fichier

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

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

## **Comment créer un dossier**

### Créer un dossier API Informations

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| chemin| chaîne| chemin|Chemin du dossier à créer (par exemple, « dossier_1/dossier_2/') |
| nom de stockage| chaîne| requête| Nom de stockage|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) définit une interface de programmation accessible au public, permettant des interactions REST directement à partir d'un navigateur Web.

### Exemple de création de dossier

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

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

## **Comment obtenir des fichiers dans un dossier**

### Obtenir les fichiers API Informations

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| chemin| chaîne| chemin| Chemin du dossier (par exemple, '/folder')|
| nom de stockage| chaîne| requête| Nom de stockage|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) définit une interface de programmation accessible au public, permettant des interactions REST directement à partir d'un navigateur Web.

### Exemple d'obtention de fichiers

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

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

## **Comment supprimer un dossier**

### Supprimer le dossier API Informations

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| chemin| chaîne| chemin| Chemin du dossier (par exemple, '/folder')|
| nom de stockage| chaîne| requête| Nom de stockage|
| récursif| booléen| requête|FAUX|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) définit une interface de programmation accessible au public, permettant des interactions REST directement à partir d'un navigateur Web.

### Exemple de suppression de dossier

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

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

## **Comment copier un dossier**

### Copier le dossier API Informations

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| chemin source| chaîne| chemin| Chemin du dossier source (par exemple, '/src')|
|chemin de destination| chaîne| requête| Chemin du dossier de destination (par exemple, '/dst')|
| srcStorageName| chaîne| requête| Nom du stockage source|
| destStorageName| chaîne| requête| Nom du stockage de destination|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) définit une interface de programmation accessible au public, permettant des interactions REST directement à partir d'un navigateur Web.

### Exemple de copie de dossier

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

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

## **Comment déplacer un dossier**

### Déplacer le dossier API Informations

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| chemin source| chaîne| chemin| Chemin du dossier à déplacer (par exemple, '/folder')|
|chemin de destination| chaîne| requête| Chemin du dossier de destination vers lequel déplacer (par exemple, '/dst')|
| srcStorageName| chaîne| requête| Nom du stockage source|
| destStorageName| chaîne| requête| Nom du stockage de destination|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) définit une interface de programmation accessible au public, permettant des interactions REST directement à partir d'un navigateur Web.

### Exemple de déplacement de dossier

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

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

## **Comment vérifier si le stockage existe**

### Stockage existant API Informations

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| nom de stockage| chaîne| chemin| Nom de stockage|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) définit une interface de programmation accessible au public, permettant des interactions REST directement à partir d'un navigateur Web.

### Exemple de stockage existant

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

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

## **Comment vérifier si un fichier ou un dossier existe**

### L'objet existe API Information

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| chemin| chaîne| chemin| Chemin du fichier ou du dossier (par exemple, « /file.ext » ou « /folder »)|
| nom de stockage| chaîne| requête| Nom de stockage|
| versionId| chaîne| requête| ID de la version du fichier|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) définit une interface de programmation accessible au public, permettant des interactions REST directement à partir d'un navigateur Web.

### Exemple d'objet existant

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

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

## **Comment obtenir l'utilisation du disque**

### Obtenir des informations sur l'utilisation du disque API

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/disc
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| nom de stockage| chaîne| requête| Nom de stockage|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) définit une interface de programmation accessible au public, permettant des interactions REST directement à partir d'un navigateur Web.

### Obtenir un exemple d'utilisation du disque

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

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

## **Comment obtenir les versions des fichiers**

### Obtenir des informations sur les versions de fichiers API

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

Les paramètres de la requête sont :

| Nom du paramètre| Taper| Chemin/Chaîne de requête/Corps HTTP|Description|
|:- |:- |:- |:- |
| chemin| chaîne| chemin| Chemin du fichier (par exemple, '/file.ext')|
| nom de stockage| chaîne| requête| Nom de stockage|

 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) définit une interface de programmation accessible au public, permettant des interactions REST directement à partir d'un navigateur Web.

### Obtenir un exemple de versions de fichiers

Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment appeler le Cloud API avec cURL.

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
