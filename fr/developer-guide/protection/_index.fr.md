---
title: "Aspose.Cells Cloud Web API – Définir ou modifier le mot de passe d’ouverture pour les fichiers Excel"
second_title: "Guide complet du développeur"
ArticleTitle: "Protection des classeurs – Définir le mot de passe d’ouverture et le mot de passe de modification"
linktitle: "Protection"
type: docs
url: /fr/protection/
keywords: "Aspose.Cells, Cloud, API, Classeur, Protection, Mot de passe d’ouverture, Mot de passe de modification, Excel"
description: "Découvrez comment protéger un classeur Excel à l’aide d’un mot de passe d’ouverture ou de modification avec l’API REST Aspose.Cells Cloud. Inclut la syntaxe des requêtes, des exemples de code et la gestion des erreurs."
weight: 60
---

Dans ce guide, vous apprendrez comment définir, modifier et supprimer à la fois le **mot de passe d’ouverture** et le **mot de passe de modification** pour les classeurs à l’aide de l’API Web Aspose.Cells Cloud. Ces fonctionnalités permettent de protéger les données sensibles de vos classeurs Excel.

**Conditions préalables**  
- Un compte Aspose.Cells Cloud actif disposant d’une clé API et d’un SID valides.  
- Le classeur que vous souhaitez protéger doit être téléchargé dans le stockage Aspose Cloud ou accessible via une URL publique.  

**Référence de l’API**  

| **Méthode HTTP** | **Point de terminaison** | **Paramètres de requête / chemin** | **Description** |
|------------------|--------------------------|------------------------------------|-----------------|
| `PUT` | `/cells/{fileName}/protection` | `fileName` (chemin) – nom du classeur<br>`openPassword` (requête, facultatif) – mot de passe requis pour ouvrir le fichier<br>`readWritePassword` (requête, facultatif) – mot de passe requis pour modifier le fichier | Définit ou met à jour les mots de passe d’ouverture et/ou de modification pour le classeur spécifié. |
| `DELETE` | `/cells/{fileName}/protection` | `fileName` (chemin) – nom du classeur | Supprime tous les mots de passe protégeant le classeur. |

**Exemple de corps de requête (JSON)**  

```json
{
  "OpenPassword": "MonMotDePasseOuverture123",
  "ReadWritePassword": "MonMotDePasseModification456"
}
```

**Exemple de réponse (JSON)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "La protection du classeur a été mise à jour avec succès."
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Le filtre a été appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite autorisée. |
| 500  | Erreur interne du serveur   | Erreur inattendue sur le serveur. |

**Exemples de code**

*C# (SDK Aspose.Cells Cloud)*  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("VOTRE_ID_CLIENT", "VOTRE_SECRET_CLIENT");
var request = new SetWorkbookProtectionRequest(
    name: "Exemple.xlsx",
    openPassword: "MonMotDePasseOuverture123",
    readWritePassword: "MonMotDePasseModification456"
);
apiInstance.SetWorkbookProtection(request);
```

*Python (SDK Aspose.Cells Cloud)*  

```python
import asposecellscloud
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models import SetWorkbookProtectionRequest

api = CellsApi(client_id="VOTRE_ID_CLIENT", client_secret="VOTRE_SECRET_CLIENT")
request = SetWorkbookProtectionRequest(
    name="Exemple.xlsx",
    open_password="MonMotDePasseOuverture123",
    read_write_password="MonMotDePasseModification456"
)
api.set_workbook_protection(request)
```

**Gestion des erreurs**  
Lorsqu’une erreur se produit, l’API renvoie une charge utile JSON contenant `Code`, `Message` et, éventuellement, `Description`. Vérifiez le code de statut et gérez-le en conséquence dans la logique de votre application.

**Sujets associés**  

- **[Comment protéger un classeur à l’aide d’un mot de passe avec Aspose.Cells Cloud](https://docs.aspose.cloud/cells/protect-spreadsheet/).**  
- **[Comment déprotéger un classeur à l’aide d’un mot de passe avec Aspose.Cells Cloud](https://docs.aspose.cloud/cells/unprotect-spreadsheet/).**  
---