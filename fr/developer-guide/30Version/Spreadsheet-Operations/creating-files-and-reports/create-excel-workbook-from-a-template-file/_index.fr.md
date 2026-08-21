---
title: "Comment créer un classeur Excel à l'aide d'un fichier modèle"
second_title: "Document"
linktitle: "Fichier modèle"
type: docs
url: /fr/create-an-excel-file-with-template-file/
aliases:
  - /create-excel-workbook-from-a-template-file/
  - /workbook/new-from-a-template-file/
  - /workbook/create/template-file/
keywords: "Excel, modèle, API, Aspose.Cells, classeur, REST, Cloud"
description: "Découvrez comment générer des classeurs Excel à partir de fichiers modèles à l’aide de l’API REST Aspose.Cells Cloud. Inclut les conditions préalables, les étapes d’authentification, des exemples cURL, des détails sur la gestion des erreurs et des extraits de code SDK."
weight: 30
---

# Comment créer un classeur Excel à l’aide d’un fichier modèle

Créez un nouveau classeur Excel à partir d’un fichier modèle existant et, éventuellement, d’un fichier de données fournissant les valeurs des marqueurs intelligents (Smart‑Markers). Cette opération est réalisée via le point de terminaison **PUT** `/cells/{name}` de Aspose.Cells Cloud.

---

## Conditions préalables

