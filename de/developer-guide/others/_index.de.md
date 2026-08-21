---
title: "Aspise.Cells Cloud Web API – Weitere Funktionen: Gesundheitsprüfung, Öffentlichen Schlüssel abrufen"
linktitle: "Weitere Funktionen"
ArticleTitle: "Weitere Funktionen: Gesundheitsprüfung, Öffentlichen Schlüssel abrufen"
second_title: "Dokument"
type: docs
url: /de/other-features/
keywords: "Aspose.Cells, Cloud API, Gesundheitsprüfung, öffentlicher Schlüssel, Zugriffstoken, Excel, REST"
description: "Entdecken Sie die weiteren Funktionen von Aspose.Cells Cloud: den Gesundheitsprüfungsendpunkt, die Abfrage des öffentlichen Schlüssels und die Erstellung von Zugriffstoken zur Sicherung Ihrer Excel-API-Integrationen."
weight: 180
---

**Voraussetzungen** – Um die unten aufgeführten Funktionen nutzen zu können, benötigen Sie ein gültiges Aspose Cloud-Abonnement sowie ein aktuelles **Client-ID** / **Client-Secret**-Paar zur Authentifizierung.

Diese „Weiteren Funktionen“ bieten wesentliche Support-Operationen für die Aspose.Cells Cloud API, wie etwa die Überprüfung der Serviceverfügbarkeit, die Abfrage kryptographischer Schlüssel und die Erstellung von Zugriffstoken. Sie werden üblicherweise vor der Arbeit mit arbeitsmappenbezogenen Endpunkten aufgerufen.

- **[Aspose.Cells Cloud Gesundheitsprüfung](https://docs.aspose.cloud/cells/check-cloud-service-health/)**  
  Überprüfen Sie, ob der Aspose.Cells Cloud-Service erreichbar und ordnungsgemäß funktionsfähig ist. Ein erfolgreicher Aufruf gibt **HTTP 200** mit JSON `{ "status": "OK" }` zurück. Rufen Sie diesen Endpunkt zu Beginn Ihres Arbeitsablaufs auf, um unnötige Fehler zu vermeiden.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/check-cloud-service-health/">Weitere Informationen</a>

- **[Aspose.Cells Cloud Ausführungsstatus abrufen](https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/)**  
  Ermitteln Sie den aktuellen Ausführungsstatus des Services. Die Antwort gibt an, ob die API vollständig betriebsbereit ist, sich im Wartungsmodus befindet oder aktuelle Probleme aufweist.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/">Weitere Informationen</a>

- **[Öffentlichen Schlüssel abrufen](https://docs.aspose.cloud/cells/get-public-key/)**  
  Rufen Sie den RSA-öffentlichen Schlüssel (PEM-Format) ab, der zur Verifizierung von JWT-Token verwendet wird, die von Aspose.Cells Cloud ausgestellt wurden. Dieser Schlüssel ist erforderlich, wenn Sie Token auf der Serverseite validieren.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-public-key/">Weitere Informationen</a>

- **[Zugriffstoken mit Client-ID und Client-Secret abrufen](https://docs.aspose.cloud/cells/post-access-token/)**  
  Generieren Sie ein OAuth 2.0-Zugriffstoken mithilfe des Grant-Typ-Verfahrens **client_credentials**. Geben Sie Ihre **Client-ID** und **Client-Secret** im Anforderungstext an; die Antwort enthält `access_token`, `token_type` und `expires_in`. Dieses Token muss in allen folgenden API-Aufrufen im `Authorization`-Header übermittelt werden.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/post-access-token/">Weitere Informationen</a>

---