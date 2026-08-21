---
title: Convertir Excel en HTML  
description: Convertir un classeur Excel en fichier HTML à l'aide de l'API Aspose.Cells Cloud v3.0.  
api_version: v3.0  
base_url: https://api.aspose.cloud/v3.0  
---

# Convertir Excel en HTML  

Aspose.Cells Cloud fournit un endpoint REST robuste permettant de convertir un classeur Excel (XLS, XLSX, CSV, etc.) en document HTML. L'opération renvoie un objet **FileInfo** contenant le fichier HTML généré (nom, taille et contenu codé en Base64).

---

## Conditions préalables

| Exigence | Comment satisfaire |
|----------|--------------------|
| **Compte Aspose Cloud** | S'inscrire sur [aspose.cloud](https://www.aspose.cloud). |
| **Jeton d’accès JWT** | Obtenir un jeton bearer via l’endpoint OAuth 2.0 `POST /connect/token`. |
| **Stockage (facultatif)** | Si vous souhaitez que l’API lise/écrive des fichiers depuis un stockage spécifique, créez-le d’abord (par exemple Amazon S3, Azure Blob ou le stockage Aspose Cloud). |
| **cURL / SDK** | Tout client HTTP capable de gérer multipart/form-data (cURL, Postman, ou l’un des SDK Aspose.Cells). |

---

## Authentification

Toutes les requêtes à Aspose.Cells Cloud nécessitent une **authentification basée sur un jeton JWT**.

```http
Authorization: Bearer <jeton-daccès>
```

Le jeton doit être inclus dans l’en-tête `Authorization` de chaque requête.

---

## Endpoint

```
POST https://api.aspose.cloud/v3.0/cells/convert/html
```

> **Remarque** – La requête doit être envoyée en tant que `multipart/form-data`. Le fichier Excel constitue la première partie du corps multipart.

---

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

## Paramètres de la requête  

### Paramètres de requête (Query Parameters)  

| Nom                      | Type    | Obligatoire | Valeur par défaut | Description |
|--------------------------|---------|-------------|-------------------|-------------|
| `password`               | string  | Non         | –                 | Mot de passe pour ouvrir un classeur protégé. |
| `storageName`            | string  | Non         | –                 | Nom du stockage où réside le fichier source. |
| `checkExcelRestriction` | boolean | Non         | `true`            | Si `true`, le service valide les restrictions spécifiques à Excel (par exemple, les feuilles protégées). |
| `region`                 | string  | Non         | –                 | Paramètres régionaux du classeur (par exemple, `fr-FR`). |
| `FontsLocation`          | string  | Non         | –                 | URL ou chemin vers un dossier contenant les polices personnalisées nécessaires au rendu. |

### Données de formulaire (multipart)  

| Nom  | Type | Obligatoire | Description |
|------|------|-------------|-------------|
| **File** | fichier | **Oui** | Le classeur Excel à convertir. Doit être fourni en tant que première partie de la requête multipart. |

---

## Exemple de requête (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/html?checkExcelRestriction=true" \
     -H "accept: multipart/form-data" \
     -H "Authorization: Bearer <jeton-daccès>" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/chemin/vers/votre_classeur.xlsx"
