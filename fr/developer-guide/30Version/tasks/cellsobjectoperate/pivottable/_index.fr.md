---
title: "Travail avec les tableaux croisés dynamiques à l’aide de la tâche CellsObjectOperate"
type: docs
url: /fr/tasks/cells-object-operate/pivottable/
aliases: [/fr/working-with-pivot-table-using-cellsobjectoperate-task/]
keywords: "API tableau croisé dynamique Aspose Cells, CellsObjectOperate, API REST Excel"
description: "Découvrez comment générer un tableau croisé dynamique dans Excel à l’aide de la tâche CellsObjectOperate d’Aspose.Cells Cloud. Inclut un exemple cURL, un guide des paramètres et des références aux SDK."
weight: 10
---

Cette API REST **crée** un tableau croisé dynamique à l’aide de la tâche **CellsObjectOperate**.

**PivotTableOperateParameter**

| Nom du paramètre    | Type          | Description                                                                 |
|---------------------|---------------|-----------------------------------------------------------------------------|
| DestCellName        | string        | Cellule en haut à gauche du tableau croisé dynamique (ex. `C1`).            |
| SourceData          | string        | Plage contenant les données sources (ex. `Sheet2!A1:E8`).                  |
| TableName           | string        | Nom attribué au nouveau tableau croisé dynamique.                          |
| UseSameSource       | string        | `true` / `false` – indique si le tableau croisé utilise le classeur source identique. |
| PivotTableIndex     | integer       | Index du tableau croisé dynamique lorsqu’il y a plusieurs tableaux dans la feuille de calcul. |
| PivotFieldRows      | integer[]     | Indexes de champs (à partir de zéro) à placer dans la zone des lignes.      |
| PivotFieldColumns   | integer[]     | Indexes de champs (à partir de zéro) à placer dans la zone des colonnes.    |
| PivotFieldData      | integer[]     | Indexes de champs (à partir de zéro) à agréger comme données.               |

## API REST

| **API**               | **Type** | **Description** | **Lien vers la ressource** |
|-----------------------|----------|-----------------|----------------------------|
| /cells/task/runtask   | POST     | Exécuter une tâche | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Conditions préalables
Avant d’invoquer l’API, vous devez :

1. Créer un compte Aspose.Cloud et une application afin d’obtenir un **client ID** et un **client secret**.  
2. Demander un **jeton JWT** à partir du point de terminaison `/connect/token` à l’aide des identifiants du client.  
3. Inclure le jeton dans l’en-tête `Authorization: Bearer <jeton JWT>` de chaque requête.  

Vous pouvez dès lors utiliser l’outil en ligne de commande **cURL** pour accéder aux services web Aspose.Cells.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
# Exemple cURL – importation des données (étape 1)
curl -v "https://api.aspose.cloud/v3.0/cells/task/runtask" \
  -X POST \
  -H "accept: application/xml" \
  -H "Content-Type: application/xml" \
  -H "Authorization: Bearer <jeton JWT>" \
  -d '
<TaskData>
  <Tasks>
    <TaskDescription>
      <TaskType>ImportData</TaskType>
      <ImportDataTaskParameter>
        <Workbook>
          <FileSourceType>CloudFileSystem</FileSourceType>
          <FilePath>Book1.xlsx</FilePath>
        </Workbook>
        <ImportBatchDataOption>
          <DestinationWorksheet>Sheet2</DestinationWorksheet>
          <IsInsert>true</IsInsert>
          <BatchData>
            <!-- Lignes d’exemple – seules quelques-unes sont affichées pour concision -->
            <CellValue><rowIndex>0</rowIndex><columnIndex>0</columnIndex><type>String</type><value>Sport</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>1</columnIndex><type>String</type><value>Année</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>2</columnIndex><type>String</type><value>Trimestre</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>3</columnIndex><type>String</type><value>Ventes</value></CellValue>
            <!-- …lignes supplémentaires omises pour clarté… -->
          </BatchData>
        </ImportBatchDataOption>
      </ImportDataTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>CellsObjectOperate</TaskType>
      <CellsObjectOperateTaskParameter>
        <OperateObject>
          <OperateObjectType>ListObject</OperateObjectType>
          <Position>
            <Workbook>
              <FileSourceType>InMemoryFiles</FileSourceType>
              <FilePath>Book1.xlsx</FilePath>
            </Workbook>
            <SheetName>Sheet1</SheetName>
            <ListObjectIndex>0</ListObjectIndex>
          </Position>
        </OperateObject>

        <PivotTableOperateParameter>
          <OperateType>Add</OperateType>
          <SourceData>=Sheet2!A1:E8</SourceData>
          <DestCellName>C1</DestCellName>
          <TableName>TestPivot</TableName>
          <UseSameSource>true</UseSameSource>
          <PivotTableIndex>0</PivotTableIndex>
          <PivotFieldRows><int>0</int><int>1</int></PivotFieldRows>
          <PivotFieldColumns><int>2</int></PivotFieldColumns>
          <PivotFieldData><int>3</int><int>4</int></PivotFieldData>
        </PivotTableOperateParameter>

        <DestinationWorkbook>
          <FileSourceType>InMemoryFiles</FileSourceType>
          <FilePath>Book001.xlsx</FilePath>
        </DestinationWorkbook>
      </CellsObjectOperateTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>SaveResult</TaskType>
      <SaveResultTaskParameter>
        <ResultSource>InMemoryFiles</ResultSource>
        <ResultDestination>
          <DestinationType>OutputStream</DestinationType>
          <InputFile>Book001.xlsx</InputFile>
          <OutputFile>Output/ReportS004.xlsx</OutputFile>
        </ResultDestination>
      </SaveResultTaskParameter>
    </TaskDescription>
  </Tasks>
</TaskData>'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
Codes de statut HTTP possibles :
- **200 OK** – Tableau croisé dynamique créé avec succès. Le corps de la réponse contient un `TaskId` permettant de consulter l’état de l’opération.
- **400 Bad Request** – Charge utile XML non valide ou paramètres requis manquants.
- **401 Unauthorized** – Jeton JWT manquant ou invalide.
- **500 Internal Server Error** – Erreur inattendue côté serveur.

Exemple de réponse réussie (XML) :

<?xml version="1.0" encoding="UTF-8"?>
<TaskResponse>
  <TaskId>12345</TaskId>
  <Status>Completed</Status>
  <Result>
    <ResultSource>InMemoryFiles</ResultSource>
    <ResultDestination>Output/ReportS004.xlsx</ResultDestination>
  </Result>
</TaskResponse>
```

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

L’utilisation d’un SDK constitue la méthode optimale pour accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur vos tâches de projet. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK d’Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :
---