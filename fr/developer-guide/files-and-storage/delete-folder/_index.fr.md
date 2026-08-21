---
---
title: "Supprimer un dossier – API Aspose.Cells Cloud | Supprimer des dossiers via REST"
description: "Découvrez comment supprimer un dossier (éventuellement de manière récursive) du stockage Aspose.Cells Cloud à l’aide du point de terminaison DELETE /v4.0/cells/storage/folder/{path}. Inclut la syntaxe de requête, les paramètres, l’authentification, des exemples de code et la gestion des erreurs."
keywords: "Aspose.Cells, suppression de dossier, stockage cloud, API, REST, Excel, gestion de fichiers"
slug: delete-folder
date: 2026-07-30
---

# Supprimer un dossier – API Aspose.Cells Cloud

Supprimez un dossier (et éventuellement tout son contenu) du stockage Aspose.Cells Cloud.

---

## Vue d’ensemble

L’opération **Supprimer un dossier** supprime définitivement un dossier du compte de stockage utilisé par Aspose.Cells Cloud.  
Vous pouvez supprimer un dossier vide ou, en définissant le drapeau `recursive` sur `true`, supprimer le dossier avec tous ses fichiers et sous-dossiers. Ce point de terminaison est couramment utilisé dans les scripts de nettoyage, les workflows automatisés ou lorsqu’un répertoire temporaire n’est plus nécessaire.

---

## Requête HTTP

```
DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

*`{path}`* – le chemin complet du dossier à supprimer (encodé en URL).

### En-têtes HTTP requis

| En-tête           | Valeur                             | Description                              |
|-------------------|------------------------------------|------------------------------------------|
| `Authorization`   | `Bearer {access_token}`            | Jeton JWT obtenu auprès du service d’authentification. |
| `Accept`          | `application/json`                | Format de réponse attendu.               |
| `Content-Type`    | `application/json` *(facultatif)* | Non requis pour DELETE, mais peut être envoyé. |

---

## Authentification

Aspose.Cells Cloud utilise **l’authentification basée sur des jetons JWT**.  
Obtenez un jeton d’accès via le [point de terminaison d’authentification](/authentication/) et incluez-le dans l’en-tête `Authorization`, comme indiqué ci-dessus.

```bash
-H "Authorization: Bearer {access_token}"
```

---

## Paramètres

| Nom           | Type    | Emplacement | Obligatoire | Description                                                               |
|---------------|---------|-------------|-------------|---------------------------------------------------------------------------|
| `path`        | string  | Chemin      | Oui         | Chemin du dossier à supprimer (encodé en URL).                             |
| `storageName` | string  | Requête     | Non         | Nom du stockage contenant le dossier. Si omis, le stockage par défaut est utilisé. |
| `recursive`   | boolean | Requête     | Non         | `true` → supprime le dossier **et tout son contenu**. Par défaut : `false`. |

**Exemple de chaîne de requête**

```
?storageName=MyStorage&recursive=true
```

---

## Exemple de requête (cURL)

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/folder/MyFolder?storageName=MyStorage&recursive=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## Réponse

Une requête réussie renvoie **HTTP 200 OK** avec un objet JSON vide :

```json
{}
```

Aucune charge utile supplémentaire n’est fournie, car le résultat de l’opération est binaire : le dossier est supprimé ou une erreur est renvoyée.

---

**Codes de statut HTTP**

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop grande    | Fichier téléchargé dépassant la taille limite. |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue. |

En cas d’erreur, le corps contient un objet JSON avec les champs `code` et `message`, décrivant le problème.

---

## Exemples de code SDK

Les exemples suivants illustrent comment appeler **Supprimer un dossier** à l’aide des SDK officiellement pris en charge. Remplacez `{access_token}` et les valeurs des paramètres par vos propres valeurs.

<details><summary>🟦 C# (.NET)</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Configuration du client API
var config = new Configuration
{
    AccessToken = "{access_token}",
    BasePath = "https://api.aspose.cloud"
};

var folderApi = new FolderApi(config);

// Suppression du dossier (récursive)
var request = new DeleteFolderRequest
{
    Path = "MyFolder",
    StorageName = "MyStorage",
    Recursive = true
};

folderApi.DeleteFolder(request);
```
</details>

<details><summary>🟨 Java</summary>

```java
import com.aspose.cloud.cells.api.FolderApi;
import com.aspose.cloud.cells.model.*;
import com.aspose.cloud.cells.model.requests.DeleteFolderRequest;

// Initialisation du client API
FolderApi folderApi = new FolderApi("{access_token}");

DeleteFolderRequest request = new DeleteFolderRequest()
        .path("MyFolder")
        .storageName("MyStorage")
        .recursive(true);

folderApi.deleteFolder(request);
```
</details>

