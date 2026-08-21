---
title: "Obtenir le titre d'un graphique à partir d'une feuille de calcul"
type: docs
url: /fr/charts/title/get/
aliases: [/get-chart-title-from-a-worksheet/]
weight: 120
keywords:
  - "Aspose.Cells Cloud"
  - "Titre de graphique"
  - "Excel"
  - "REST API"
  - "Obtenir le titre du graphique"
  - "cURL"
  - "SDK"
  - "Automatisation des graphiques Excel"
  - "GET chart title"
description: "Découvrez comment récupérer le titre d’un graphique à partir d’une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut l’endpoint, les paramètres, l’authentification, ainsi que des exemples de code cURL et SDK."
ArticleTitle: "Obtenir le titre d'un graphique à partir d'une feuille de calcul"
---

Cet API REST permet de récupérer le titre d’un graphique stocké dans une feuille de calcul d’un classeur Excel.

**Prérequis** : Pour appeler cet endpoint, vous devez disposer d’un jeton d’accès OAuth2/JWT valide pour Aspose.Cells Cloud avec la portée `Cells.Read`. Le classeur doit déjà avoir été téléchargé dans l’emplacement de stockage spécifié.

## API GetWorksheetChartTitle

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                           |
| ---------------- | ------- | ----------- | ----------------------------------------------------- |
| name             | string  | path        | Nom du fichier de classeur.                           |
| sheetName        | string  | path        | Nom de la feuille de calcul contenant le graphique.  |
| chartIndex       | integer | path        | Index du graphique (indexation à partir de zéro).     |
| folder           | string  | query       | Chemin du dossier où le classeur est stocké.         |
| storageName      | string  | query       | Nom du service de stockage.                           |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/charts/0/title" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Title": {
    "Text": "Ventes T1",
    "Font": {
      "Name": "Arial",
      "Size": 12,
      "IsBold": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**Champs de la réponse**

| Champ                | Description                                        |
| -------------------- | -------------------------------------------------- |
| `Title.Text`         | Texte réel affiché comme titre du graphique.      |
| `Title.Font.Name`    | Famille de police utilisée pour le titre (ex. _Arial_). |
| `Title.Font.Size`    | Taille de la police en points.                     |
| `Title.Font.IsBold`  | Indique si le texte du titre est en gras.         |

**Codes d’état de la réponse**

| Code | Description |
|------|-------------|
| 200 OK | Le titre du graphique a été récupéré avec succès. |
| 401 Unauthorized | L’authentification a échoué ou le jeton est manquant/ invalide. |
| 404 Not Found | Le classeur, la feuille de calcul ou le graphique spécifié n’existe pas. |
| 500 Internal Server Error | Une erreur serveur inattendue s’est produite. |

**Notes** : L’index du graphique est indexé à partir de zéro ; assurez-vous que le graphique existe bien. Si le classeur n’a pas encore été téléchargé, procédez d’abord à son téléchargement à l’aide de l’API appropriée.

**Comment extraire le titre dans un script (à l’aide de `jq`)**

```bash
# En supposant que la réponse JSON est enregistrée dans response.json
title=$(jq -r '.Title.Text' response.json)
echo "Titre du graphique : $title"
```

## Famille de SDK Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Exemple en C# utilisant le SDK Aspose.Cells Cloud
var config = new Configuration
{
    AccessToken = "<jeton jwt>",
    BasePath = "https://api.aspose.cloud"
};
var api = new ChartsApi(config);
var response = api.GetWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, folder: "", storageName: "");
Console.WriteLine(response.Title.Text);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Exemple en Java utilisant le SDK Aspose.Cells Cloud
Configuration config = new Configuration();
config.setAccessToken("<jeton jwt>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
System.out.println(response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// Exemple en PHP utilisant le SDK Aspose.Cells Cloud
$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jeton jwt>');
$config->setHost('https://api.aspose.cloud');
$apiInstance = new Aspose\Cells\Api\ChartsApi($config);
$response = $apiInstance->getWorksheetChartTitle('Book1.xlsx', 'Sheet1', 0, '', '');
echo $response->getTitle()->getText();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Exemple en Ruby utilisant le SDK Aspose.Cells Cloud
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jeton jwt>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::ChartsApi.new
result = api_instance.get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '')
puts result.title.text
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Exemple en Python utilisant le SDK Aspose.Cells Cloud
from asposecellscloud import ChartsApi, Configuration

config = Configuration()
config.access_token = "<jeton jwt>"
config.host = "https://api.aspose.cloud"

api_instance = ChartsApi(config)
response = api_instance.get_worksheet_chart_title("Book1.xlsx", "Sheet1", 0, "", "")
print(response.title.text)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Exemple en Node.js utilisant le SDK Aspose.Cells Cloud
const { ChartsApi, Configuration } = require('asposecellscloud');

let config = new Configuration();
config.accessToken = "<jeton jwt>";
config.basePath = "https://api.aspose.cloud";

let apiInstance = new ChartsApi(config);
apiInstance.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "", (error, data) => {
    if (error) console.error(error);
    else console.log(data.title.text);
});
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Exemple pour Android (Java) utilisant le SDK Aspose.Cells Cloud
Configuration config = new Configuration();
config.setAccessToken("<jeton jwt>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
Log.d("ChartTitle", response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Exemple en Swift utilisant le SDK Aspose.Cells Cloud
import AsposeCellsCloud

let config = Configuration()
config.accessToken = "<jeton jwt>"
config.host = "https://api.aspose.cloud"

let api = ChartsApi(configuration: config)
api.getWorksheetChartTitle(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, folder: "", storageName: "") { result, error in
    if let title = result?.title?.text {
        print("Titre du graphique : \(title)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Exemple en Perl utilisant le SDK Aspose.Cells Cloud
use AsposeCellsCloud::ChartsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '<jeton jwt>';
$config->{host} = 'https://api.aspose.cloud';

my $api_instance = AsposeCellsCloud::ChartsApi->new($config);
my $result = $api_instance->get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '');
print $result->{title}{text}, "\n";
```

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e1b22ed45ca780faa3231c3a8c60ddd4" >}}

{{< /tab >}}

{{< /tabs >}}

Vous pouvez également consulter la documentation individuelle des SDK pour des scénarios plus avancés, tels que la mise à jour ou la suppression d’un titre de graphique.

**Voir également** : [Mettre à jour le titre du graphique](/fr/charts/title/put/), [Supprimer le titre du graphique](/fr/charts/title/delete/).
---