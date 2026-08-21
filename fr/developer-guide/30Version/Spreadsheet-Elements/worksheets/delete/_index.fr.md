---
title: "Comment gérer la suppression de feuilles de calcul dans un classeur Excel"
second_title: "Document"
linktype: "Supprimer"
type: docs
url: /fr/worksheets/delete/
keywords: "Aspose.Cells, Cloud, API REST, Supprimer une feuille de calcul, Excel, C#, Java, Python"
description: "Découvrez comment supprimer une ou plusieurs feuilles de calcul à partir d’un classeur Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut des exemples en C#, Java et Python, les conditions préalables, des conseils sur la gestion des erreurs et les opérations associées."
weight: 20
ArticleTitle: "Supprimer une ou plusieurs feuilles de calcul dans un classeur Excel à l’aide de l’API Aspose.Cells Cloud"
---

## Gestion de la suppression de feuilles de calcul dans un classeur Excel

Lorsqu’une application génère ou modifie dynamiquement des fichiers Excel, vous pouvez avoir besoin de supprimer des feuilles de calcul qui ne sont plus nécessaires — telles que des rapports temporaires, des feuilles de remplacement ou des données obsolètes. L’API REST Aspose.Cells Cloud facilite la suppression d’une seule feuille de calcul ou de plusieurs feuilles de calcul en une seule requête.

**Référence API**

| Élément | Détails |
|--------|---------|
| **Méthode HTTP** | `DELETE` |
| **Point de terminaison** | `/cells/{fileName}/worksheets` |
| **Paramètres de chemin** | `fileName` – nom du fichier Excel (obligatoire) |
| **Paramètres de requête** | `sheetName` – nom de la feuille de calcul à supprimer (facultatif, pour une suppression unique) <br> `folder` – dossier source dans le stockage (facultatif) <br> `storage` – nom du stockage (facultatif) |
| **Corps de la requête** | *Aucun* |
| **Réponse en cas de succès** | `200 OK` – feuille(s) de calcul supprimée(s) avec succès. Renvoie un objet JSON contenant le statut de l’opération. |
| **Réponses d’erreur** | `400 Bad Request` – paramètres non valides <br> `401 Unauthorized` – échec d’authentification <br> `404 Not Found` – fichier ou feuille de calcul introuvable <br> `500 Internal Server Error` – problème côté serveur |

**Requête**

Pour supprimer une ou plusieurs feuilles de calcul, envoyez une requête `DELETE` vers le point de terminaison ci-dessus, en incluant le paramètre obligatoire `fileName` et éventuellement le paramètre de requête `sheetName` pour une suppression unique. Lorsque `sheetName` est omis, toutes les feuilles de calcul du classeur sont supprimées.

**Paramètres**

- `fileName` (chaîne, obligatoire) : Nom du fichier Excel, incluant l’extension.  
- `sheetName` (chaîne, facultatif) : Nom spécifique de la feuille de calcul à supprimer. Si omis, l’API supprime toutes les feuilles de calcul.  
- `folder` (chaîne, facultatif) : Chemin du dossier contenant le fichier dans le stockage.  
- `storage` (chaîne, facultatif) : Nom du stockage Aspose Cloud à utiliser.

**Réponses**

- **200 OK** – Exemple de JSON :  
  ```json
  {
    "code": 200,
    "status": "OK",
    "message": "Feuille(s) de calcul supprimée(s) avec succès."
  }
  ```
- **400 Bad Request** – Paramètres de requête non valides.  
- **401 Unauthorized** – Jeton d’authentification manquant ou non valide.  
- **404 Not Found** – Le fichier ou la feuille de calcul spécifié n’existe pas.  
- **500 Internal Server Error** – Erreur serveur inattendue.

**Exemples**

*Ci-dessous figurent de courts extraits de code illustrant comment appeler le point de terminaison de suppression à l’aide de trois langages populaires.*

**Exemple en C#**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("client_id", "client_secret");
var fileName = "Sample.xlsx";
var sheetName = "TempSheet";

try
{
    var response = api.DeleteWorksheet(fileName, sheetName);
    Console.WriteLine($"Statut : {response.Status}");
}
catch (Exception ex)
{
    Console.WriteLine($"Erreur : {ex.Message}");
}
```

**Exemple en Java**  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.ResponseMessage;

public class DeleteWorksheetDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String fileName = "Sample.xlsx";
        String sheetName = "TempSheet";

        try {
            ResponseMessage response = api.deleteWorksheet(fileName, sheetName, null, null);
            System.out.println("Statut : " + response.getStatus());
        } catch (Exception e) {
            System.err.println("Erreur : " + e.getMessage());
        }
    }
}
```

**Exemple en Python**  
```python
from asposecellscloud import CellsApi, ApiException

api = CellsApi(client_id="client_id", client_secret="client_secret")
file_name = "Sample.xlsx"
sheet_name = "TempSheet"

try:
    response = api.delete_worksheet(file_name, sheet_name)
    print(f"Statut : {response.status}")
except ApiException as e:
    print(f"Erreur : {e}")
```

**Gestion des erreurs**

- Vérifiez que le jeton d’authentification est valide avant d’envoyer la requête.  
- Vérifiez le code de statut de la réponse ; gérez les erreurs `400`, `401`, `404` et `500` en conséquence.  
- Utilisez des blocs try-catch (ou équivalent) pour capturer les exceptions réseau ou liées au SDK.

**Opérations associées**

- [Ajouter une feuille de calcul](/worksheets/add/) – Créer une nouvelle feuille de calcul dans un classeur existant.  
- [Copier une feuille de calcul](/worksheets/copy/) – Dupliquer une feuille de calcul existante.  
- [Renommer une feuille de calcul](/worksheets/rename/) – Modifier le nom d’une feuille de calcul.  
- [Déplacer une feuille de calcul](/worksheets/move/) – Réorganiser les feuilles de calcul dans un classeur.  
---