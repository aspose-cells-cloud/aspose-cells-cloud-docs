---
title: "SDK Aspose.Cells Cloud disponibles"
second_title: "Document"
ArticleTitle: "SDK Aspose.Cells Cloud disponibles : C#, Java, PHP, Python, Ruby, Node.js, Go, Perl"
LinkTitle: "SDK disponibles"
type: docs
url: /available-sdks/
description: "Découvrez les SDK Aspose.Cells Cloud pour C#, Java, PHP, Python, Ruby, Node.js, Go et Perl. Créez, convertissez et analysez des fichiers Excel dans le cloud à l’aide d’API multiplateformes et à faible coût."
weight: 30
keywords: "SDK Aspose.Cells Cloud, C#, Java, PHP, Python, Ruby, Node.js, Go, Perl, Excel, API cloud"
---

# **Pourquoi utiliser les SDK Aspose.Cells Cloud**

## **Compatibilité multiplateforme**

Les SDK Aspose.Cells Cloud offrent une bibliothèque fiable et stable pour de multiples langages de développement. Ils permettent aux développeurs une prise en charge multiplateforme robuste, facilitant l’intégration sur Windows, Linux ou macOS.

## **Traitement efficace des fichiers Excel et riche ensemble de fonctionnalités**

Les SDK Aspose.Cells Cloud permettent aux développeurs de manipuler efficacement des fichiers Excel dans le cloud, notamment lecture, écriture, modification et conversion, sans avoir à installer de logiciel Office local. L’SDK fournit un large éventail d’API et de fonctions pour prendre en charge des opérations Excel complexes, telles que le calcul de formules, la création de graphiques, le formatage conditionnel, etc., répondant ainsi aux besoins variés des développeurs.

## **Facilité d’intégration**

L’SDK propose une API concise et claire qui permet aux développeurs de l’intégrer rapidement dans leurs projets existants, réduisant ainsi le temps et les coûts de développement.

## **Réduction des coûts**

L’utilisation des SDK Aspose.Cells Cloud permet de réduire les coûts d’exploitation de votre entreprise, en évitant l’achat et la maintenance de logiciels ou serveurs Office locaux coûteux.

### Vue d’ensemble des SDK

<table>
<thead>
<tr>
<th>Langage</th>
<th>Dernière version</th>
<th>Installation</th>
<th>Exemple de démarrage rapide</th>
</tr>
</thead>
<tbody>
<tr>
<td>C#</td>
<td>23.12</td>
<td><code>dotnet add package Aspose.Cells-Cloud</code></td>
<td>
<pre><code class="language-csharp">var api = new CellsApi("clientId", "clientSecret");
var result = api.ConvertSpreadsheet(new ConvertSpreadsheetRequest("sample.xlsx", "pdf"));</code></pre>
</td>
</tr>
<tr>
<td>Java</td>
<td>23.12</td>
<td><code>mvn dependency:copy -Dartifact=aspose:aspose-cells-cloud:23.12</code></td>
<td>
<pre><code class="language-java">CellsApi api = new CellsApi("clientId", "clientSecret");
ConvertSpreadsheetRequest request = new ConvertSpreadsheetRequest();
request.setSpreadsheet("Book1.xlsx");
request.setFormat("pdf");
File result = api.ConvertSpreadsheetRequest(request);</code></pre>
</td>
</tr>
<tr>
<td>PHP</td>
<td>23.12</td>
<td><code>composer require aspose/cells-cloud-sdk</code></td>
<td>
<pre><code class="language-php">$instance = new CellsApi(getenv("CellsCloudClientId"), getenv("CellsCloudClientSecret"));
$convertSpreadsheetRequest = new ConvertSpreadsheetRequest();
$convertSpreadsheetRequest->setSpreadsheet($EmployeeSalesSummaryXlsx);
$convertSpreadsheetRequest->setFormat("pdf");
$instance->convertSpreadsheet($convertSpreadsheetRequest, "export-out1.pdf");</code></pre>
</td>
</tr>
<tr>
<td>Python</td>
<td>23.12</td>
<td><code>pip install aspose-cells-cloud</code></td>
<td>
<pre><code class="language-python">instance = CellsApi(os.getenv('CellsCloudClientId'), os.getenv('CellsCloudClientSecret'))
instance.convert_spreadsheet(ConvertSpreadsheetRequest('EmployeeSalesSummary.xlsx', 'pdf'), local_outpath="EmployeeSalesSummary.pdf")</code></pre>
</td>
</tr>
<tr>
<td>Ruby</td>
<td>23.12</td>
<td><code>gem install aspose_cells_cloud</code></td>
<td>
<pre><code class="language-ruby">@instance = AsposeCellsCloud::CellsApi.new(ENV['CellsCloudClientId'], ENV['CellsCloudClientSecret'])
request = AsposeCellsCloud::ConvertSpreadsheetRequest.new(:Spreadsheet=>'EmployeeSalesSummary.xlsx', :format=>'pdf')
response = @instance.convert_spreadsheet(request)</code></pre>
</td>
</tr>
<tr>
<td>Node.js</td>
<td>23.12</td>
<td><code>npm install asposecellscloud</code></td>
<td>
<pre><code class="language-javascript">const cellsApi = new CellsApi(process.env.CellsCloudClientId, process.env.CellsCloudClientSecret, "v4.0", process.env.CellsCloudApiBaseUrl);
var request = new model.ConvertSpreadsheetRequest();
request.spreadsheet = "Book1.xlsx";
request.format = "pdf";
return cellsApi.convertSpreadsheet(request).then((result) => {
    expect(result.response.statusCode).to.equal(200);
});</code></pre>
</td>
</tr>
<tr>
<td>Go</td>
<td>23.12</td>
<td><code>go get github.com/aspose/cells-cloud-go/v2</code></td>
<td>
<pre><code class="language-go">instance := NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"))
convertedData, httpResponse, err := instance.ConvertSpreadsheet(&amp;ConvertSpreadsheetRequest{Spreadsheet: employeeSalesSummaryXlsx, Format: "pdf"})</code></pre>
</td>
</tr>
</tbody>
</table>