```

---

## Réponse réussie  

**Code d’état :** `200 OK`

| Champ          | Type   | Description |
|----------------|--------|-------------|
| `Filename`     | string | Nom du fichier HTML généré (par exemple, `exemple.html`). |
| `FileSize`     | int    | Taille du fichier HTML en octets. |
| `FileContent`  | string | Contenu HTML codé en Base64. |

```json
{
  "Filename": "exemple.html",
  "FileSize": 12345,
  "FileContent": "chaine_base64_codée"
}
```

Le schéma de réponse est défini par le modèle **FileInfo** : [/cells/file-info](/cells/file-info/).

---

## Réponses d’erreur  

| Code | Signification                      | Exemple de charge utile |
|------|------------------------------------|--------------------------|
| `400` | Requête incorrecte – paramètres manquants ou invalides | ```json { "Code": "BadRequest", "Message": "La partie 'File' est obligatoire." } ``` |
| `401` | Non autorisé – jeton JWT invalide ou manquant | ```json { "Code": "InvalidToken", "Message": "Le jeton d’accès est manquant ou expiré." } ``` |
| `404` | Non trouvé – fichier source introuvable dans le stockage spécifié | ```json { "Code": "FileNotFound", "Message": "Le fichier 'mon.xlsx' n’existe pas dans le stockage 'MonStockage'." } ``` |
| `413` | Charge utile trop volumineuse – fichier téléchargé dépassant la taille autorisée | ```json { "Code": "RequestEntityTooLarge", "Message": "Le fichier téléchargé dépasse la limite de 100 Mo." } ``` |
| `429` | Trop de requêtes – limite de débit dépassée | ```json { "Code": "TooManyRequests", "Message": "La limite de débit de 60 appels par minute est dépassée." } ``` |
| `500` | Erreur interne du serveur – condition inattendue sur le serveur | ```json { "Code": "InternalError", "Message": "Une erreur inattendue s’est produite. Veuillez réessayer plus tard." } ``` |

---

## Limites de débit  

| Limite | Description |
|--------|-------------|
| **60 requêtes par minute** par compte (par défaut) | Dépasser cette limite renvoie `429 Trop de requêtes`. Ajustez la logique de votre client ou demandez un quota supérieur via le portail Aspose Cloud. |

---

## Prise en charge par les SDK  

Aspose propose des SDK de première classe qui encapsulent cet endpoint pour plusieurs langages. Les exemples ci-dessous illustrent la même conversion à l’aide des SDK officiels.

| Langage | Exemple |
|---------|---------|
| C#      | <details><summary>Voir l’exemple</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new ConversionApi();\nvar file = File.ReadAllBytes("votre.xlsx");\nvar result = apiInstance.PostConvertWorkbookToHtml(file, password: null, checkExcelRestriction: true);\nConsole.WriteLine(result.Filename);\n```</details> |
| Java    | <details><summary>Voir l’exemple</summary>```java\nConversionApi api = new ConversionApi();\nFile file = new File("votre.xlsx");\nFileInfo info = api.postConvertWorkbookToHtml(file, null, true);\nSystem.out.println(info.getFilename());\n```</details> |
| Python  | <details><summary>Voir l’exemple</summary>```python\nfrom asposecellscloud import ConversionApi\napi = ConversionApi()\nwith open('votre.xlsx', 'rb') as f:\n    file_info = api.post_convert_workbook_to_html(file=f.read())\nprint(file_info.filename)\n```</details> |
| Node.js | <details><summary>Voir l’exemple</summary>```javascript\nconst { ConversionApi } = require('asposecellscloud');\nconst api = new ConversionApi();\nconst fs = require('fs');\napi.postConvertWorkbookToHtml({ File: fs.createReadStream('votre.xlsx') })\n   .then(info => console.log(info.Filename));\n```</details> |
| Go      | <details><summary>Voir l’exemple</summary>```go\nimport (\n    "asposecellscloud"\n    "os"\n)\nfunc main() {\n    api := asposecellscloud.NewConversionApi()\n    f, _ := os.Open("votre.xlsx")\n    info, _ := api.PostConvertWorkbookToHtml(f, nil, true)\n    fmt.Println(info.Filename)\n}\n```</details> |
| PHP     | <details><summary>Voir l’exemple</summary>```php\nuse Aspose\Cells\ConversionApi;\n$api = new ConversionApi();\n$file = fopen('votre.xlsx', 'r');\n$info = $api->postConvertWorkbookToHtml($file);\necho $info->getFilename();\n```</details> |
| Ruby    | <details><summary>Voir l’exemple</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::ConversionApi.new\nfile = File.open('votre.xlsx')\ninfo = api.post_convert_workbook_to_html(file: file)\nputs info.filename\n```</details> |
| Perl    | <details><summary>Voir l’exemple</summary>```perl\nuse Aspose::Cells::ConversionApi;\nmy $api = Aspose::Cells::ConversionApi->new();\nopen my $fh, '<', 'votre.xlsx' or die $!;\nmy $info = $api->post_convert_workbook_to_html(file => $fh);\nprint $info->{Filename};\n```</details> |

Pour la liste complète des SDK pris en charge et les instructions d’installation, consultez le dépôt **Aspose.Cells Cloud SDKs** : <https://github.com/aspose-cells-cloud>.

---

## Endpoints connexes  

| Endpoint | Description |
|----------|-------------|
| `POST /cells/{name}/saveAs` | Enregistrer un fichier Excel existant en tant que HTML (ou autres formats) directement dans le stockage. |
| `PUT /cells/convert` | Convertir un classeur en HTML avec des options de conversion supplémentaires ; le résultat est renvoyé dans le corps de la réponse. |
| `GET /cells/{name}` | Récupérer un classeur déjà stocké en tant que HTML (ou autres formats) avec des paramètres de requête optionnels. |

---

## Questions fréquentes  

**Q :** *Comment m’authentifier lors de l’appel de l’API de conversion Excel vers HTML ?*  
**A :** Inclure l’en-tête `Authorization: Bearer <jeton-daccès>` obtenu via l’endpoint OAuth 2.0 `/connect/token`.

**Q :** *Que contient la réponse `FileInfo` ?*  
**A :** Trois champs : `Filename` (chaîne), `FileSize` (entier, octets) et `FileContent` (contenu HTML codé en Base64).

**Q :** *Quels codes d’erreur puis-je rencontrer ?*  
**A :** `400` (Requête incorrecte), `401` (Non autorisé), `404` (Fichier non trouvé), `413` (Charge utile trop volumineuse), `429` (Trop de requêtes), `500` (Erreur interne du serveur). Chacun renvoie une charge utile JSON avec `Code` et `Message`.

**Q :** *Puis-je spécifier un emplacement personnalisé pour les polices ?*  
**A :** Oui. Utiliser le paramètre de requête `FontsLocation` pour pointer vers un dossier ou une URL contenant les polices requises.

**Q :** *Y a-t-il une limite de débit pour cette opération ?*  
**A :** La limite par défaut est de **60 appels par minute** par compte. Le dépassement de cette limite renvoie `429 Trop de requêtes`.

---

## Breadcrumb JSON-LD (données structurées)

Ajouter ce bloc améliore le SEO en permettant l’affichage de filles d’Ariane en tant que snippets enrichis dans les résultats de recherche.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Accueil", "item": "https://docs.aspose.cloud/" },
    { "@type": "ListItem", "position": 2, "name": "Centre développeur", "item": "https://docs.aspose.cloud/cells/" },
    { "@type": "ListItem", "position": 3, "name": "Conversion", "item": "https://docs.aspose.cloud/cells/conversion/" },
    { "@type": "ListItem", "position": 4, "name": "Excel vers HTML", "item": "https://docs.aspose.cloud/cells/convert-excel-file-to-html-file/" }
  ]
}
</script>
```

---

## Journal des modifications  

| Version | Date | Modifications |
|---------|------|---------------|
| **v3.0** | 2024‑10‑01 | Version initiale publique de `PostConvertWorkbookToHtml`. |
| **v3.1** | 2025‑04‑15 | Ajout des paramètres de requête `region` et `FontsLocation` ; mise à jour du format de charge utile des erreurs. |
| **v3.2** | 2026‑03‑20 | Documentation relative aux limites de débit et exemples de réponses d’erreur. |

---

*Pour toute assistance complémentaire, veuillez contacter le support Aspose ou consulter la documentation officielle de l’API :* <https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToHtml>  
---