| Exigence | Description |
|----------|-------------|
| **Compte Aspose.Cells Cloud** | Inscrivez-vous sur https://dashboard.aspose.cloud/ et obtenez un **Client Id** / **Client Secret**. |
| **Jeton d’accès JWT** | Générez un jeton JWT conformément au guide d’[authentification](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Fichier modèle** | Téléversez le fichier Excel modèle (par exemple, `Calendar.xlsx`) vers votre stockage choisi à l’aide de l’API **Upload File** ou de l’interface utilisateur. |
| **Fichier de données (facultatif)** | Un fichier JSON ou XML contenant les valeurs des marqueurs intelligents (par exemple, `Sample_Data.xml`). |
| **Stockage pris en charge** | Stockage par défaut (`Default`) ou stockage personnalisé configuré dans votre compte Aspose. |

---

## Authentification

Toutes les requêtes vers Aspose.Cells Cloud exigent un **jeton JWT Bearer** transmis dans l’en-tête `Authorization` :

```http
Authorization: Bearer {access_token}
```

Le jeton doit être obtenu au préalable et est valide par défaut pendant une heure.

---

## Requête

### Requête HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

| Composant | Valeur |
|-----------|--------|
| **Méthode** | `PUT` |
| **Chemin** | `/cells/{name}` – `name` correspond au nom souhaité du nouveau classeur (y compris l’extension, par exemple `newworkbook.xlsx`). |
| **Content‑Type** | `multipart/form-data` (lorsqu’un fichier de données est envoyé dans le corps de la requête). |
| **Accept** | `application/json` |

### Paramètre de chemin

| Nom | Type | Obligatoire | Description |
|-----|------|-------------|-------------|
| `name` | string | **Oui** | Nom du classeur à créer (par exemple, `newworkbook.xlsx`). |

### Paramètres de requête

| Paramètre | Type | Obligatoire | Valeur par défaut | Description |
|-----------|------|-------------|-------------------|-------------|
| `templateFile` | string | Non | — | Nom du fichier modèle stocké dans le cloud. |
| `dataFile` | string | Non | — | Nom du fichier de données (XML ou JSON) stocké dans le cloud. |
| `isWriteOver` | boolean | Non | `false` | Écraser le fichier cible s’il existe déjà. Passer `true` ou `false` **sans** guillemets. |
| `folder` | string | Non | — | Chemin du dossier où réside le modèle (et éventuellement le fichier de données). |
| `storageName` | string | Non | — | Nom du service de stockage contenant les fichiers. |
| `checkExcelRestriction` | boolean | Non | `true` | Valider le classeur par rapport aux restrictions Excel avant sa création. |

### Corps de la requête (facultatif)

Lorsque les données des placeholders des marqueurs intelligents sont envoyées directement dans la requête, incluez-les en tant que pièce jointe multipart nommée **`data`**.

| Nom de la pièce | Type | Description |
|-----------------|------|-------------|
| `data` | file | Fichier XML ou JSON contenant les valeurs des marqueurs intelligents. |

#### Exemple cURL avec corps de requête

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&isWriteOver=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "data=@Sample_Data.xml"
```

*Si le paramètre de requête `dataFile` est utilisé au lieu d’un corps multipart, omettez l’option `-F`.*

---

## Réponse

Un appel réussi renvoie un code **`200 OK`** (ou **`201 Created`** lorsqu’un nouveau fichier est généré) accompagné d’une charge utile JSON décrivant le classeur créé.

```json
{
    "Code": 200,
    "Status": "OK",
    "File": {
        "Name": "newworkbook.xlsx",
        "Size": 18234,
        "Path": "output/newworkbook.xlsx",
        "Url": "https://api.aspose.cloud/v3.0/storage/file/output/newworkbook.xlsx"
    }
}
```

### Types de données de réponse

| Propriété | Type | Description |
|-----------|------|-------------|
| `Code` | integer | Code de statut HTTP retourné par l’API. |
| `Status` | string | Description textuelle du statut. |
| `File` | object | Détails du classeur généré. |
| `File.Name` | string | Nom du fichier du classeur créé. |
| `File.Size` | integer | Taille en octets. |
| `File.Path` | string | Chemin relatif dans le stockage. |
| `File.Url` | string | URL de téléchargement direct (nécessite le même jeton JWT). |

---

**Codes de statut HTTP**

| Code | Signification | Description |
|------|---------------|-------------|
| 200  | OK | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop volumineuse | Le fichier téléversé dépasse la limite de taille. |
| 500  | Erreur interne du serveur | Erreur serveur inattendue. |

---

## Exemples de SDK

Les extraits suivants illustrent comment invoquer **PutWorkbookCreate** à l’aide des SDK officiels Aspose.Cells Cloud.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System.IO;

var apiInstance = new WorkbookApi();
var name = "newworkbook.xlsx"; // string | Nom du nouveau document.
var templateFile = "Calendar.xlsx"; // string | Nom du fichier modèle.
var dataFile = "Sample_Data.xml"; // string | Nom du fichier de données (facultatif).
var isWriteOver = true; // bool? | Écraser si le fichier existe déjà.
var folder = "templates"; // string | Dossier où résident les fichiers.
var storageName = "MyStorage"; // string | Nom du stockage.

using (var dataStream = File.OpenRead("Sample_Data.xml"))
{
    var response = apiInstance.PutWorkbookCreate(
        name,
        templateFile: templateFile,
        dataFile: dataFile,
        isWriteOver: isWriteOver,
        folder: folder,
        storageName: storageName,
        data: dataStream);
    Console.WriteLine(response);
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cloud.cells.api.WorkbookApi;
import com.aspose.cloud.cells.model.*;

import java.io.File;
import java.io.FileInputStream;

WorkbookApi api = new WorkbookApi();
String name = "newworkbook.xlsx";
String templateFile = "Calendar.xlsx";
String dataFile = "Sample_Data.xml";
Boolean isWriteOver = true;
String folder = "templates";
String storageName = "MyStorage";

FileInputStream dataStream = new FileInputStream(new File("Sample_Data.xml"));
CellsCloudResponse response = api.putWorkbookCreate(
        name,
        templateFile,
        dataFile,
        isWriteOver,
        folder,
        storageName,
        dataStream);
System.out.println(response);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once('vendor/autoload.php');

use Aspose\Cells\Cloud\Api\WorkbookApi;
use Aspose\Cells\Cloud\Configuration;

$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new WorkbookApi(null, $config);
$name = "newworkbook.xlsx";
$templateFile = "Calendar.xlsx";
$dataFile = "Sample_Data.xml";
$isWriteOver = true;
$folder = "templates";
$storageName = "MyStorage";

$data = fopen("Sample_Data.xml", "r");
$result = $apiInstance->putWorkbookCreate($name, $templateFile, $dataFile, $isWriteOver, $folder, $storageName, $data);
print_r($result);
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::WorkbookApi.new
api.config.access_token = '{access_token}'

name = 'newworkbook.xlsx'
template_file = 'Calendar.xlsx'
data_file = 'Sample_Data.xml'
is_write_over = true
folder = 'templates'
storage_name = 'MyStorage'

File.open('Sample_Data.xml', 'rb') do |data|
  response = api.put_workbook_create(name,
                                     template_file: template_file,
                                     data_file: data_file,
                                     is_write_over: is_write_over,
                                     folder: folder,
                                     storage_name: storage_name,
                                     data: data)
  puts response
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const { WorkbookApi, Configuration } = require('asposecellscloud');
const fs = require('fs');

let config = new Configuration();
config.accessToken = '{access_token}';
config.basePath = 'https://api.aspose.cloud';

let apiInstance = new WorkbookApi(config);

let name = 'newworkbook.xlsx';
let templateFile = 'Calendar.xlsx';
let dataFile = 'Sample_Data.xml';
let isWriteOver = true;
let folder = 'templates';
let storageName = 'MyStorage';

let data = fs.createReadStream('Sample_Data.xml');

apiInstance.putWorkbookCreate(name, templateFile, dataFile, isWriteOver, folder, storageName, data)
    .then(response => console.log(response))
    .catch(err => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
import asposecellscloud
from asposecellscloud.apis import WorkbookApi
from asposecellscloud.models import CellsCloudResponse

config = asposecellscloud.Configuration()
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

api_instance = WorkbookApi(asposecellscloud.ApiClient(config))

name = 'newworkbook.xlsx'
template_file = 'Calendar.xlsx'
data_file = 'Sample_Data.xml'
is_write_over = True
folder = 'templates'
storage_name = 'MyStorage'

with open('Sample_Data.xml', 'rb') as data:
    response = api_instance.put_workbook_create(
        name,
        template_file=template_file,
        data_file=data_file,
        is_write_over=is_write_over,
        folder=folder,
        storage_name=storage_name,
        data=data)
    print(response)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Api::WorkbookApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '{access_token}';
$config->{host} = 'https://api.aspose.cloud';

my $api_instance = AsposeCellsCloud::Api::WorkbookApi->new($config);

my $name = 'newworkbook.xlsx';
my $template_file = 'Calendar.xlsx';
my $data_file = 'Sample_Data.xml';
my $is_write_over = 1;
my $folder = 'templates';
my $storage_name = 'MyStorage';

open my $fh, '<:raw', 'Sample_Data.xml' or die $!;
my $response = $api_instance->put_workbook_create(
    name => $name,
    template_file => $template_file,
    data_file => $data_file,
    is_write_over => $is_write_over,
    folder => $folder,
    storage_name => $storage_name,
    data => $fh);
print $response;
close $fh;
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "os"

    asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := asposecellscloud.NewConfiguration()
    cfg.AccessToken = "{access_token}"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorkbookApi(cfg)

    name := "newworkbook.xlsx"
    templateFile := "Calendar.xlsx"
    dataFile := "Sample_Data.xml"
    isWriteOver := true
    folder := "templates"
    storageName := "MyStorage"

    data, _ := os.Open("Sample_Data.xml")
    defer data.Close()

    result, _, err := apiInstance.PutWorkbookCreate(name, &templateFile, &dataFile, &isWriteOver, &folder, &storageName, data)
    if err != nil {
        fmt.Println("Error:", err)
    } else {
        fmt.Printf("Response: %+v\n", result)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## Gestion des erreurs

| Code de statut | Situation | Action recommandée |
|----------------|-----------|--------------------|
| **400** | Paramètres obligatoires manquants ou type de fichier non valide. | Vérifiez les paramètres de requête, assurez-vous que les fichiers modèle et de données existent et sont pris en charge (`.xlsx`, `.xml`, `.json`). |
| **401** | Jeton JWT manquant, expiré ou mal formé. | Régénérez un nouveau jeton d’accès à l’aide de votre Client Id/Secret. |
| **413** | Fichier téléversé dépassant la limite de taille du service (50 MB par défaut). | Réduisez la taille du fichier ou divisez le classeur en parties plus petites. |
| **500** | Erreur serveur inattendue. | Réessayez après un court délai ; si le problème persiste, contactez le support Aspose en fournissant la valeur de l’en-tête `Request‑Id`. |

---

## Voir aussi

- **[PutWorkbookSave](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookSave)** – Enregistrer un classeur existant dans un format spécifié.  
- **[GetWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbook)** – Récupérer les informations du classeur ou télécharger le fichier.  
- **[API Upload File](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)** – Téléverser les fichiers modèle ou de données vers le stockage cloud.  

---