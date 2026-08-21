---
title: "Enregistrer une feuille de calcul dans un autre format – API Aspose.Cells Cloud (v4.0)"
second_title: "Document"
ArticleTitle: "Comment enregistrer une feuille de calcul dans un autre format sur un stockage distant : guide étape par étape"
linktype: "docs"
url: /save-spreadsheet-as/
keywords: "Aspose Cells, conversion de feuille de calcul, enregistrer sous, API, XLSX vers PDF, stockage cloud, Excel vers PDF, export CSV, conversion cloud"
description: "Découvrez comment enregistrer une feuille de calcul stockée dans Aspose Cloud dans un autre format (XLSX, PDF, CSV, etc.) à l’aide de l’API Aspose.Cells Cloud « Save Spreadsheet ». Inclut la syntaxe de requête, les paramètres, un exemple cURL et du code SDK."
weight: 100
---

Enregistrez une feuille de calcul ou un fichier Excel stocké dans le cloud sous un autre format dans le stockage cloud.

## **API d’enregistrement de feuille de calcul**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                                                                                      |
| :---------------- | :----- | :---------- | :----------------------------------------------------------------------------------------------- |
| name              | String | Path        | **Obligatoire.** Le nom du fichier classeur à convertir.                                        |
| format            | String | Query       | **Obligatoire.** Le format de sortie souhaité (par exemple, `Xlsx`, `PDF`, `CSV`).             |
| saveOptionsData   | Class  | Body        | Données optionnelles d’options d’enregistrement. Si omises, la valeur par défaut est `null`.   |
| folder            | String | Query       | Chemin du dossier optionnel où le classeur source est stocké. Si omis, la valeur par défaut est `null`. |
| storageName       | String | Query       | Nom optionnel d’un stockage personnalisé. Si omis, le stockage par défaut est utilisé.          |
| outPath           | String | Query       | Chemin de sortie optionnel pour le fichier converti. Si omis, la valeur par défaut est `null`.  |
| outStorageName    | String | Query       | Nom optionnel du stockage pour le fichier de sortie.                                            |
| fontsLocation     | String | Query       | Emplacement optionnel des polices personnalisées.                                                |
| region            | String | Query       | Paramètre optionnel de région de la feuille de calcul.                                          |
| password          | String | Query       | Mot de passe optionnel pour ouvrir le fichier de feuille de calcul.                             |

**Formats de sortie pris en charge**

| Format | Extension |
| :----- | :-------- |
| Xlsx   | .xlsx     |
| Pdf    | .pdf      |
| Csv    | .csv      |
| Html   | .html     |
| Ods    | .ods      |
| Xls    | .xls      |
| Txt    | .txt      |
| Mhtml  | .mhtml    |
| Tiff   | .tiff     |
| Pptx   | .pptx     |
| … (plus) | Voir la spécification de l’API pour la liste complète (plus de 20 formats) |

### **Réponse**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Exemple de réponse d’erreur (400 Bad Request)**

```json
{
  "Code": 400,
  "Message": "Paramètres de requête invalides."
}
```

**Codes de statut HTTP**

| Code | Signification        | Description                                                      |
| ---- | -------------------- | ---------------------------------------------------------------- |
| 200  | OK                   | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Bad Request          | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Unauthorized         | Jeton JWT invalide ou manquant.                                  |
| 413  | Payload Too Large    | Le fichier téléchargé dépasse la limite de taille.              |
| 500  | Internal Server Error | Erreur serveur inattendue.                                       |

## Où utiliser l’API d’enregistrement de feuille de calcul ?

### Système de gestion de documents d’entreprise

- Enregistrer automatiquement les rapports financiers sous forme d’archives PDF.
- Sauvegarder régulièrement les données commerciales au format CSV.
- Enregistrer les plans de projet sous forme de fichiers en lecture seule pour éviter les modifications accidentelles.

### Intégration de données et processus ETL

- Exporter les données d’un système CRM et les enregistrer dans un modèle Excel standard.
- Convertir les données ERP en CSV pour les importer dans d’autres systèmes.
- Enregistrer les données brutes en JSON pour transmission via API.

### Scénarios de développement et d’automatisation

- Traitement backend pour les applications web.
- Systèmes automatisés de génération de rapports.
- Plateformes de collaboration cloud.
- Intégration dans les processus d’approbation.
- Sauvegarde et migration de données.

## Pourquoi utiliser l’API d’enregistrement de feuille de calcul ?

- **Conviviale pour les développeurs** – Fournit des SDK pour de nombreux langages, accompagnés d’une documentation détaillée, ce qui simplifie l’intégration.
- **Économie de main-d’œuvre** – Gère la conversion côté serveur, réduisant le besoin de code de conversion personnalisé.
- **Tarification à l’usage** – Ne facture que les appels API effectués, sans frais d’installation préalables.
- **Pas de maintenance serveur** – Le service fonctionne dans le cloud, éliminant le besoin de gérer l’infrastructure de conversion.
- **Large support des formats** – Prend en charge la conversion entre plus de 20 formats de feuilles de calcul.
- **Fidélité des données** – Préserve la mise en page, les formules et le style pendant la conversion.

## Comment utiliser l’API d’enregistrement de feuille de calcul avec les SDK ?

### Spécification de l’API d’enregistrement de feuille de calcul

La [Spécification de l’API d’enregistrement de feuille de calcul](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/SaveSpreadsheetAs) définit une interface de programmation publiquement accessible, vous permettant d’effectuer des interactions REST directement depuis un navigateur web.

**Exemple avec corps de requête et cURL**

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/saveas?format=pdf&outPath=output.pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{"SaveOptions":{"SaveFormat":"pdf"}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau et vous permet d’enregistrer une feuille de calcul dans un autre format avec un minimum de code. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{</tab>}}
{{< /tabs >}}