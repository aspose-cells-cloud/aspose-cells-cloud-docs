---
title: "Aspose.Cells Cloud Web API – Traduire une feuille de calcul vers une langue cible"
second_title: "Document"
ArticleTitle: "Comment traduire une feuille de calcul entière à l’aide de l’API de traduction IA d’Aspose.Cells Cloud"
linktitle: "Traduire une feuille de calcul"
type: docs
url: /fr/translate-spreadsheet/
keywords: "Aspose.Cells Cloud, API de traduction de feuille de calcul, traduction IA, traduction de feuille de calcul, targetLanguage, traduction multi-feuilles, traitement de feuille de calcul dans le cloud, traduction Aspose.Cells Cloud"
description: "Traduisez un classeur Excel complet à l’aide d’Aspose.Cells Cloud IA. Préservez les formules, les graphiques et la mise en forme tout en convertissant le texte vers n’importe quelle langue prise en charge. Découvrez le point de terminaison, les paramètres, les exemples de SDK, les limites et la gestion des erreurs."
weight: 100
---

Le point de terminaison **TranslateSpreadsheet**, faisant partie de l’**API de traduction de feuille de calcul**, lit chaque élément textuel d’un classeur, envoie le contenu vers un service de traduction alimenté par l’IA, puis renvoie un nouveau fichier de feuille de calcul dans lequel toutes les données textuelles sont rendues dans la **targetLanguage** spécifiée. L’opération conserve la mise en page d’origine, les styles de cellule, les formules et **la** structure multi-feuilles intacte, ce qui en fait une solution idéale pour internationaliser des rapports, des tableaux de bord et des documents basés sur des données. Les formats de fichier pris en charge incluent XLS, XLSX, XLSM, CSV et ODS. Des erreurs sont renvoyées en cas de codes de langue invalides, d’échecs d’authentification ou de pannes du service de traduction.

## **API de traduction de feuille de calcul**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/spreadsheet
```

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement | Obligatoire / facultatif | Description                                                                                                                                                                                                 |
| :--------------- | :----- | :---------- | :----------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | Requis     | FormData                 | Le classeur Excel à traduire. Extensions acceptées : .xls, .xlsx, .xlsm, .csv, .ods. Taille maximale du fichier : 50 Mo. Exemple : `budget.xlsx`.                                                               |
| targetLanguage   | string | Requis     | Query                    | Code de langue ISO 639‑1 pour la langue cible souhaitée (par exemple, « es » pour l’espagnol, « fr » pour le français, « de » pour l’allemand). Doit correspondre à une langue prise en charge par le service IA sous-jacent. |
| region           | string | Facultatif | Query                    | Identifiant de région de la feuille de calcul influençant la mise en forme spécifique à la localisation (dates, nombres, devises). Valeurs courantes : « US », « EU », « CN ». Si omis, le paramètre de région d’origine du classeur est utilisé. |
| password         | string | Facultatif | Query                    | Mot de passe permettant d’ouvrir un classeur protégé. Laisser vide si le fichier n’est pas protégé par un mot de passe.                                                                                     |

### **Réponse**

Réponse réussie (200 OK)  
En‑têtes :  
Content‑Type: application/octet-stream // ou text/csv si une sortie CSV est demandée  
Content‑Disposition: attachment; filename="translated.xlsx"  
Content‑Length: <taille en octets>

Corps :  
<flux binaire contenant le fichier de feuille de calcul traduit>

Les réponses d’erreur suivent le modèle d’erreur standard d’Aspose.Cells Cloud (application/json), avec les champs `code`, `message` et éventuellement `details`.

**Codes d’état HTTP**

| Code | Signification         | Description                                                      |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte    | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT non valide ou manquant.                                |
| 413  | Charge utile trop volumineuse | Le fichier envoyé dépasse la limite de taille.                         |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                         |

## Où utiliser l’API de traduction de feuille de calcul ?

- **Rapports financiers internationaux** – Convertir des rapports Excel trimestriels en plusieurs langues pour les bureaux régionaux, tout en préservant les formules et la mise en page des graphiques.
- **Tableaux de bord marketing multilingues** – Générer automatiquement des versions localisées de tableaux de bord de performance des ventes pour les équipes mondiales.
- **Distribution de contenus éducatifs** – Traduire des carnet de notes, des feuilles d’exercices ou des feuilles de calcul pédagogiques pour les élèves de différents pays, sans recourir à des copier-coller manuels.
- **Conformité réglementaire** – Produire des feuilles de calcul de conformité spécifiques à chaque langue, tout en conservant les règles de validation et les listes de validation des données.

## Pourquoi utiliser l’API de traduction de feuille de calcul ?

- **Précision basée sur l’IA** – Exploite des modèles neuronaux de pointe pour une conversion linguistique contextuelle et de haute qualité.
- **Aucune modification de la mise en page** – Conserve exactement les formules de cellule, le formatage conditionnel, les graphiques et l’ordre des feuilles du fichier source.
- **Traitement multi-feuilles en une seule requête** – Traduit chaque feuille de calcul en une seule demande, éliminant le besoin de boucles par feuille.
- **Intégration fluide dans le cloud** – Fonctionne avec l’authentification Aspose.Cells Cloud, permettant des pipelines automatisés dans CI/CD, des fonctions serverless ou des systèmes back-end d’entreprise.

## Comment utiliser l’API de traduction de feuille de calcul avec les SDK ?

### Spécification de l’API de traduction de feuille de calcul

La [Spécification de l’API de traduction de feuille de calcul](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/TranslateSpreadsheet) fournit une interface de programmation publiquement accessible pour exécuter directement des interactions REST depuis un navigateur web.

## SDK d’API Excel

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant d’intégrer une feuille de calcul dans une autre à l’aide d’un code minimal.  
Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.  
Les exemples de code suivants illustrent comment interagir avec les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}