---
title: "Convertir un objet OLE en image – Aspose.Cells Cloud REST API"
description: "Récupérer un objet OLE intégré à partir d'une feuille de calcul Excel et le convertir au format PNG, JPEG, TIFF, GIF, EMF ou BMP à l'aide de l'API REST Aspose.Cells Cloud."
keywords:
  - "conversion d'objet OLE en image"
  - "Aspose.Cells Cloud"
  - "API REST"
  - "Excel"
  - "OLE"
  - "conversion d'image"
  - "PNG"
  - "JPEG"
  - "TIFF"
  - "GIF"
  - "EMF"
  - "BMP"
weight: 40
---

# Convertir un objet OLE en image

Récupérer un objet OLE intégré à partir d'une feuille de calcul et le renvoyer au format d'image demandé.

---

## Conditions préalables

Avant d’appeler cette endpoint, assurez-vous d’avoir :

1. **Un compte Aspose.Cells Cloud** – inscrivez-vous sur le [portail Aspose Cloud](https://dashboard.aspose.cloud/).
2. **Classeur téléversé dans le stockage cloud** – utilisez l’API **Upload File** ou l’interface utilisateur d’Aspose Cloud.
3. **Jeton d’accès JWT** – obtenez un jeton en suivant le [guide d’authentification](/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## Sécurité et authentification

Toutes les API Aspose.Cells Cloud exigent une **authentification basée sur un jeton JWT**. Incluez le jeton dans l’en-tête `Authorization` :

```http
Authorization: Bearer <jeton-jwt>
```

Seuls les endpoints HTTPS sont pris en charge ; n’utilisez jamais `http://`.

---

## Requête

### Méthode HTTP
`GET`

### Endpoint
```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### Paramètres de chemin

| Nom               | Type   | Obligatoire | Description                                |
|-------------------|--------|-------------|--------------------------------------------|
| `name`            | string | ✅          | Nom du fichier classeur (par exemple, `Book1.xlsx`). |
| `sheetName`       | string | ✅          | Feuille de calcul contenant l’objet OLE.   |
| `objectNumber`    | integer| ✅          | Index de base zéro de l’objet OLE.         |

### Paramètres de requête

| Nom           | Type   | Obligatoire | Description |
|---------------|--------|-------------|-------------|
| `format`      | string | ❌          | Format d’image souhaité (`png`, `jpeg`, `tiff`, `gif`, `emf`, `bmp`). Si omis, la valeur par défaut est `png`. |
| `folder`      | string | ❌          | Chemin vers le dossier contenant le classeur. |
| `storageName` | string | ❌          | Nom du service de stockage (par exemple, `MyCloud`). |

---

## Exemple de requête (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton-jwt>"
```

*Remplacez `<jeton-jwt>` par un jeton JWT valide.*

---

## Réponse

| Statut | Type de contenu         | Description |
|--------|-------------------------|-------------|
| `200`  | `image/png` (ou le format demandé) | Données binaires d’image représentant l’objet OLE. |
| `400`  | `application/json`      | Paramètres de requête non valides. |
| `401`  | `application/json`      | Échec de l’authentification (JWT manquant ou non valide). |
| `404`  | `application/json`      | Classeur, feuille de calcul ou objet OLE spécifié introuvable. |
| `500`  | `application/json`      | Erreur côté serveur. |

### Traitement de la charge utile binaire

L’API renvoie les octets bruts de l’image. Vous pouvez :

* **Enregistrer directement dans un fichier** (exemple Linux/macOS) :

  ```bash
  curl -o oleobject.png "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jeton-jwt>"
  ```

* **Encoder en Base64** pour débogage ou intégration dans JSON :

  ```bash
  curl -s "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jeton-jwt>" | base64
  ```

  *Exemple (partiel) de sortie Base64 :*

  ```
  iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkY…
  ```

---

## Réponses d’erreur

| Statut HTTP | Code                   | Message |
|-------------|------------------------|---------|
| `400`       | `InvalidParameter`     | Un ou plusieurs paramètres de la requête ne sont pas valides. |
| `401`       | `AuthenticationFailed` | Jeton JWT manquant ou non valide. |
| `404`       | `PropertyNotFound`     | Le classeur, la feuille de calcul ou l’objet OLE demandé n’existe pas. |
| `500`       | `InternalError`        | Une erreur inattendue s’est produite sur le serveur. |

---

## Exemples avec SDK

Les extraits suivants illustrent comment appeler cette opération à l’aide des SDK officiels. Remplacez `YOUR_JWT_TOKEN` et autres espaces réservés par vos valeurs réelles.

| Langage | Exemple |
|---------|---------|
| **C#** | <details><summary>Afficher le code</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model.Requests;\n\nvar config = new Configuration { AccessToken = "YOUR_JWT_TOKEN" };\nvar api = new OleObjectsApi(config);\nvar request = new GetWorksheetOleObjectRequest(\n    name: "Embedded_OleObject_Sample_Book1.xlsx",\n    sheetName: "Sheet1",\n    objectNumber: 0,\n    format: "png"\n);\nvar stream = api.GetWorksheetOleObject(request);\nusing var file = File.Create("oleobject.png");\nstream.CopyTo(file);\n```</details> |
| **Java** | <details><summary>Afficher le code</summary>```java\nimport com.aspose.cells.cloud.ApiException;\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.model.*;\nimport com.aspose.cells.cloud.model.requests.*;\nimport java.io.FileOutputStream;\nimport java.io.InputStream;\n\nOleObjectsApi api = new OleObjectsApi();\napi.getApiClient().setAccessToken("YOUR_JWT_TOKEN");\nGetWorksheetOleObjectRequest req = new GetWorksheetOleObjectRequest(\n    "Embedded_OleObject_Sample_Book1.xlsx",\n    "Sheet1",\n    0,\n    "png",\n    null,\n    null\n);\nInputStream stream = api.getWorksheetOleObject(req);\ntry (FileOutputStream out = new FileOutputStream("oleobject.png")) {\n    stream.transferTo(out);\n}\n```</details> |
| **Python** | <details><summary>Afficher le code</summary>```python\nfrom asposecellscloud import CellsApi, GetWorksheetOleObjectRequest\n\napi = CellsApi()\napi.api_client.configuration.access_token = "YOUR_JWT_TOKEN"\nrequest = GetWorksheetOleObjectRequest(\n    name="Embedded_OleObject_Sample_Book1.xlsx",\n    sheet_name="Sheet1",\n    object_number=0,\n    format="png"\n)\nstream = api.get_worksheet_ole_object(request)\nwith open('oleobject.png', 'wb') as f:\n    f.write(stream.read())\n```</details> |
| **Node.js** | <details><summary>Afficher le code</summary>```javascript\nconst { CellsApi, GetWorksheetOleObjectRequest } = require('asposecellscloud');\n\nconst api = new CellsApi();\napi.apiClient.configuration.accessToken = 'YOUR_JWT_TOKEN';\n\nconst request = new GetWorksheetOleObjectRequest({\n    name: 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheetName: 'Sheet1',\n    objectNumber: 0,\n    format: 'png'\n});\napi.getWorksheetOleObject(request).then(stream => {\n    const fs = require('fs');\n    const writeStream = fs.createWriteStream('oleobject.png');\n    stream.pipe(writeStream);\n});\n```</details> |
| **Go** | <details><summary>Afficher le code</summary>```go\npackage main\nimport (\n    "io"\n    "os"\n    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\nfunc main() {\n    cfg := cells.NewConfiguration()\n    cfg.AccessToken = "YOUR_JWT_TOKEN"\n    api := cells.NewOleObjectsApi(cfg)\n    req := cells.GetWorksheetOleObjectRequest{\n        Name:         "Embedded_OleObject_Sample_Book1.xlsx",\n        SheetName:    "Sheet1",\n        ObjectNumber: 0,\n        Format:       "png",\n    }\n    stream, _, err := api.GetWorksheetOleObject(req)\n    if err != nil { panic(err) }\n    out, _ := os.Create("oleobject.png")\n    defer out.Close()\n    io.Copy(out, stream)\n}\n```</details> |
| **PHP** | <details><summary>Afficher le code</summary>```php\n<?php\nrequire_once 'vendor/autoload.php';\nuse Aspose\\Cells\\Cloud\\Api\\OleObjectsApi;\nuse Aspose\\Cells\\Cloud\\Model\\Requests\\GetWorksheetOleObjectRequest;\n\n$config = new \\Aspose\\Cells\\Cloud\\Configuration();\n$config->setAccessToken('YOUR_JWT_TOKEN');\n$apiInstance = new OleObjectsApi($config);\n$request = new GetWorksheetOleObjectRequest(\n    'Embedded_OleObject_Sample_Book1.xlsx',\n    'Sheet1',\n    0,\n    'png'\n);\n$stream = $apiInstance->getWorksheetOleObject($request);\nfile_put_contents('oleobject.png', $stream);\n?>\n```</details> |
| **Ruby** | <details><summary>Afficher le code</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::OleObjectsApi.new\napi.api_client.config.access_token = 'YOUR_JWT_TOKEN'\nrequest = AsposeCellsCloud::GetWorksheetOleObjectRequest.new(\n  name: 'Embedded_OleObject_Sample_Book1.xlsx',\n  sheet_name: 'Sheet1',\n  object_number: 0,\n  format: 'png'\n)\nstream = api.get_worksheet_ole_object(request)\nFile.open('oleobject.png', 'wb') { |f| f.write(stream) }\n```\n</details> |
| **Perl** | <details><summary>Afficher le code</summary>```perl\nuse AsposeCellsCloud::Api::OleObjectsApi;\nuse AsposeCellsCloud::Object::GetWorksheetOleObjectRequest;\n\nmy $api = AsposeCellsCloud::Api::OleObjectsApi->new();\n$api->{api_client}->{config}->{access_token} = 'YOUR_JWT_TOKEN';\nmy $req = AsposeCellsCloud::Object::GetWorksheetOleObjectRequest->new(\n    name => 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheet_name => 'Sheet1',\n    object_number => 0,\n    format => 'png'\n);\nmy $stream = $api->get_worksheet_ole_object(request => $req);\nopen my $fh, '>', 'oleobject.png' or die $!;\nbinmode $fh;\nprint $fh $stream;\nclose $fh;\n```</details> |

*(La liste complète des SDK est disponible dans le [dépôt GitHub](https://github.com/aspose-cells-cloud).)*

---

## Opérations associées

- **Ajouter un objet OLE** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`
- **Mettre à jour un objet OLE** – `PUT /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **Supprimer un objet OLE** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **Obtenir la liste des objets OLE** – `GET /cells/{name}/worksheets/{sheetName}/oleobjects`

Pour plus de détails, consultez les pages de référence correspondantes de l’API.

---

## Ressources supplémentaires

- **Spécification OpenAPI** – <https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject>
- **Guide d’authentification** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **Dépôts SDK** – <https://github.com/aspose-cells-cloud>
- **Performance et accessibilité** – Exécutez des audits Lighthouse et axe‑core pour garantir des temps de chargement optimaux et la conformité WCAG 2.1 AA.