<details><summary>🟪 PHP</summary>

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\FolderApi;
use Aspose\Cells\Cloud\Configuration;

// Configuration
$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new FolderApi($config);

// Suppression récursive du dossier
try {
    $apiInstance->deleteFolder('MyFolder', 'MyStorage', true);
    echo "Dossier supprimé.";
} catch (Exception $e) {
    echo 'Exception lors de l’appel à FolderApi->deleteFolder : ', $e->getMessage(), PHP_EOL;
}
?>
```
</details>

<details><summary>🟧 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::FolderApi.new

begin
  api.delete_folder('MyFolder', storage_name: 'MyStorage', recursive: true)
  puts 'Dossier supprimé.'
rescue AsposeCellsCloud::ApiError => e
  puts "Erreur : #{e.message}"
end
```
</details>

<details><summary>🟢 Node.js (TypeScript)</summary>

```ts
import { FolderApi, DeleteFolderRequest } from '@asposecloud/cells-sdk';

const config = {
    accessToken: '{access_token}',
    basePath: 'https://api.aspose.cloud'
};

const folderApi = new FolderApi(config);

const request: DeleteFolderRequest = {
    path: 'MyFolder',
    storageName: 'MyStorage',
    recursive: true
};

folderApi.deleteFolder(request)
    .then(() => console.log('Dossier supprimé'))
    .catch(err => console.error('Erreur :', err));
```
</details>

<details><summary>🐍 Python</summary>

```python
from asposecellscloud import FolderApi, DeleteFolderRequest, Configuration

config = Configuration()
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

folder_api = FolderApi(config)

request = DeleteFolderRequest(
    path='MyFolder',
    storage_name='MyStorage',
    recursive=True
)

folder_api.delete_folder(request)
print("Dossier supprimé")
```
</details>

<details><summary>🦪 Perl</summary>

```perl
use AsposeCellsCloud::FolderApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '{access_token}',
    host => 'https://api.aspose.cloud'
);

my $api = AsposeCellsCloud::FolderApi->new($config);

eval {
    $api->delete_folder(
        path => 'MyFolder',
        storage_name => 'MyStorage',
        recursive => 1
    );
    print "Dossier supprimé.\n";
};
if ($@) {
    warn "Erreur lors de la suppression du dossier : $@";
}
```
</details>

<details><summary>🦑 Go</summary>

```go
package main

import (
    "context"
    "fmt"
    cells "github.com/asposecellscloud/aspose-cells-cloud-go/v4"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AccessToken = "{access_token}"
    cfg.Host = "https://api.aspose.cloud"

    api := cells.NewFolderApi(cfg)

    req := cells.DeleteFolderRequest{
        Path:        "MyFolder",
        StorageName: "MyStorage",
        Recursive:   true,
    }

    _, err := api.DeleteFolder(context.Background(), req)
    if err != nil {
        fmt.Printf("Erreur : %v\n", err)
        return
    }
    fmt.Println("Dossier supprimé")
}
```
</details>

---

## Voir aussi

- **[Créer un dossier](/create-folder/)** – Créez un nouveau dossier dans le stockage cloud.  
- **[Copier un dossier](/copy-folder/)** – Dupliquez un dossier et son contenu.  
- **[Déplacer un dossier](/move-folder/)** – Déplacez un dossier vers un autre chemin.  
- **[Spécification OpenAPI]** – <a href="https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder" rel="noopener noreferrer">Opération DeleteFolder</a> (explorateur d’API interactif).

---

## Liste de vérification SEO et accessibilité (interne)

- **Titre et H1** utilisent le trait d’union correct (–) et contiennent le mot-clé principal *Supprimer un dossier*.  
- Tous les titres suivent une hiérarchie logique (`H1 → H2 → H3`).  
- Aucun artefact d’encodage UTF-8 n’est présent.  
- Les mots-clés méta sont regroupés dans une liste unique et propre (ou omis si préféré).  
- Les liens externes incluent `rel="noopener noreferrer"` pour des raisons de sécurité.  
- Les icônes d’interface utilisateur et les drapeaux linguistiques (si rendus sur la page) devraient comporter les attributs `aria-label` / `alt` (par exemple, `aria-label="Français (France)"`).  
- Les balises `<link rel="alternate" hreflang="xx" href="…">` sont recommandées dans l’en-tête de la page pour chaque version linguistique.  

---