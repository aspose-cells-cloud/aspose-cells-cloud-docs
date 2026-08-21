---
title: "Aspose.Cells Cloud Docker-Image herunterladen"  
second_title: "Dokument"  
ArticleTitle: "Aspose.Cells Cloud Docker-Image herunterladen"  
linktitle: "Image herunterladen"  
type: docs  
url: /docker/downloads/  
description: "Holen Sie sich die neuesten Aspose.Cells Cloud Docker-Images für Windows Server 2016/2019 und Linux. Folgen Sie den schrittweisen Anleitungen, Voraussetzungen und Sicherheitstipps, um den Container lokal auszuführen."  
weight: 30  
keywords: "Aspose.Cells, Cloud, Docker, Container, Image, herunterladen, Windows Server, Linux, REST-API"  
---  

## Übersicht  

`aspose/cells-cloud` – das offizielle Docker-Image, das die **Aspose.Cells Cloud** REST-API hostet. Das Image ermöglicht es Ihnen, die vollständige Spreadsheet-Verarbeitungs-Engine innerhalb eines Containers auszuführen, sodass Offline- oder Private-Cloud-Deployments ohne Abhängigkeit von Asposes öffentlichen Cloud-Diensten möglich sind.  

**Zuletzt aktualisiert:** 2026‑06‑30  

**Schnellstart-Checkliste**

- Überprüfen Sie, ob Docker Engine-Version 20.10 oder höher installiert ist.  
- Ziehen Sie das passende Image für Ihr Betriebssystem (siehe folgende Abschnitte).  
- Legen Sie die Umgebungsvariablen `ASPOSE_CLIENT_ID` und `ASPOSE_CLIENT_SECRET` fest.  
- Führen Sie den Container mit Port-Mapping von 8080 auf den internen Port 80 aus.  

---  

## Voraussetzungen  

| Anforderung | Details |
|-------------|---------|
| **Docker Engine** | Docker 20.10 oder höher auf dem Host-Betriebssystem installiert. |
| **Betriebssystem** | Windows Server 2016, Windows Server 2019 oder eine moderne Linux-Distribution. |
| **Docker Hub-Zugriff** | Ein aktives Docker Hub-Konto (optional, aber empfohlen für private Images). Führen Sie `docker login` aus, wenn Sie ein Image aus einem privaten Repository ziehen müssen. |
| **Aspose Cloud-Anmeldeinformationen** | `ASPOSE_CLIENT_ID` und `ASPOSE_CLIENT_SECRET` – erhalten Sie diese aus dem Aspose Cloud-Dashboard. |

> **Tipp:** Überprüfen Sie die Docker-Installation mit `docker --version`.  

---  

## Windows Server 2016  

```powershell
docker pull aspose/cells-cloud:ltsc2016.21.9
```

---  

## Windows Server 2019  

```powershell
docker pull aspose/cells-cloud:ltsc2019.21.9
```

---  

## Linux  

```sh
docker pull aspose/cells-cloud:linux.21.9
```

---  

## Container ausführen  

```sh
docker run -d \
  -e ASPOSE_CLIENT_ID=IHRE_CLIENT_ID \
  -e ASPOSE_CLIENT_SECRET=IHRE_CLIENT_GEHEIMNIS \
  -p 8080:80 \
  --name aspose-cells \
  aspose/cells-cloud:ltsc2019.21.9
```

* **Umgebungsvariablen** – `ASPOSE_CLIENT_ID` und `ASPOSE_CLIENT_SECRET` liefern die Anmeldeinformationen, die von der API benötigt werden.  
* **Port-Mapping** – Der Container stellt Port 80 zur Verfügung; ordnen Sie diesen einem Host-Port (z. B. 8080) zu, um auf den Dienst zuzugreifen.  
* **Detached-Modus (`-d`)** – Führt den Container im Hintergrund aus.  

---  

## Versionierung & Aktualisierungen  

| Betriebssystem | Tag | Veröffentlichungsdatum | So erhalten Sie die neueste Version |
|----------------|-----|------------------------|--------------------------------------|
| Windows Server 2016 | `ltsc2016.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:ltsc2016.latest` |
| Windows Server 2019 | `ltsc2019.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:ltsc2019.latest` |
| Linux | `linux.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:linux.latest` |

> **Hinweis:** Der Tag `21.9` ist die aktuelle stabile Version. Verwenden Sie den Tag `latest` oder prüfen Sie die [Aspose.Cells Cloud-Versionshinweise](/cells/release-notes/) für neuere Versionen.  

---  

## Überprüfung & Sicherheit  

* **Prüfung des Image-Digests**  

  ```sh
  docker image inspect aspose/cells-cloud:ltsc2019.21.9 --format='{{.RepoDigests}}'
  ```

* **Schwachstellen-Scan** (empfohlen)  

  ```sh
  trivy image aspose/cells-cloud:ltsc2019.21.9
  ```

* **Best Practices** – Halten Sie Docker auf dem neuesten Stand, führen Sie Container mit den minimalen erforderlichen Rechten aus und scannen Sie Images regelmäßig auf bekannte CVEs.  

* **Strukturierte Daten (JSON-LD)-Beispiel**  

  ```html
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "SoftwareApplication",
    "name": "Aspose.Cells Cloud Docker Image",
    "operatingSystem": "Windows Server 2016/2019, Linux",
    "softwareVersion": "21.9",
    "downloadUrl": "https://hub.docker.com/r/aspose/cells-cloud",
    "offers": {
      "price": "0",
      "priceCurrency": "USD"
    }
  }
  </script>
  ```

---  

## Häufige Probleme & Fehlerbehebung  

| Symptom | Mögliche Ursache | Lösung |
|---------|------------------|--------|
| `docker: command not found` | Docker ist nicht installiert oder der PATH ist nicht gesetzt | Installieren Sie Docker und starten Sie das Terminal neu. |
| Authentifizierungsfehler beim Ziehen | Fehlende oder falsche `docker login`-Anmeldeinformationen | Führen Sie `docker login` mit gültigen Docker Hub-Anmeldeinformationen aus. |
| Container beendet sich sofort | Fehlende erforderliche Umgebungsvariablen | Geben Sie `ASPOSE_CLIENT_ID` und `ASPOSE_CLIENT_SECRET` wie im Abschnitt **Container ausführen** gezeigt an. |
| Portkonflikt auf dem Host | Host-Port ist bereits in Verwendung | Wählen Sie einen anderen Host-Port (z. B. `-p 8081:80`). |

---  

## Siehe auch  

* [Aspose.Cells Cloud API-Dokumentation](/cells/cloud/api/)  
* [Aspose.Cells Cloud-Versionshinweise](/cells/release-notes/) – detailliertes Änderungsprotokoll für Version 21.9 und neuer.  
* [Aspose.Cells Docker-Container-Funktionen](/cells/docker/features/)  
* [Aspose.Cells Docker-Image-Tags](/cells/docker/tag-list/)  

---  

*Vom Aspose Cloud Engineering-Team erstellt.*