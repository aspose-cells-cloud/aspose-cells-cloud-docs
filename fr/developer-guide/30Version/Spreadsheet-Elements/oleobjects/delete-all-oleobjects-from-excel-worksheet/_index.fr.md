---
title: Supprimer tous les objets OLE dans une feuille de calcul Excel
description: Découvrez comment supprimer tous les objets OLE (Object Linking and Embedding) d'une feuille de calcul Excel à l'aide de l'API REST Aspose.Cells Cloud (v3.0). Inclut l'endpoint, les paramètres, des exemples de requête/réponse, des extraits de code SDK, l'authentification, la gestion des erreurs et les FAQ.
keywords: Aspose.Cells Cloud, suppression d'objets OLE, API Excel, API REST, vidage OLE dans la feuille de calcul, SDK cloud
api_version: v3.0
last_updated: 2024-11-01
weight: 60
---

# Supprimer tous les objets OLE dans une feuille de calcul Excel

**OleObjects – Clear** supprime **tous** les objets OLE (*Object Linking and Embedding*, ou liaison et intégration d'objets) d'une feuille de calcul spécifiée, tout en laissant les données des cellules intactes. Cette opération est utile pour nettoyer des classeurs hérités ou préparer un classeur à une redistribution.

---

## Conditions préalables

- Un **jeton d'accès JWT Aspose Cloud** valide (OAuth 2.0).  
- Le classeur cible doit être stocké dans le stockage Aspose Cloud (ou vous devez spécifier le `folder`/`storageName` où il se trouve).  
- Version de l'API **v3.0** ou supérieure.  

> **Remarque :** L'opération est *idempotente* – l'appeler alors qu'aucun objet OLE n'existe renvoie un succès `200 OK`.

---

## Requête HTTP

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### Paramètres de chemin

| Nom           | Type   | Obligatoire | Description                          |
|---------------|--------|-------------|--------------------------------------|
| `name`        | string | ✔️          | Nom du fichier du classeur.          |
| `sheetName`   | string | ✔️          | Nom de la feuille de calcul.         |

### Paramètres de requête

| Nom           | Type   | Obligatoire | Description                              |
|---------------|--------|-------------|------------------------------------------|
| `folder`      | string | optionnel   | Dossier contenant le classeur.           |
| `storageName` | string | optionnel   | Nom du stockage où se trouve le classeur. |

**En-têtes**

| En-tête              | Valeur                        |
|----------------------|------------------------------|
| `Authorization`      | `Bearer <jeton jwt>`         |
| `Accept`             | `application/json`           |
| `Content-Type`       | `application/json`           |

---

## Exemple de requête (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects?folder=Samples&storageName=MyStorage" \
     -X DELETE \
     -H "Authorization: Bearer <jeton jwt>" \
     -H "Accept: application/json" \
     -H "Content-Type: application/json"
```

*Remplacez `<jeton jwt>` par un jeton d'accès valide et ajustez `folder`/`storageName` selon vos besoins.*

---

## Réponse réussie

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                      |
|------|-----------------------------|------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l'opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou invalides (par ex. type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                  |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la limite de taille.              |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                       |
---

## Exemples de SDK

Les extraits de code suivants montrent comment appeler **DeleteWorksheetOleObjects** à l’aide des SDK officiels d’Aspose.Cells Cloud. Remplacez les valeurs génériques (`<VOTRE_JETON>`, `<NOM_FICHIER>`, etc.) par vos propres données.

| Langage   | Exemple |
|-----------|---------|
| **C#**    | <details><summary>Afficher l'exemple C#</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar config = new Configuration { AccessToken = "<VOTRE_JETON>", BasePath = "https://api.aspose.cloud" };\nvar api = new OleObjectsApi(config);\napi.DeleteWorksheetOleObjects(name: "Sample.xlsx", sheetName: "Sheet1", folder: "Samples", storageName: null);\n```</details> |
| **Java**  | <details><summary>Afficher l'exemple Java</summary>```java\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.client.ApiClient;\nimport com.aspose.cells.cloud.client.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<VOTRE_JETON>");\nconfig.setBasePath("https://api.aspose.cloud");\nOleObjectsApi api = new OleObjectsApi(new ApiClient(config));\napi.deleteWorksheetOleObjects("Sample.xlsx", "Sheet1", "Samples", null);\n```</details> |
| **Python**| <details><summary>Afficher l'exemple Python</summary>```python\nfrom asposecellscloud import ApiClient, Configuration, OleObjectsApi\n\nconfig = Configuration()\nconfig.access_token = '<VOTRE_JETON>'\nconfig.host = 'https://api.aspose.cloud'\nclient = ApiClient(configuration=config)\napi = OleObjectsApi(client)\napi.delete_worksheet_ole_objects(name='Sample.xlsx', sheet_name='Sheet1', folder='Samples')\n```</details> |
| **Node.js** | <details><summary>Afficher l'exemple Node.js</summary>```javascript\nconst { OleObjectsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({ accessToken: '<VOTRE_JETON>', basePath: 'https://api.aspose.cloud' });\nlet api = new OleObjectsApi(config);\napi.deleteWorksheetOleObjects('Sample.xlsx', 'Sheet1', { folder: 'Samples' })\n  .then(() => console.log('Tous les objets OLE ont été supprimés'))\n  .catch(err => console.error(err));\n```</details> |
| **Go**    | <details><summary>Afficher l'exemple Go</summary>```go\npackage main\nimport (\n    \"context\"\n    \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = "<VOTRE_JETON>"\n    cfg.Host = "https://api.aspose.cloud"\n    api := asposecellscloud.NewOleObjectsApi(cfg)\n    _, err := api.DeleteWorksheetOleObjects(context.Background(), "Sample.xlsx", "Sheet1", map[string]interface{}{ "folder": "Samples" })\n    if err != nil { panic(err) }\n    println("Tous les objets OLE ont été supprimés")\n}\n```</details> |

*Les fichiers sources complets pour tous les langages pris en charge sont disponibles sur le [dépôt GitHub d’Aspose.Cells Cloud](https://github.com/aspose-cells-cloud).*

---

## Erreurs et gestion

- **Idempotence** – La suppression des objets OLE sur une feuille de calcul qui n’en contient déjà aucun renvoie toujours `200 OK`.  
- **Expiration du jeton** – Si vous recevez `401 Non autorisé`, obtenez un nouveau jeton JWT et réessayez.  
- **Nom de feuille de calcul incorrect** – Assurez-vous que le nom de la feuille de calcul correspond exactement (y compris la casse) à celui utilisé dans le classeur ; sinon, une erreur `400 Mauvaise requête` est renvoyée.  

Implémentez une logique de reprise avec backoff exponentiel pour les erreurs transitoires `500`.

---

## FAQ

**Q1 : Dois-je spécifier les paramètres `folder` et `storageName` ?**  
**R :** Non. Si omis, Aspose Cloud utilise le stockage par défaut et le dossier racine.

**Q2 : Puis-je supprimer des objets OLE à partir d’une cellule spécifique uniquement ?**  
**R :** Cet endpoint supprime **tous** les objets OLE présents dans la feuille de calcul. Pour supprimer un seul objet, utilisez l’opération *Supprimer un objet OLE spécifique*.

**Q3 : Que se passe-t-il si le classeur est verrouillé en mode édition ?**  
**R :** L’API renverra `400 Mauvaise requête` avec un message indiquant que le fichier est verrouillé. Assurez-vous que le fichier n’est pas ouvert ailleurs avant d’appeler l’endpoint.

**Q4 : Existe-t-il une limite de taille pour le classeur ?**  
**R :** Le service suit les limites générales de taille de fichier d’Aspose Cloud (actuellement jusqu’à 2 Go par fichier). Les fichiers plus volumineux devront être divisés ou traités par parties.

---

## Bonnes pratiques

- **Performance** – Utilisez les attributs `async` ou `defer` lors du chargement de scripts tiers sur votre site de documentation afin de réduire le temps de chargement initial de la page.  
- **Sécurité** – Ajoutez `rel="noopener noreferrer"` à tout lien externe ouvrant dans un nouvel onglet.  
- **Accessibilité** – Les icônes décoratives (par ex. flèches vers le bas dans les barres latérales) doivent comporter `alt=""` et `role="presentation"` pour respecter les normes WCAG AA.  
- **Cohérence** – Conservez les dates au format ISO‑8601 (`AAAA-MM-JJ`) afin d’éviter des artefacts d’encodage.

---

## Opérations connexes

- **Ajouter un objet OLE** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`  
- **Supprimer un objet OLE spécifique** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  

Utilisez les liens de navigation en bas de page pour passer d’une opération API à l’autre.

---
---