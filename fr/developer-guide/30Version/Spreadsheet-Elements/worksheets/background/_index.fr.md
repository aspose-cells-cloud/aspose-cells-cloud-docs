---
title: "Ajouter ou supprimer une image d’arrière-plan de feuille de calcul – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Arrière-plan"
type: docs
url: /fr/worksheets/background/
keywords: "Aspose.Cells Cloud, arrière-plan de feuille de calcul, API Excel, ajouter une image d’arrière-plan, supprimer l’arrière-plan de feuille de calcul, exemples de SDK"
description: "Découvrez comment ajouter ou supprimer une image d’arrière-plan sur une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut la syntaxe des requêtes, des exemples de SDK pour Java, .NET, Python, PHP et la gestion des erreurs."
weight: 20
ArticleTitle: "Ajouter ou supprimer une image d’arrière-plan de feuille de calcul à l’aide de l’API Aspose.Cells Cloud"
---

## Gestion de l’arrière-plan d’une feuille de calcul Excel

**Vue d’ensemble :** Un arrière-plan de feuille de calcul est une image qui apparaît derrière les cellules d’une feuille, utile pour le branding ou pour fournir des repères visuels. L’API Aspose.Cells Cloud vous permet d’ajouter ou de supprimer programmatically cette image d’arrière-plan.

**Prérequis :**  
- Jeton d’accès valide à Aspose.Cells Cloud (OAuth 2.0).  
- Un classeur Excel stocké dans le cloud.  
- Un fichier image (PNG, JPEG, BMP) servant d’arrière-plan.

- **Ajouter un arrière-plan** – Définir une image d’arrière-plan sur une feuille de calcul. Consultez le guide détaillé [Comment définir un arrière-plan sur une feuille de calcul Excel](/cells/worksheets/background/add/).  
- **Supprimer un arrière-plan** – Supprimer une image d’arrière-plan existante d’une feuille de calcul. Consultez le guide détaillé [Comment supprimer un arrière-plan sur une feuille de calcul Excel](/cells/worksheets/background/delete/).

L’utilisation d’un arrière-plan de feuille de calcul peut améliorer le branding, mettre en évidence des sections importantes ou fournir des repères visuels aux utilisateurs finaux. L’API Aspose.Cells Cloud simplifie la définition ou la suppression directe de cette image d’arrière-plan depuis votre application.

### Référence de l’API

| Opération | Méthode HTTP | Point de terminaison | Paramètres de chemin | Corps de la requête | Réponse en cas de succès |
|-----------|-------------|----------------------|--------------------|----------------------|--------------------------|
| Ajouter un arrière-plan | PUT | `/cells/{name}/worksheets/{sheetName}/background` | `name` – nom du fichier du classeur<br>`sheetName` – feuille de calcul cible | Fichier image (PNG, JPEG, BMP) en tant que multipart/form‑data | `200 OK` – arrière-plan appliqué |
| Supprimer un arrière-plan | DELETE | `/cells/{name}/worksheets/{sheetName}/background` | `name` – nom du fichier du classeur<br>`sheetName` – feuille de calcul cible | *aucun* | `200 OK` – arrière-plan supprimé |

#### Exemple (SDK Java)

```java
// Ajouter une image d’arrière-plan
CellsApi cellsApi = new CellsApi("client_id", "client_secret");
File image = new File("chemin/vers/arrière-plan.png");
cellsApi.putWorksheetBackground("Book1.xlsx", "Sheet1", image, null);

// Supprimer l’image d’arrière-plan
cellsApi.deleteWorksheetBackground("Book1.xlsx", "Sheet1", null);
```

#### Exemple (SDK Python)

```python
import asposecellscloud
api = asposecellscloud.CellsApi(client_id="VOTRE_ID_CLIENT", client_secret="VOTRE_CLE_SECRETE_CLIENT")

# Ajouter un arrière-plan
with open("arrière-plan.png", "rb") as img:
    api.put_worksheet_background("Book1.xlsx", "Sheet1", img)

# Supprimer l’arrière-plan
api.delete_worksheet_background("Book1.xlsx", "Sheet1")
```

Pour d’autres exemples dans d’autres langages (C#, PHP, Ruby), veuillez vous référer à la documentation du SDK.

**Sujets connexes**  
- Pour en savoir plus sur la gestion des feuilles de calcul en général : [Vue d’ensemble des feuilles de calcul](/cells/worksheets/).  
- Pour comprendre comment s’authentifier auprès d’Aspose.Cells Cloud : [Guide d’authentification de l’API](/cells/authentication/).  
- Pour explorer d’autres éléments de feuilles de calcul tels que les graphiques, les tableaux et les formules : [Index des éléments de feuilles de calcul](/cells/elements/).
---