**Prérequis** – .NET 6+ / Java 8+ / PHP 7.4+ / Python 3.7+ / Ruby 2.6+ / Node 12+ / Go 1.16+ / Perl 5.30+. Vous devez également disposer d’un identifiant client et d’un secret client Aspose Cloud valides.

**Exemple de requête et réponse d’API** – conversion d’un classeur Excel en PDF :

```json
{
  "Input": "EmployeeSalesSummary.xlsx",
  "OutputFormat": "pdf"
}
```

Les SDK sont open source et hébergés sur GitHub ; vous pouvez les fork ou y contribuer :

- C# : https://github.com/aspose-cells-cloud/aspose-cells-cloud-csharp  
- Java : https://github.com/aspose-cells-cloud/aspose-cells-cloud-java  
- PHP : https://github.com/aspose-cells-cloud/aspose-cells-cloud-php  
- Python : https://github.com/aspose-cells-cloud/aspose-cells-cloud-python  
- Ruby : https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby  
- Node.js : https://github.com/aspose-cells-cloud/aspose-cells-cloud-node  
- Go : https://github.com/aspose-cells-cloud/aspose-cells-cloud-go  
- Perl : https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl  

En résumé, l’utilisation des SDK Aspose.Cells Cloud apporte de nombreux avantages : compatibilité multiplateforme, gestion efficace des fichiers Excel, riche ensemble de fonctionnalités, protection de la sécurité et de la vie privée, haute extensibilité, facilité d’intégration, support communautaire et documentation, ainsi que réduction des coûts. Ces avantages font de ces SDK un choix idéal pour les développeurs travaillant avec des fichiers Excel.

# **Scénarios d’application**

## **Automatisation du traitement des feuilles de calcul**

- À l’aide des SDK Aspose.Cells Cloud, les développeurs peuvent écrire des scripts d’automatisation pour le traitement par lot de fichiers de feuilles de calcul tels qu’Excel.  
- Les tâches automatisées peuvent inclure l’importation/exportation de données, le formatage, les calculs de formules, la génération de graphiques, etc.

## **Traitement et analyse de données dans le cloud**

- Grâce au service Aspose.Cells dans le cloud, les grandes quantités de données de feuilles de calcul peuvent être traitées sans solliciter les ressources informatiques locales.  
- Cette solution convient aux scénarios nécessitant des analyses complexes, de la fouille de données ou la génération de rapports.

## **Compatibilité multiplateforme**

- Grâce à sa nature multiplateforme, les SDK Aspose.Cells Cloud facilitent la mise en œuvre du traitement de feuilles de calcul sur différents systèmes d’exploitation et architectures.  
- C’est particulièrement adapté aux scénarios nécessitant la prise en charge de plusieurs environnements, tels que les backends d’applications web, les applications de bureau ou les backends d’applications mobiles.

## **Intégration et extensions d’API**

- Les SDK Aspose.Cells Cloud peuvent être intégrés dans des API existantes, fournissant des capacités de traitement de feuilles de calcul comme composant d’un service.  
- Cette solution convient à la construction d’applications d’entreprise, de plateformes SaaS ou à la fourniture de services API.

## **Collaboration et partage de documents**

- À l’aide des SDK Aspose.Cells Cloud, plusieurs utilisateurs peuvent éditer une feuille de calcul en ligne en temps réel.  
- Les utilisateurs peuvent modifier, commenter et partager des fichiers de feuilles de calcul dans le cloud pour améliorer la collaboration d’équipe.

## **Migration et transformation de données**

- Lorsque des données doivent être migrées depuis d’autres formats ou systèmes, les SDK Aspose.Cells Cloud peuvent servir de pont pour la transformation des données.  
- Les données provenant d’autres formats peuvent être converties au format Excel pour une analyse et un traitement ultérieurs.

## **Génération automatique de rapports**

- En exécutant des scripts à intervalles réguliers, des rapports périodiques ou des tableaux de bord peuvent être générés automatiquement à l’aide des SDK Aspose.Cells Cloud.  
- Cette solution est utile pour les organisations devant surveiller régulièrement des indicateurs d’activité, des données de ventes ou des données financières.

## **Intégration dans des processus CI/CD**

- Intégrez les SDK Aspose.Cells Cloud dans vos processus d’intégration et de déploiement continus (CI/CD) pour automatiser la vérification de la conformité des données dans les feuilles de calcul.  
- Cela permet de garantir que les modifications apportées au code ne compromettent pas l’intégrité ni le format des données des feuilles de calcul.

## **Application de feuille de calcul personnalisée**

- À l’aide des SDK Aspose.Cells Cloud, vous pouvez développer des applications de feuilles de calcul sur mesure pour répondre à des besoins métier spécifiques.  
- Par exemple, concevoir des applications de traitement de formulaires personnalisés, des outils de gestion de données financières, etc.

# **Avantages des SDK**

Nos SDK sont 100 % testés et prêts à l’emploi dès l’installation. Ils sont open source et licenciés sous MIT, vous permettant de les utiliser et de les personnaliser entièrement gratuitement.  
---