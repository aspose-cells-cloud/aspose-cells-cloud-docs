---
title: "Aspose.Cells Cloud Excel – API Web pour ajouter une feuille de calcul – Insérer de nouvelles feuilles avec contrôle du type et de la position"
second_title: "Document"
ArticleTitle: "Comment ajouter des feuilles de calcul à Excel – Insérer de nouvelles feuilles à des emplacements spécifiques"
linktitle: "Ajouter une feuille de calcul à un classeur"
type: docs
url: /fr/add-worksheet-to-spreadsheet/
keywords: "excel, ajouter une feuille de calcul, aspose cells api, classeur, api cloud, type de feuille, position de la feuille"
description: "Découvrez comment ajouter programmatically une nouvelle feuille de calcul, une feuille graphique ou une feuille de macro à un classeur Excel à l’aide de l’API Aspose.Cells Cloud. Contrôlez le type, le nom et la position d’insertion de la feuille en une seule requête REST."
weight: 100
---

Ajoutez programmatically des feuilles de calcul à des fichiers Excel, avec un contrôle complet sur le type et l’emplacement de la feuille. Insérez des feuilles de calcul standard, des feuilles graphiques ou des feuilles de macro à n’importe quelle position dans le classeur. Cette opération RESTful permet la gestion et l’organisation automatisées des classeurs Excel.

**Prérequis**

- Un compte Aspose.Cells Cloud actif disposant d’un jeton d’accès JWT valide.
- Un nom de stockage cloud configuré (par exemple, `CompanyOneDrive`) où le classeur sera enregistré.
- Le classeur cible doit être accessible dans le stockage spécifié ; s’il est protégé par mot de passe, le mot de passe correct doit être fourni.

| **Type de feuille**       | Description                                               |
| :------------------------ | :-------------------------------------------------------- |
| **VB**                    | Module Visual Basic                                       |
| **Worksheet**             | Feuille de calcul standard                                |
| **Chart**                 | Feuille graphique                                         |
| **BIFF4Macro**            | Feuille de macro BIFF4                                    |
| **InternationalMacro**    | Feuille de macro internationale                           |
| **Other**                 | Type de feuille personnalisé ou moins courant non listé ci-dessus |
| **Dialog**                | Feuille de dialogue                                       |

## **API d’ajout d’une feuille de calcul à un classeur**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre   | Type    | Emplacement | Description                                                                                                                                                                                          |
| :----------------- | :------ | :---------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | Fichier | FormData    | **Obligatoire.** Le classeur Excel (.xlsx, .xls, etc.) auquel une nouvelle feuille sera ajoutée.                                                                                                         |
| **sheetType**      | Chaîne  | Query       | **Facultatif.** Le type de feuille à créer. Les valeurs acceptables sont `worksheet` (par défaut), `chartsheet`, `macrosheet`, `vbmodule` et `dialog`.                                                        |
| **position**       | Entier  | Query       | **Facultatif.** Index de base zéro indiquant l’emplacement d’insertion de la nouvelle feuille. `0` insère avant la première feuille ; `2` insère comme troisième feuille. Omettre pour ajouter la feuille à la fin.                                       |
| **sheetName**      | Chaîne  | Query       | **Facultatif.** Nom de la nouvelle feuille de calcul. Doit être unique dans le classeur. Si omis, un nom par défaut tel que « FeuilleX » est généré.                                                              |
| **outPath**        | Chaîne  | Query       | **Facultatif.** Répertoire cible dans le stockage cloud où le classeur modifié sera enregistré. Si `null` ou omis, le classeur est enregistré à l’emplacement du fichier source ou dans un chemin par défaut. |
| **outStorageName** | Chaîne  | Query       | **Obligatoire.** Identifiant du stockage cloud configuré (par exemple, `CompanyOneDrive`) où le fichier de sortie doit être écrit.                                                                          |
| **region**         | Chaîne  | Query       | **Facultatif.** Paramètre régional (par exemple, `fr‑CA`) pouvant affecter le formatage et les règles régionales dans la nouvelle feuille.                                                                                     |
| **password**       | Chaîne  | Query       | **Facultatif.** Mot de passe permettant de déchiffrer et modifier un classeur protégé par mot de passe. Omettre si le fichier n’est pas chiffré.                                                                                       |

### Réponse

En cas de succès, l’API renvoie **HTTP 200 OK** (ou **201 Created** si un nouveau fichier est généré), accompagnée du classeur mis à jour.

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

**Codes d’état HTTP**

| Code | Signification         | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte    | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT invalide ou manquant.                                     |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille maximale autorisée.                                 |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                          |

## À quoi sert l’API d’ajout d’une feuille de calcul à un classeur ?

- **Génération automatisée de rapports** – Créer et insérer dynamiquement des feuilles mensuelles (par exemple, `2024‑05`) lors de la génération d’états financiers.
- **Initialisation par lots de modèles** – Ajouter une feuille d’analyse dédiée pour chaque nouveau client ou projet lors de la génération en masse de devis ou de propositions commerciales.
- **Extension dynamique de tableaux de bord** – Insérer des feuilles graphiques en temps réel dès que de nouvelles dimensions de données deviennent disponibles.
- **Archivage conformité et audit** – Ajouter automatiquement des feuilles de collecte de preuves lors des audits annuels, en isolant chaque point d’inspection.
- Pour supprimer une feuille, voir l’opération **[Delete Worksheet](/delete-worksheet/)**.
- Pour déplacer une feuille, voir l’opération **[Move Worksheet](/move-worksheet/)**.

## Pourquoi utiliser l’API d’ajout d’une feuille de calcul à un classeur ?

- **Adapté aux développeurs** – Aspose.Cells Cloud fournit des SDK pour de nombreux langages, réduisant l’effort de développement et offrant une documentation complète.
- **Réduction des coûts de main-d’œuvre** – Élimine la nécessité de créer manuellement des feuilles de calcul et d’effectuer des tâches répétitives de copier-coller.
- **Paiement à l’utilisation** – Vous ne payez que les appels API effectivement effectués.
- **Maintenance nulle** – Aucun serveur à gérer, aucune mise à jour logicielle à effectuer, aucune préoccupation de compatibilité.

## Comment utiliser l’API d’ajout d’une feuille de calcul à un classeur avec les SDK

### Spécification de l’API d’ajout d’une feuille de calcul à un classeur

La [spécification de l’API d’ajout d’une feuille de calcul à un classeur](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet?worksheetName=Feuille1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json" \
     -F "Spreadsheet=@/chemin/vers/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (encodé en Base64)",
  "contentType": "type MIME",
  "fileDownloadName": "nom de fichier optionnel"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK masque les détails de bas niveau, vous permettant d’ajouter une feuille de calcul avec un minimum de code. Reportez-vous à la liste complète des SDK dans le [dépôt GitHub](https://github.com/aspose-cells-cloud).

Les exemples de code suivants montrent comment appeler le service à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}