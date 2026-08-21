---
title: "Ajouter un commentaire de feuille de calcul"
description: "Ajouter un commentaire à une cellule spécifique dans une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud (PUT /v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName})."
keywords: "Aspose.Cells, API Cloud, Ajouter un commentaire de feuille de calcul, Excel, Classeur, Commentaire de cellule"
weight: 20
api_version: "v3.0"
---

# Ajouter un commentaire de feuille de calcul

Ajouter un commentaire à une cellule spécifique dans une feuille de calcul d’un classeur Excel à l’aide de l’API REST Aspose.Cells Cloud.

---

## Conditions préalables / Authentification

* Un **jeton Bearer JWT** est requis pour chaque requête.  
  *Obtenir un jeton* via le point de terminaison **/connect/token** (voir le [guide d’authentification](/cells/authentication/)).  
* Inclure le jeton dans l’en-tête `Authorization` :

```http
Authorization: Bearer <jeton jwt>
```

* Toutes les appels doivent être effectués via **HTTPS** afin de protéger le jeton et les données.

---

## Requête HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### Paramètres de chemin

| Nom       | Type   | Requis | Description |
|-----------|--------|--------|-------------|
| `name`    | string | ✔️ | Nom du fichier du classeur (par exemple, `test.xlsx`). |
| `sheetName` | string | ✔️ | Nom de la feuille de calcul (par exemple, `Sheet1`). |
| `cellName` | string | ✔️ | Adresse de la cellule cible (par exemple, `A1`). |

### Paramètres de requête

| Nom              | Type   | Requis | Description |
|------------------|--------|--------|-------------|
| `folder`         | string | facultatif | Dossier contenant le classeur. |
| `storageName`    | string | facultatif | Nom du service de stockage où le fichier est situé. |

### Corps de la requête

Le corps doit contenir un objet **Comment** au format JSON.

```json
{
  "CellName": "A1",
  "Author": "string",
  "HtmlNote": "string",
  "Note": "string",
  "AutoSize": true,
  "IsVisible": true,
  "Width": 10,
  "Height": 10,
  "TextHorizontalAlignment": "Left",
  "TextOrientationType": "NoRotation",
  "TextVerticalAlignment": "Top"
}
```

**Champs de l’objet Comment**

| Champ                            | Type    | Requis | Description |
|----------------------------------|---------|--------|-------------|
| `CellName`                       | string  | ✔️ | Adresse de la cellule (doit correspondre à la valeur `{cellName}` du chemin). |
| `Author`                         | string  | facultatif | Nom de l’auteur du commentaire. |
| `HtmlNote`                       | string  | facultatif | Texte du commentaire au format HTML. |
| `Note`                           | string  | facultatif | Texte brut du commentaire. |
| `AutoSize`                       | boolean | facultatif | Redimensionner automatiquement la boîte de commentaire. |
| `IsVisible`                      | boolean | facultatif | Afficher le commentaire par défaut. |
| `Width` / `Height`               | number  | facultatif | Dimensions de la boîte de commentaire (en points). |
| `TextHorizontalAlignment`       | string  | facultatif | Alignement horizontal (`Left`, `Center`, `Right`). |
| `TextOrientationType`           | string  | facultatif | Orientation du texte (`NoRotation`, `Rotate90`, etc.). |
| `TextVerticalAlignment`         | string  | facultatif | Alignement vertical (`Top`, `Center`, `Bottom`). |

---

## Exemple cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>" \
  -d '{
        "CellName": "A1",
        "Author": "test",
        "HtmlNote": "<font style=\"font-weight:bold;font-family:Tahoma;font-size:9pt;color:#000000;text-align:left;\">this is a comment</font>",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10,
        "TextHorizontalAlignment": "Left",
        "TextOrientationType": "NoRotation",
        "TextVerticalAlignment": "Top"
      }'
