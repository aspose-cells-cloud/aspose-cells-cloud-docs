---
title: "Converter une plage Excel en CSV – Aspose.Cells Cloud API"
second_title: "Document"
articleTitle: "Comment convertir une plage locale de classeur en fichier CSV : Guide pas à pas"
linktype: "docs"
url: "/convert-range-to-csv/"
keywords: "Aspose Cells, convertir une plage en CSV, Excel en CSV, API Excel, classeur cloud, conversion, Excel, CSV, Aspose.Cells, API cloud"
description: "Découvrez comment convertir une plage spécifique d’un classeur Excel local (XLSX ou XLS) en CSV à l’aide de l’API REST Aspose.Cells Cloud. Inclut la syntaxe des requêtes, les paramètres, la gestion des erreurs et des exemples SDK."
---

Exportez une plage spécifique d’un fichier Excel local au format CSV à l’aide de l’API Aspose.Cells Cloud.

## **API de conversion de plage en CSV**

**Prérequis**  
Pour appeler ce point de terminaison, vous devez disposer d’un **ID client** et d’un **secret client** Aspose Cloud valides, obtenir un **jeton d’accès JWT**, et vous assurer que le classeur source est au format **XLSX** ou **XLS**.

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/csv
```

**Exemple cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/csv?worksheet=Feuil1&range=A1:C10" \
     -H "Authorization: Bearer {jeton_d_accès}" \
     -F "Spreadsheet=@exemple.xlsx"
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                              |
| :--------------- | :----- | :---------------------------------------------------- | :----------------------------------------------------------------------- |
| Spreadsheet      | Fichier | FormData                                              | Téléchargez le fichier de classeur.                                      |
| worksheet        | Chaîne  | Chaîne de requête                                     | Nom de la feuille de calcul.                                             |
| range            | Chaîne  | Chaîne de requête                                     | Zone de cellules à spécifier (par exemple, A1:C10).                      |
| outPath          | Chaîne  | Chaîne de requête                                     | Chemin du dossier où le classeur sera stocké (facultatif). Par défaut : null. |
| outStorageName   | Chaîne  | Chaîne de requête                                     | Nom du stockage de sortie.                                               |
| fontsLocation    | Chaîne  | Chaîne de requête                                     | Spécifiez des polices personnalisées si nécessaire.                      |
| region           | Chaîne  | Chaîne de requête                                     | Définit le paramètre de région du classeur.                              |
| password         | Chaîne  | Chaîne de requête                                     | Mot de passe requis pour ouvrir le fichier de classeur.                 |

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

_Exemple de contenu CSV renvoyé (premières lignes) :_

```csv
Nom,Date,Montant
Jean Dupont,2023-01-15,1250.00
Marie Martin,2023-01-16,980.50
```

**Codes de statut HTTP**

| Code | Signification          | Description                                                           |
| ---- | ---------------------- | --------------------------------------------------------------------- |
| 200  | OK                     | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête       | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé           | Jeton JWT invalide ou manquant.                                       |
| 413  | Charge utile trop grande | Le fichier téléchargé dépasse la taille limite.                    |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                          |

## Où utiliser l’API de conversion de plage en CSV ?

### **1. Scénarios d’exportation et de migration de données**

- **Intégration avec base de données** : Exportez des plages Excel spécifiques directement vers des systèmes de base de données.
- **Intégration d’applications** : Alimentez des applications SaaS avec des données sélectionnées à partir de classeurs.
- **Migration de systèmes** : Transférez des plages de données spécifiques entre systèmes hérités et modernes.
- **Partage multiplateforme** : Partagez des sous-ensembles de données ciblés entre différentes plateformes.

### **2. Rapports et analytique**

- **Rapports ciblés** : Exportez des sections spécifiques de rapports au format CSV pour une analyse ciblée.
- **Flux de données pour tableaux de bord** : Fournissez des plages de données spécifiques aux outils de tableaux de bord BI.
- **Métriques de performance** : Extrayez des plages de KPI pour les systèmes de suivi des performances.
- **Rapports financiers** : Exportez des sections d’états financiers à des fins d’audit externe.

### **3. Développement et tests**

- **Gestion des données de test** : Exportez des plages spécifiques à des fins de test.
- **Environnements de développement** : Partagez des plages d’échantillons de données avec les équipes de développement.
- **Tests d’API** : Générez des données CSV de test à partir de sections spécifiques de classeurs.
- **Développement de prototypes** : Fournissez des jeux de données ciblés pour les prototypes d’applications.

### **4. Opérations métier**

- **Partage sélectif de données** : Partagez des plages spécifiques avec des partenaires externes.
- **Sauvegarde partielle des données** : Sauvegardez des plages critiques au format CSV.
- **Transfert interne de données** : Partagez des données spécifiques entre départements.
- **Rapports de conformité** : Exportez des plages de données réglementaires pour les soumissions de conformité.

### **5. Automatisation des flux de travail**

- **Exportations planifiées de plages** : Exportez automatiquement des plages spécifiques selon un calendrier.
- **Extraction déclenchée** : Exportez des plages selon des événements ou déclencheurs métier.
- **Intégration dans les flux de travail** : Intégrez les exports de plages dans les flux de travail métier.
- **Traitement par lots de plages** : Traitez plusieurs plages spécifiques en une seule opération en lot.

## Pourquoi utiliser l’API de conversion de plage en CSV ?

- Vous pouvez convertir une plage de classeur sans avoir à la télécharger au préalable, ce qui économise de l’espace de stockage et réduit les coûts.
- Le développement peut être réalisé rapidement à l’aide des SDK existants d’Aspose.Cells Cloud.
- **Intégration simple** : API REST accompagnée d’une documentation claire.
- **Architecture évolutif** : Gère des opérations allant de la petite échelle à l’échelle entreprise.

## Comment utiliser l’API de conversion de plage en CSV avec les SDK ?

### Spécification OpenAPI

La [spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToCSV) décrit une API publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

## Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant de convertir une plage de données en fichier CSV avec un minimum de code.  
Consultez la liste complète des SDK Aspose.Cells Cloud sur notre [dépôt GitHub](https://github.com/aspose-cells-cloud).

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK. Si le chargement à partir de Gist est bloqué, vous pouvez télécharger directement les exemples depuis le dépôt.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}