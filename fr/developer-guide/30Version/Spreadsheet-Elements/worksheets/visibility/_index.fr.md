---
title: "Comment gérer la visibilité d'une feuille de calcul Excel"
second_title: "Document"
linktitle: "Visibilité"
type: docs
url: /worksheets/panes/
keywords: "Aspose.Cells Cloud, API de masquage de feuille de calcul, API d’affichage de feuille de calcul, visibilité d’une feuille de calcul Excel, API REST Excel, Aspose.Cells v3.0"
description: "Découvrez comment masquer ou afficher des feuilles de calcul Excel de manière programmatique à l’aide de l’API REST Aspose.Cells Cloud. Inclut les URL de requête, des exemples cURL et .NET SDK, la gestion des erreurs et des notes spécifiques à chaque version."
weight: 20
---

## Gestion de la visibilité d'une feuille de calcul Excel

La *visibilité de la feuille de calcul* définit si une feuille est affichée à l’utilisateur final. Avec Aspose.Cells Cloud, vous pouvez masquer ou afficher une feuille de calcul via un appel REST simple. Les points de terminaison de l’API utilisés sont les suivants :

* **Masquer une feuille de calcul** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`  
* **Afficher une feuille de calcul** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`

> **Version d’API prise en charge :** **v3.0** (au mois de mars 2026)

### Conditions préalables
1. Un compte **Aspose.Cells Cloud** activé.  
2. Un **identifiant client** et un **secret client** valides (ou un jeton d’accès OAuth 2.0).  
3. Le classeur (`{fileName}`) doit déjà être téléchargé dans le stockage cloud Aspose.  

---

## Masquer une feuille de calcul

### Requête
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": false
}
```

### Réponse
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": false
  }
}
```

### Exemple cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer VOTRE_JETON_D’ACCÈS" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": false }'
```

### Exemple .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = false };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Feuille de calcul masquée : {response.Worksheet.Visible}");
```

### Erreurs courantes
| Code HTTP | Description                                    | Mesure correctrice                                                  |
|----------|-----------------------------------------------|---------------------------------------------------------------------|
| 400      | Corps JSON invalide ou champ `Visible` manquant | Vérifiez que le corps de la requête est un JSON valide contenant la clé. |
| 401      | Non autorisé – jeton manquant ou expiré        | Actualisez le jeton OAuth et incluez-le dans l’en-tête.            |
| 404      | Feuille de calcul ou fichier introuvable       | Vérifiez que `{fileName}` et `{sheetName}` sont corrects.          |
| 409      | Feuille de calcul déjà masquée                 | Vérifiez la visibilité actuelle avant d’envoyer la requête.        |

---

## Afficher une feuille de calcul

### Requête
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": true
}
```

### Réponse
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": true
  }
}
```

### Exemple cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer VOTRE_JETON_D’ACCÈS" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": true }'
```

### Exemple .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = true };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Feuille de calcul affichée : {response.Worksheet.Visible}");
```

### Erreurs courantes
| Code HTTP | Description                                    | Mesure correctrice                                                  |
|----------|-----------------------------------------------|---------------------------------------------------------------------|
| 400      | Corps JSON invalide ou champ `Visible` manquant | Fournissez une charge utile JSON correcte contenant `"Visible": true`. |
| 401      | Non autorisé – jeton manquant ou expiré        | Régénérez le jeton d’accès et réessayez.                           |
| 404      | Feuille de calcul ou fichier introuvable       | Vérifiez que le fichier et le nom de la feuille existent dans le stockage. |
| 409      | Feuille de calcul déjà affichée                | Aucune action nécessaire ; la feuille est déjà visible.            |

---

## Opérations associées
> *Geler les volets* | *Découper les volets* | *Zoom* – consultez les pages correspondantes pour des contrôles supplémentaires de mise en page des feuilles de calcul.

---

## Questions fréquentes

<dl>
  <dt>Comment masquer une feuille de calcul à l’aide de l’API Aspose.Cells Cloud ?</dt>
  <dd>Envoyez une requête `PUT` vers `/cells/{fileName}/worksheets/{sheetName}/visibility` avec le corps JSON `{ "Visible": false }`. Incluez un jeton porteur OAuth 2.0 valide. Une réponse `200 OK` renvoie l’objet feuille de calcul mis à jour.</dd>

  <dt>Quelle réponse reçoit-on après avoir affiché une feuille de calcul ?</dt>
  <dd>L’API renvoie `200 OK` avec une charge utile contenant l’objet feuille de calcul où `"Visible": true`. La réponse inclut les propriétés `Name`, `Index` et `Visible` de la feuille de calcul.</dd>

  <dt>Puis-je masquer plusieurs feuilles de calcul en une seule requête ?</dt>
  <dd>Non. Le point de terminaison de visibilité fonctionne sur une seule feuille de calcul identifiée par `{sheetName}`. Pour masquer plusieurs feuilles, parcourez chaque nom dans votre code client.</dd>
</dl>

---

*Rédigé par l’équipe Aspose Docs – plus de 15 ans d’expérience dans l’automatisation des flux de travail Excel.*