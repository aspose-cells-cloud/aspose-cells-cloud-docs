---
title: "Supprimer les doublons"
ArticleTitle: "Supprimer les doublons – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Supprimer les doublons"
type: docs
url: /cells/remove/duplicates
aliases: []
keywords: "Aspose.Cells, Supprimer les doublons, API"
description: "Supprime les valeurs en double dans une feuille de calcul, une plage ou un tableau."
weight: 1000
---

## La fonctionnalité Supprimer les doublons des services web Aspose.Cells Cloud

Supprime les valeurs en double dans la feuille de calcul, la plage ou le tableau. Cette méthode scanne la portée cible à la recherche de lignes dont les valeurs sont identiques dans les colonnes spécifiées à vérifier. Pour chaque ensemble de doublons, toutes les occurrences sauf la première sont supprimées. La comparaison est généralement sensible à la casse et correspond à la valeur exacte de la cellule.

### Point de terminaison de l'API web

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/duplicates
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement (chemin/chaîne de requête/ Corps HTTP) | Description |
|------------------|--------|-----------------------------------------------------|-------------|
| Spreadsheet      | Fichier | FormData                                            | Télécharger le fichier de classeur. |
| worksheet        | Chaîne  | Chaîne de requête                                   | Nom de la feuille de calcul. (facultatif) |
| range            | Chaîne  | Chaîne de requête                                   | Nom de la plage à nettoyer des doublons. (facultatif) |
| table            | Chaîne  | Chaîne de requête                                   | Nom du tableau à nettoyer des doublons. (facultatif) |
| outPath          | Chaîne  | Chaîne de requête                                   | (Facultatif) Chemin du dossier où le classeur est stocké. La valeur par défaut est null. |
| outStorageName   | Chaîne  | Chaîne de requête                                   | Nom du stockage pour le fichier de sortie. |
| region           | Chaîne  | Chaîne de requête                                   | Paramètre de région/langue du classeur (par ex. `en-US`, `fr-FR`). Affecte le formatage des nombres, l'analyse des dates et le comportement propre à la localisation. |
| password         | Chaîne  | Chaîne de requête                                   | Mot de passe pour ouvrir le fichier de classeur. |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| [TBD]            | [TBD] | [TBD]       |

### **Réponse**

```json
{
  "File": "flux binaire du classeur résultant (par ex., .xlsx)"
}
```

**Codes d'état de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200  | OK            | Le classeur résultant, avec les doublons supprimés, est renvoyé sous forme de flux de fichiers. |
| 400  | Requête incorrecte | Paramètres de requête invalides ou URL mal formée. |
| 401  | Non autorisé  | L'authentification a échoué ou aucune authentification n'a été fournie. |
| 413  | Payload trop volumineux | Le fichier téléchargé dépasse la taille limite autorisée. |
| 500  | Erreur interne du serveur | Une anomalie s'est produite lors de l'extraction des données dans le classeur ou une autre erreur côté serveur. |

## Comment utiliser la fonction Supprimer les doublons avec les SDK

### Spécification de la fonction Supprimer les doublons

La [spécification de l'API Supprimer les doublons](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{RemoveDuplicates}) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}
{< tab tabNum="1" >}
```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/remove/duplicates?worksheet=Sheet1&range=A1:C10&table=MyTable&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F 'Spreadsheet=@exemple.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "File": "flux binaire du classeur résultant (par ex., .xlsx)"
}
```
{< /tab >}
{< /tabs >}

### Utiliser les SDK Aspose Cells Cloud

L'utilisation d'un SDK est le moyen le plus rapide d'accélérer le développement. Un SDK abstractise les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose Cells Cloud à l'aide de divers SDK :
```csharp
// Exemple de code SDK pour C#
var config = new Configuration
{
    AccessToken = "<jeton jwt>"
};
var apiInstance = new TransformApi(config);
var file = File.ReadAllBytes("exemple.xlsx");
var result = apiInstance.RemoveDuplicates(
    file,
    worksheet: "Sheet1",
    range: "A1:C10",
    table: "MyTable",
    outPath: "output/folder",
    outStorageName: "MyStorage",
    region: "en-US",
    password: "MyPassword"
);
File.WriteAllBytes("resultat.xlsx", result);
```

```java
// Exemple de code SDK pour Java
ApiClient client = new ApiClient();
client.setAccessToken("<jeton jwt>");
TransformApi api = new TransformApi(client);
byte[] file = Files.readAllBytes(Paths.get("exemple.xlsx"));
byte[] result = api.removeDuplicates(
    file,
    "Sheet1",
    "A1:C10",
    "MyTable",
    "output/folder",
    "MyStorage",
    "en-US",
    "MyPassword"
);
Files.write(Paths.get("resultat.xlsx"), result);
```

```python
# Exemple de code SDK pour Python
import asposecellscloud
from asposecellscloud.rest import ApiException

configuration = asposecellscloud.Configuration()
configuration.access_token = "<jeton jwt>"
api_instance = asposecellscloud.TransformApi(asposecellscloud.ApiClient(configuration))

with open('exemple.xlsx', 'rb') as f:
    file_bytes = f.read()

try:
    result = api_instance.remove_duplicates(
        file=file_bytes,
        worksheet='Sheet1',
        range='A1:C10',
        table='MyTable',
        out_path='output/folder',
        out_storage_name='MyStorage',
        region='en-US',
        password='MyPassword'
    )
    with open('resultat.xlsx', 'wb') as out_f:
        out_f.write(result)
except ApiException as e:
    print("Exception lors de l'appel à TransformApi->remove_duplicates : %s\n" % e)
```

`[TBD]`
---