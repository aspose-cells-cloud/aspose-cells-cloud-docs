---
title: "Aspose.Cells Cloud Web API – Suppression automatique des lignes vides"
second_title: "Document"
ArticleTitle: "Comment supprimer toutes les lignes vides dans Excel – Guide complet de nettoyage des données"
linktitle: "Supprimer les lignes vides"
type: docs
url: /fr/delete-spreadsheet-blank-rows/
keywords: "Aspose.Cells, Excel, lignes vides, suppression de lignes, nettoyage de feuille de calcul, API"
description: "Supprimez toutes les lignes vides des fichiers Excel via l’API Aspose.Cells Cloud. Rapide, prêt pour le traitement par lots et entièrement programmable – consultez les exemples de code en C#, Java, Python, etc."
weight: 100
---

Supprimez automatiquement toutes les lignes vides des feuilles de calcul Excel à l’aide de l’API Aspose.Cells Cloud. Notre API intelligente détecte et supprime les lignes ne contenant aucune donnée, formule, commentaire ou objet, tout en préservant tout autre contenu. Elle prend en charge le traitement par lots, l’automatisation dans le cloud et l’intégration transparente dans les flux de travail d’entreprise de nettoyage des données.

## API DeleteSpreadsheetBlankRows

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/delete/blank-rows
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```


### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Description                                                                                                                                    |
|------------------|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Fichier | FormData    | Le fichier Excel (`.xlsx`, `.xls`, `.ods`, etc.) à traiter.                                                                                   |
| outPath          | Chaîne  | Query       | (Facultatif) Répertoire cible dans votre stockage cloud pour le classeur nettoyé. Si omis, le fichier est enregistré à côté du fichier source. |
| outStorageName   | Chaîne  | Query       | Nom du stockage cloud configuré (par exemple, `MyDropbox`, `CorporateOneDrive`). Obligatoire si vous souhaitez que la sortie soit stockée dans un stockage spécifique. |
| region           | Chaîne  | Query       | Paramètres régionaux (par exemple, `en-US`, `fr-FR`) appliqués lors du traitement.                                                            |
| password         | Chaîne  | Query       | Mot de passe pour ouvrir une feuille de calcul chiffrée. À omettre si le fichier n’est pas protégé.                                           |

**Authentification**  
Tous les appels doivent inclure l’en-tête `Authorization: Bearer <access_token>`. Obtenez le jeton d’accès via le flux OAuth2 Aspose Cloud décrit dans le guide d’authentification.

**Prérequis et notes**  
- Assurez-vous que votre stockage Aspose Cloud est configuré et que le classeur source est uploadé avant d’appeler l’API.  
- Les formats de fichier pris en charge incluent `.xlsx`, `.xls`, `.ods` et d’autres types courants de feuilles de calcul.  
- La taille maximale de fichier par requête est de 150 Mo ; pour des fichiers plus volumineux, procédez par morceaux.

### Réponse

L’API renvoie un tableau JSON contenant une référence au fichier traité.

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### Codes d’erreur

- **400 Bad Request** – URI invalide pour l’API Aspose.Cells Cloud.
- **401 Unauthorized** – Jeton d’accès ou identifiants client invalides.
- **404 Not Found** – Le fichier de feuille de calcul ne peut pas être accessible.
- **500 Server Error** – Une erreur inattendue est survenue lors du traitement du fichier.

## Où utiliser l’API Delete Spreadsheet Blank Rows ?

- **Flux d’importation et nettoyage des données** – Nettoyez immédiatement les lignes vides finales ou structurelles après importation de données depuis des CSV, des bases de données ou des API web.
- **Génération de rapports et tableaux de bord** – Assurez une présentation professionnelle en supprimant les lignes vides inutiles avant la finalisation des rapports financiers, commerciaux ou opérationnels.
- **Préparation des données pour l’analyse (ETL)** – Prétraitez les données Excel dans les pipelines ETL avant leur chargement dans des entrepôts de données (Snowflake, BigQuery) ou des outils BI (Tableau, Power BI).
- **Intégration système et flux API** – Normalisez les fichiers Excel reçus depuis des systèmes partenaires, des CRM ou des ERP en supprimant les lignes inutilisées.
- **Automatisation documentaire et traitement par lots** – Supprimez les lignes d’exemple générées par des moteurs de modèles avant la distribution.
- **Traitement de contenus générés par les utilisateurs** – Standardisez les fichiers Excel uploadés depuis des portails web ou applications avant un traitement ou stockage ultérieur.
- **Migration de données anciennes** – Simplifiez les archives de feuilles de calcul anciennes en supprimant les lignes historiquement vides ou d’exemple.

## Pourquoi utiliser l’API Delete Spreadsheet Blank Rows ?

- **Adapté aux développeurs** – Des SDK sont disponibles pour de nombreux langages, réduisant l’effort de développement par rapport à la construction de solutions personnalisées.
- **Réduction des coûts de main-d’œuvre** – Élimine le besoin de nettoyage manuel des feuilles de calcul ou d’un personnel dédié.
- **Paiement à l’usage** – Vous ne payez que pour les appels API effectivement réalisés.
- **Zéro coût de maintenance** – Aucun serveur à gérer, aucune mise à jour logicielle et aucune préoccupation de compatibilité.

## Comment utiliser l’API Delete Spreadsheet Blank Rows avec les SDK ?

### Spécification de l’API Delete Spreadsheet Blank Rows

La [Spécification de l’API Delete Spreadsheet Blank Rows](https://reference.aspose.cloud/cells/#/TransformController/DeleteSpreadsheetBlankRows) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau et permet de supprimer les lignes vides dans les feuilles de calcul à l’aide de code concis.  
Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankRows.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankRows.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankRows.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankRows.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankRows.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankRows.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankRows.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankRows.go" >}}  
{{</tab>}}  
{{< /tabs >}}