```

---

## Schéma de réponse

| Champ     | Type   | Description |
|-----------|--------|-------------|
| `Comment` | object | Objet commentaire créé (voir **Champs de l’objet Comment** ci-dessus, ainsi que les métadonnées de lien). |
| `Code`    | integer | Code de statut HTTP retourné par l’API (par exemple, `200`). |
| `Status`  | string  | Message de statut textuel (par exemple, `"OK"`). |

L’objet `Comment` contient également un sous-objet **link** :

| Sous-champ | Type   | Description |
|------------|--------|-------------|
| `Href`     | string | URL de référence vers la ressource du commentaire. |
| `Rel`      | string | Type de relation (`self`). |
| `Title`    | string | Titre facultatif (peut être `null`). |
| `Type`     | string | Type MIME facultatif (peut être `null`). |

---

## Exemple de réponse réussie

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "test",
    "HtmlNote": "<Font Style=\"FONT-WEIGHT: bold;FONT-FAMILY: Tahoma;FONT-SIZE: 9pt;COLOR: #000000;TEXT-ALIGN: left;\">this is a comment</Font>",
    "Note": "this is a comment",
    "AutoSize": true,
    "IsVisible": true,
    "Width": 10,
    "Height": 10,
    "TextHorizontalAlignment": "Left",
    "TextOrientationType": "NoRotation",
    "TextVerticalAlignment": "Top",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/comments/A1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## Réponses d’erreur

| Code HTTP | Description | Exemple |
|-----------|-------------|---------|
| **400**   | Requête incorrecte – paramètres manquants ou invalides. | `{ "Error": { "Code": "InvalidParameter", "Message": "Le paramètre 'cellName' est manquant ou mal formé." }, "Code": 400, "Status": "Bad Request" }` |
| **401**   | Non autorisé – jeton manquant ou invalide. | `{ "Error": { "Code": "InvalidToken", "Message": "L’authentification a échoué." }, "Code": 401, "Status": "Unauthorized" }` |
| **404**   | Introuvable – le classeur, la feuille de calcul ou la cellule n’existe pas. | `{ "Error": { "Code": "FileNotFound", "Message": "Le classeur 'test.xlsx' est introuvable." }, "Code": 404, "Status": "Not Found" }` |
| **500**   | Erreur interne du serveur – condition inattendue sur le serveur. | `{ "Error": { "Code": "ServerError", "Message": "Une erreur inattendue s’est produite." }, "Code": 500, "Status": "Internal Server Error" }` |

---

## Exemples de SDK

Les SDK suivants fournissent des wrappers prêts à l’emploi pour cette opération. Remplacer les valeurs génériques (`<YOUR_TOKEN>`, `<FILE_NAME>`, etc.) par des données réelles.

{{< tabs tabTotal="8" tabID="sdk" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Configurer le client API
var config = new Configuration
{
    ClientId = "<votre_client_id>",
    ClientSecret = "<votre_client_secret>"
};
var apiInstance = new WorksheetsApi(config);

// Préparer l’objet commentaire
var comment = new Comment
{
    CellName = "A1",
    Author = "test",
    Note = "this is a comment",
    HtmlNote = "<font style=\"font-weight:bold;\">this is a comment</font>",
    AutoSize = true,
    IsVisible = true,
    Width = 10,
    Height = 10
};

try
{
    var response = apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, folder: null, storageName: null);
    Console.WriteLine(response);
}
catch (Exception e)
{
    Console.WriteLine("Exception lors de l’appel à WorksheetsApi.PutWorksheetComment : " + e.Message );
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.*;
import com.aspose.cells.cloud.model.*;

ApiClient client = new ApiClient();
client.setAppSid("<votre_client_id>");
client.setAppKey("<votre_client_secret>");

WorksheetsApi worksheetsApi = new WorksheetsApi(client);

Comment comment = new Comment()
        .cellName("A1")
        .author("test")
        .note("this is a comment")
        .htmlNote("<font style=\"font-weight:bold;\">this is a comment</font>")
        .autoSize(true)
        .isVisible(true)
        .width(10)
        .height(10);

try {
    CommentResponse resp = worksheetsApi.putWorksheetComment("test.xlsx", "Sheet1", "A1", comment, null, null);
    System.out.println(resp);
} catch (ApiException e) {
    e.printStackTrace();
}
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<votre_client_id>');
$config->setAppKey('<votre_client_secret>');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

$comment = new Aspose\Cells\Model\Comment([
    'CellName' => 'A1',
    'Author'   => 'test',
    'Note'     => 'this is a comment',
    'HtmlNote' => '<font style="font-weight:bold;">this is a comment</font>',
    'AutoSize' => true,
    'IsVisible'=> true,
    'Width'    => 10,
    'Height'   => 10
]);

try {
    $result = $apiInstance->putWorksheetComment('test.xlsx', 'Sheet1', 'A1', $comment);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception lors de l’appel à WorksheetsApi->putWorksheetComment : ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.client_id = '<votre_client_id>'
config.client_secret = '<votre_client_secret>'

api_instance = AsposeCellsCloud::WorksheetsApi.new

comment = AsposeCellsCloud::Comment.new(
  cell_name: 'A1',
  author: 'test',
  note: 'this is a comment',
  html_note: '<font style="font-weight:bold;">this is a comment</font>',
  auto_size: true,
  is_visible: true,
  width: 10,
  height: 10
)

begin
  result = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
  puts result
rescue AsposeCellsCloud::ApiError => e
  puts "Exception lors de l’appel à WorksheetsApi->put_worksheet_comment : #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const { WorksheetsApi, Configuration, Comment } = require('asposecellscloud');

let config = new Configuration();
config.clientId = '<votre_client_id>';
config.clientSecret = '<votre_client_secret>';

let api = new WorksheetsApi(config);

let comment = new Comment({
  CellName: 'A1',
  Author: 'test',
  Note: 'this is a comment',
  HtmlNote: '<font style="font-weight:bold;">this is a comment</font>',
  AutoSize: true,
  IsVisible: true,
  Width: 10,
  Height: 10
});

api.putWorksheetComment('test.xlsx', 'Sheet1', 'A1', comment)
  .then(response => console.log(response))
  .catch(err => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.models import Comment

config = asposecellscloud.Configuration()
config.client_id = '<votre_client_id>'
config.client_secret = '<votre_client_secret>'

api_instance = asposecellscloud.WorksheetsApi(asposecellscloud.ApiClient(config))

comment = Comment(
    CellName='A1',
    Author='test',
    Note='this is a comment',
    HtmlNote='<font style="font-weight:bold;">this is a comment</font>',
    AutoSize=True,
    IsVisible=True,
    Width=10,
    Height=10
)

try:
    api_response = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
    print(api_response)
except ApiException as e:
    print("Exception lors de l’appel à WorksheetsApi->put_worksheet_comment : %s\\n" % e)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Object::Comment;

my $config = AsposeCellsCloud::Configuration->new(
    client_id     => '<votre_client_id>',
    client_secret => '<votre_client_secret>'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $comment = AsposeCellsCloud::Object::Comment->new(
    CellName => 'A1',
    Author   => 'test',
    Note     => 'this is a comment',
    HtmlNote => '<font style="font-weight:bold;">this is a comment</font>',
    AutoSize => 1,
    IsVisible=> 1,
    Width    => 10,
    Height   => 10
);

eval {
    my $result = $api_instance->put_worksheet_comment(
        name      => 'test.xlsx',
        sheet_name=> 'Sheet1',
        cell_name => 'A1',
        comment   => $comment
    );
    print $result;
};
if ($@) {
    warn "Exception lors de l’appel à WorksheetsApi->put_worksheet_comment : $@";
}
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/model"
)

func main() {
    cfg := cellscloud.NewConfiguration()
    cfg.ClientId = "<votre_client_id>"
    cfg.ClientSecret = "<votre_client_secret>"

    apiInstance := api.NewWorksheetsApi(cfg)

    comment := model.Comment{
        CellName: "A1",
        Author:   "test",
        Note:     "this is a comment",
        HtmlNote: "<font style=\"font-weight:bold;\">this is a comment</font>",
        AutoSize: true,
        IsVisible: true,
        Width: 10,
        Height: 10,
    }

    resp, _, err := apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, nil, nil)
    if err != nil {
        fmt.Printf("Erreur : %v\\n", err)
    } else {
        fmt.Printf("Réponse : %+v\\n", resp)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## Voir aussi

* **Obtenir un commentaire de feuille de calcul** – `GET /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Mettre à jour un commentaire de feuille de calcul** – `POST /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Supprimer un commentaire de feuille de calcul** – `DELETE /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Effacer tous les commentaires** – `DELETE /cells/{name}/worksheets/{sheetName}/comments`  

---

## Notes supplémentaires

* Le chemin du point de terminaison inclut **v3.0**. Une version plus récente (**v3.1**) est disponible ; mettez à jour l’URL de base en conséquence si vous avez besoin des dernières fonctionnalités.  
* Pour la définition complète OpenAPI, visitez la [documentation de référence de l’API Aspose.Cells Cloud](/cells/#/Worksheets/PutWorksheetComment).  
* Pensez à gérer le *rate limiting* (HTTP 429) et à réessayer conformément aux directives de l’API.  

---
---