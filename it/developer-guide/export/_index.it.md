---
title: Esporta la cartella di lavoro e gli oggetti interni in tipi di forma
second_title: Aspose.Cells Cloud Documen
linktitle: Esporta
type: docs
url: /it/export/
keywords: Export workbook and internal objects to kinds of format files
description: Aspose.Cells Cloud REST API supporta l'esportazione di file Excel e oggetti interni in tipi di file di formato. L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 31
---
 Se hai originariamente creato un file Excel in un certo formato, come[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) , E[CSV](https://docs.fileformat.com/spreadsheet/csv/) , a volte potresti trovare utile convertire il file excel in un altro formato in modo da poter sfruttare le funzionalità speciali fornite da esso. Ad esempio, potresti voler esportare un file excel in[PDF](https://docs.fileformat.com/pdf/) per proteggere i tuoi contenuti da eventuali modifiche non autorizzate e facilitarne la lettura e la condivisione simultanea.

 Excel l'esportazione di oggetti è un processo complesso. Molti fattori contribuiscono alla complessità e, pertanto, dovrebbero essere presi in considerazione durante il processo di esportazione. La possibilità di esportare l'oggetto Excel in un file di formato con una precisa qualità professionale è una delle caratteristiche principali di Aspose.Cells Cloud.

 Funziona perfettamente per cartelle di lavoro, grafici, forme e immagini esportate da file excel. Puoi esportare formati:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/) . I formati di sola esportazione:[PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMERI](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

La richiesta è una richiesta HTTP con contenuto in più parti (vedi[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)O[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La prima parte del contenuto multiparte contiene il file di dati e la seconda contiene le opzioni di salvataggio.

La cartella di lavoro REST API `export` e gli oggetti interni in file di formato diverso.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

 I parametri della richiesta sono:
 
| Nome parametro| Tipo| Percorso/Stringa di query/HTTPBody|Descrizione|
|:- |:- |:- |:- |
| file| file| formData| File da caricare|
| tipo di oggetto| corda| domanda|tipo di oggetto (cartella di lavoro/foglio di lavoro/grafico/forma/immagine/listobject/oleobject)|
| formato| corda| domanda|[Formato del file](/cells/it/supported-file-formats/)  |
 
 IL[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/LiteCells/PostExport) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/export" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
    "Files":
    [
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Famiglia di SDK cloud


 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:


{{< tabs tabTotal="9" tabID="3" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" tabName10="C#" tabName11="Java" >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Export.cs" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Export.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LiteCells-Export.php" >}}


{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LiteCellsExport.py" >}}
{{< /tab >}}

{{< /tabs >}}


I seguenti articoli spiegano ogni API in dettaglio e contengono cURL ed esempi SDK di ogni API:


1. [Esporta il grafico Excel in un formato di file diverso](/cells/it/export/excel-chart-to-different-formats/)
2. [Esporta l'oggetto elenco Excel in un formato di file diverso](/cells/it/export/excel-listobject-to-different-formats/)
3. [Esporta Excel ole-object in un formato di file diverso](/cells/it/export/excel-ole-object/)
4. [Esporta l'immagine Excel in un formato di file diverso](/cells/it/export/excel-picture-to-different-formats/)
5. [Esporta la forma Excel in un formato di file diverso](/cells/it/export/excel-shape-to-different-formats/)
6. [Esporta la cartella di lavoro Excel in un formato di file diverso](/cells/it/export/excel-to-different-formats/)
7. [Esporta il foglio di lavoro Excel in un formato di file diverso](/cells/it/export/excel-worksheet-to-different-formats//)
