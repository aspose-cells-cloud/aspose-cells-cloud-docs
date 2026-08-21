---
title: "Aspose.Cells Cloud Web API – Convertir une feuille de calcul en HTML"
second_title: "Document"
ArticleTitle: "Comment convertir une feuille de calcul en HTML à l’aide de l’API Aspose.Cells Cloud"
linktitle: "Convertir une feuille de calcul en HTML"
type: docs
url: /convert-worksheet-to-html/
description: "Découvrez comment convertir une feuille de calcul Excel en HTML à l’aide de l’API Aspose.Cells Cloud – pas de téléchargement nécessaire, prise en charge des polices personnalisées, des paramètres régionaux et de la gestion des erreurs."
keywords: "Aspose.Cells, Excel vers HTML, conversion de feuille de calcul, API cloud"
weight: 100
---

Le point de terminaison **ConvertWorksheetToHtml** lit un classeur Excel à partir du système de fichiers local, extrait la feuille de calcul spécifiée, puis renvoie le contenu sous forme de fichier HTML. La conversion s’effectue entièrement sur les serveurs cloud d’Aspose, ce qui élimine toute nécessité de téléchargement ou de stockage intermédiaire. Idéal pour générer des vues prêtes au web des données de feuilles de calcul, cette API prend en charge les chemins de sortie optionnels, les polices personnalisées, les paramètres régionaux et les classeurs protégés par mot de passe.

## API de conversion de feuille de calcul en HTML

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la demande

| Nom du paramètre | Type   | Emplacement | Obligatoire/Optionnel | Description                                                                                                                                                                                                |
| :--------------- | :----- | :---------- | :------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | Obligatoire | FormData             | Fichier Excel binaire à traiter. Doit être un fichier valide (.xlsx, .xls, .xlsb, etc.). Exemple : `monClasseur.xlsx`. Le fichier Excel est lu directement à partir du corps de la demande ; aucun téléchargement préalable vers un stockage cloud n’est nécessaire. |
| worksheet        | Chaîne  | Obligatoire | Query                | Nom de la feuille de calcul à convertir (sensible à la casse). Doit exister dans le classeur fourni. Exemple : `Feuil1`.                                                                                   |
| outPath          | Chaîne  | Optionnel   | Query                | Chemin du dossier cible (dans le stockage cloud) où le fichier HTML généré sera enregistré. Si omis, le fichier est renvoyé directement dans la réponse. Exemple : `/output/html/`.                         |
| outStorageName   | Chaîne  | Optionnel   | Query                | Nom du service de stockage cloud à utiliser pour `outPath`. Nécessaire uniquement si `outPath` pointe vers un stockage non par défaut.                                                                      |
| fontsLocation    | Chaîne  | Optionnel   | Query                | Chemin absolu vers un dossier contenant des polices TrueType/OpenType personnalisées à utiliser lors de la conversion. Permet un rendu correct des caractères non standard.                                 |
| region           | Chaîne  | Optionnel   | Query                | Identifiant de paramètres régionaux influençant le formatage des nombres et des dates (par exemple, `fr-FR`, `en-US`). Par défaut, utilise le paramètre régional interne du classeur.                        |
| password         | Chaîne  | Optionnel   | Query                | Mot de passe requis pour ouvrir un classeur protégé. À omettre pour les fichiers non protégés.                                                                                                             |

### Réponse

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

**Codes d’état HTTP**

| Code | Signification          | Description                                                    |
| ---- | ---------------------- | -------------------------------------------------------------- |
| 200  | OK                     | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Demande incorrecte     | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé           | Jeton JWT invalide ou manquant.                                |
| 413  | Charge utile trop grande | Le fichier téléchargé dépasse la limite de taille.            |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur.                                  |

## Où utiliser l’API Convert Worksheet to HTML ?

- Intégrer des données de feuille de calcul en direct dans un portail web – Convertir une feuille de calcul de rapport financier en HTML pour une visualisation directe dans les navigateurs sans nécessiter de plugins Excel.
- Générer des factures HTML imprimables à partir d’un modèle Excel – Automatiser la création de pages de facture prêtes au web à partir d’une feuille de calcul prédéfinie.
- Créer des extraits de documentation – Convertir des feuilles de spécifications de conception en fragments HTML pouvant être insérés dans des manuels techniques ou des wikis.
- Développer des tableaux de bord BI à faible code – Extraire les données de la feuille de calcul, les convertir en HTML, puis les afficher dans des widgets de tableau de bord personnalisés.

## Pourquoi utiliser l’API Convert Worksheet to HTML ?

- **Workflow sans téléchargement** – Convertir des fichiers locaux directement dans le cloud, éliminant la nécessité de transférer d’abord de grands classeurs vers un stockage.
- **Rendu haute performance** – La conversion côté serveur exploite le moteur optimisé d’Aspose, garantissant une sortie HTML rapide et précise.
- **Contrôle total sur la sortie** – Les paramètres optionnels (polices personnalisées, régions, mots de passe) permettent d’adapter le HTML aux exigences locales et de marque.
- **Intégration transparente** – Une simple requête PUT avec multipart/form-data s’intègre naturellement dans les pipelines CI/CD, les microservices ou les fonctions sans serveur.

## Comment utiliser l’API Convert Worksheet to HTML à l’aide des SDK

### Spécification de l’API Convert Worksheet to HTML

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtml" target="_blank" rel="noopener noreferrer">Spécification de l’API Convert Worksheet to HTML</a> fournit une interface de programmation publiquement accessible pour exécuter directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Demande" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html?worksheet=Feuil1" \
  -H "Authorization: Bearer {jeton_d'accès}" \
  -F "Spreadsheet=@monClasseur.xlsx" \
  -o converted.html
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

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer, car elle abstraît les détails de bas niveau, vous permettant de fusionner des feuilles de calcul à l’aide d’un code concis.  
Veuillez consulter le <a href="https://github.com/aspose-cells-cloud/aspnet-sdk" target="_blank" rel="noopener noreferrer">dépôt GitHub des SDK Aspose.Cells Cloud</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.  
Les exemples de code suivants illustrent comment interagir avec les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}

---