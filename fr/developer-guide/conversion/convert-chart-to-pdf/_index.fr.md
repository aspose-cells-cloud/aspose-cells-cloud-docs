---
title: "Aspose.Cells Cloud API – Convertir un graphique Excel en PDF"
second_title: "Document"
ArticleTitle: "Comment convertir un graphique de classeur local en fichier PDF : guide pas à pas"
linktype: "Convertir un graphique en PDF"
type: docs
url: /fr/convert-chart-to-pdf/
keywords: "Aspose Cells, graphique, PDF, Excel, conversion, API cloud"
description: "Exporter des graphiques à partir de fichiers Excel locaux au format PDF à l’aide de l’API REST Aspose.Cells Cloud. Prend en charge les fichiers XLSX et XLS."
weight: 100
---

Exporter des graphiques à partir d’un fichier Excel local au format [PDF](https://docs.fileformat.com/pdf/) à l’aide de l’API Cloud.

## **Convertir un graphique en PDF – API Web**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête :**

| Nom du paramètre | Type    | Emplacement (Chemin / Chaîne de requête / Corps HTTP) | Description                                                                 |
| ---------------- | ------- | ----------------------------------------------------- | --------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | FormData                                              | Télécharger le fichier de classeur.                                         |
| worksheet        | Chaîne  | Chaîne de requête                                     | Nom de la feuille de calcul contenant le graphique.                        |
| chartIndex       | Entier  | Chaîne de requête                                     | Index du graphique à convertir.                                             |
| outPath          | Chaîne  | Chaîne de requête                                     | (Facultatif) Chemin du dossier où le fichier converti sera enregistré. La valeur par défaut est null. |
| outStorageName   | Chaîne  | Chaîne de requête                                     | Nom du stockage destiné au fichier de sortie.                              |
| fontsLocation    | Chaîne  | Chaîne de requête                                     | Utiliser des polices personnalisées si nécessaire.                         |
| region           | Chaîne  | Chaîne de requête                                     | Paramètre régional du classeur.                                             |
| password         | Chaîne  | Chaîne de requête                                     | Mot de passe pour ouvrir le fichier de classeur.                           |

### **Réponse**

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

**Codes de statut HTTP**

| Code | Signification           | Description                                                      |
| ---- | ----------------------- | ---------------------------------------------------------------- |
| 200  | OK                      | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte      | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé            | Jeton JWT invalide ou manquant.                                  |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille maximale autorisée.     |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                      |

## À quoi sert l’API Convert Chart to PDF ?

### **1. Rapports et automatisation professionnels**

- **Services financiers** : Graphiques des rapports financiers mensuels → Archivage en PDF
- **Équipes commerciales** : Graphiques des tendances de performance → Rapports clients en PDF
- **Analyse marketing** : Graphiques de performance des campagnes → Résumés exécutifs en PDF
- **Gestion opérationnelle** : Graphiques de suivi de production → Documents de conformité en PDF

### **2. Développement logiciel et intégration**

- **Applications SaaS** : Données de graphiques générées par l’utilisateur → Rapports PDF téléchargeables
- **Systèmes d’entreprise** : Graphiques des systèmes ERP/CRM → Documentation d’audit en PDF
- **Applications mobiles** : Graphiques d’analyse intégrés → Fichiers PDF partageables
- **Applications web** : Graphiques des tableaux de bord → Fonctionnalité d’export PDF

### **3. Flux de travail de traitement de documents**

- **Traitement par lots** : Conversion simultanée en PDF de plusieurs graphiques à partir de fichiers Excel
- **Tâches planifiées** : Génération automatisée de rapports hebdomadaires ou quotidiens
- **Sorties basées sur des modèles** : Formats de graphique standard → Documents PDF
- **Assemblage de documents** : Combiner des graphiques avec d’autres contenus au format PDF

### **4. Applications spécifiques aux secteurs**

- **Établissements de recherche** : Graphiques de données expérimentales → Figures pour articles scientifiques en PDF
- **Secteur éducatif** : Graphiques de supports pédagogiques → Matériel pédagogique en PDF
- **Sociétés de conseil** : Graphiques d’analyse → Livrables clients en PDF
- **Industrie manufacturière** : Graphiques de contrôle qualité → Rapports d’inspection en PDF
- **Santé** : Graphiques de données patients → Dossiers médicaux en PDF
- **Secteur public** : Graphiques statistiques → Publications officielles en PDF

### **5. Gestion et diffusion de contenu**

- **Gestion des actifs numériques** : Archivage des graphiques au format PDF normalisé
- **Bases de connaissances** : Documentation technique incluant des graphiques intégrés en PDF
- **Portails clients** : Livraison sécurisée de rapports PDF aux parties prenantes
- **Conformité réglementaire** : Génération de documentation PDF prête à l’audit

## Pourquoi utiliser l’API Convert Chart to PDF ?

- Vous pouvez convertir des graphiques **sans avoir à télécharger préalablement le classeur**, ce qui permet d’économiser de l’espace de stockage et de réduire les coûts.
- Le développement peut être rapidement achevé à l’aide des SDK Aspose.Cells Cloud existants.
- **Intégration simplifiée** : API REST avec documentation claire.
- **Architecture évolutive** : Prend en charge des charges de travail allant des petites aux grandes opérations d’entreprise.

## Comment utiliser l’API Convert Chart to PDF avec les SDK ?

### Spécification de l’API Convert Chart to PDF

La [spécification de l’API Convert Chart to PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPDF) définit une interface de programmation publiquement accessible et permet d’effectuer directement des interactions REST depuis un navigateur web.

## Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant de convertir un graphique en fichier PDF avec un nombre minimal de lignes de code.  
Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}