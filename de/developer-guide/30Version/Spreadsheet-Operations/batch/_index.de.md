---
title: "Stapelverarbeitung von Excel-Dateien: Konvertieren, Sperren, Schützen, Aufteilen und Entsperren"
second_title: "Dokument"
linktitle: "Stapelverarbeitung von Excel-Dateien"
type: docs
url: /batch/
keywords: "Stapelverarbeitung, Excel, Konvertierung, Sperren, Schützen, Aufteilen, Entsperren, Aspose.Cells Cloud API, API-Referenz, Stapeloperationen"
description: "Die Aspose.Cells Cloud API ermöglicht die Stapelverarbeitung mehrerer Excel-Dateien für Konvertierung, Sperren, Schützen, Aufteilen und Entsperren. Enthält detaillierte API-Spezifikationen und SDK-Unterstützung für Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift."
weight: 35
ArticleTitle: "Stapelverarbeitung von Excel-Dateien – Konvertieren, Sperren, Schützen, Aufteilen, Entsperren mit der Aspose.Cells Cloud API"
---

Die Aspose.Cells Cloud API bietet Stapelendpunkte, mit denen Sie häufige Vorgänge für mehrere Excel-Dateien in einer einzigen Anforderung durchführen können. Nachfolgend finden Sie eine schnelle Übersicht der verfügbaren Stapeloperationen sowie eine knappe API-Spezifikation für jede Operation.

- **["Excel-Dateien im Stapel konvertieren"](https://docs.aspose.cloud/cells/batch/convert "Excel-Dateien im Stapel konvertieren")**  
  *Konvertieren Sie mehrere Excel-Dateien in einem einzigen Aufruf in ein gewähltes Ausgabeformat.*  

  **API-Details**  
  ```http
  POST /cells/batch/convert
  Content-Type: multipart/form-data
  Authorization: Bearer {access_token}
  ```  

  **Parameter**  

  | Name          | Typ      | Beschreibung                                   |
  |---------------|----------|------------------------------------------------|
  | files         | Datei[]  | Eine oder mehrere zu konvertierende Excel-Dateien. |
  | outputFormat  | string   | Gewünschtes Ausgabeformat (z. B. pdf, csv, html). |
  | storage       | string   | (Optional) Name des Cloud-Speichers.           |

  **Antworten**  

  | Code | Beschreibung                                  |
  |------|-----------------------------------------------|
  | 200  | Konvertierung erfolgreich; Dateien werden zurückgegeben. |
  | 400  | Ungültige Parameter übergeben.                |
  | 401  | Nicht autorisiert – fehlendes oder ungültiges Token. |
  | 500  | Interner Serverfehler.                        |

- **["Excel-Dateien im Stapel sperren"](https://docs.aspose.cloud/cells/batch/lock "Excel-Dateien im Stapel sperren")**  
  *Wenden Sie gleichzeitig ein Passwortschloss auf mehrere Excel-Dateien an.*  

  **API-Details**  
  ```http
  POST /cells/batch/lock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parameter**  

  | Name     | Typ    | Beschreibung                               |
  |----------|--------|--------------------------------------------|
  | files    | array  | Liste von Dateikennungen oder URLs.        |
  | password | string | Passwort zum Sperren der Arbeitsmappen.    |
  | storage  | string | (Optional) Name des Cloud-Speichers.        |

  **Antworten**  

  | Code | Beschreibung                                 |
  |------|----------------------------------------------|
  | 200  | Dateien erfolgreich gesperrt.                |
  | 400  | Fehlende oder ungültige Parameter.           |
  | 401  | Nicht autorisierter Zugriff.                 |
  | 500  | Serverfehler.                                |

- **["Excel-Dateien im Stapel schützen"](https://docs.aspose.cloud/cells/batch/protect "Excel-Dateien im Stapel schützen")**  
  *Fügen Sie Schutzeinstellungen (z. B. schreibgeschützt, Struktur) für mehrere Arbeitsmappen hinzu.*  

  **API-Details**  
  ```http
  POST /cells/batch/protect
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parameter**  

  | Name          | Typ    | Beschreibung                                         |
  |---------------|--------|------------------------------------------------------|
  | files         | array  | Liste von Dateikennungen oder URLs.                 |
  | protection    | object | Schutzoptionen (z. B. readOnly, structure).         |
  | storage       | string | (Optional) Name des Cloud-Speichers.                 |

  **Antworten**  

  | Code | Beschreibung                                 |
  |------|----------------------------------------------|
  | 200  | Schutz erfolgreich angewendet.               |
  | 400  | Ungültige Anforderungsdaten.                 |
  | 401  | Authentifizierung fehlgeschlagen.            |
  | 500  | Unerwarteter Serverfehler.                   |

- **["Stapelweises Aufteilen"](https://docs.aspose.cloud/cells/batch/split "Stapelweises Aufteilen")**  
  *Teilen Sie große Excel-Arbeitsmappen basierend auf Arbeitsblättern oder Zeilenbereichen in kleinere Dateien auf.*  

  **API-Details**  
  ```http
  POST /cells/batch/split
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parameter**  

  | Name        | Typ    | Beschreibung                                         |
  |-------------|--------|------------------------------------------------------|
  | files       | array  | Aufzuteilende Dateien.                               |
  | splitBy     | string | Kriterium: „worksheet“ (Arbeitsblatt) oder „rowRange“ (Zeilenbereich). |
  | criteria    | object | Details für die gewählte Aufteilungsmethode.        |
  | storage     | string | (Optional) Name des Cloud-Speichers.                 |

  **Antworten**  

  | Code | Beschreibung                                 |
  |------|----------------------------------------------|
  | 200  | Aufteilungsvorgang abgeschlossen; Teile werden zurückgegeben. |
  | 400  | Falsche Aufteilungsparameter.                 |
  | 401  | Nicht autorisierte Anforderung.               |
  | 500  | Verarbeitungsfehler.                          |

- **["Stapelweises Entsperren"](https://docs.aspose.cloud/cells/batch/unlock "Stapelweises Entsperren")**  
  *Entfernen Sie den Passwortschutz für mehrere Excel-Dateien in einem einzigen Aufruf.*  

  **API-Details**  
  ```http
  POST /cells/batch/unlock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parameter**  

  | Name     | Typ    | Beschreibung                                  |
  |----------|--------|-----------------------------------------------|
  | files    | array  | Liste von Kennungen oder URLs gesperrter Dateien. |
  | password | string | Aktuelles Passwort der Dateien.               |
  | storage  | string | (Optional) Name des Cloud-Speichers.          |

  **Antworten**  

  | Code | Beschreibung                                 |
  |------|----------------------------------------------|
  | 200  | Dateien erfolgreich entsperrt.               |
  | 400  | Falsches Passwort oder fehlende Dateien.     |
  | 401  | Nicht autorisierter Zugriff.                 |
  | 500  | Serverseitiger Fehler.                       |
---