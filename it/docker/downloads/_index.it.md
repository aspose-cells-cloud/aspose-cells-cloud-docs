---
title: "Download dell'immagine Docker di Aspose.Cells Cloud"  
second_title: "Documento"  
ArticleTitle: "Download dell'immagine Docker di Aspose.Cells Cloud"  
linktitle: "Download immagine"  
type: docs  
url: /docker/downloads/  
description: "Scarica le ultime immagini Docker di Aspose.Cells Cloud per Windows Server 2016/2019 e Linux. Segui le istruzioni passo-passo, i prerequisiti e i consigli di sicurezza per eseguire il container in locale."  
weight: 30  
keywords: "Aspose.Cells, Cloud, Docker, container, immagine, download, Windows Server, Linux, REST API"  
---  

## Panoramica  

`aspose/cells-cloud` – l’immagine Docker ufficiale che ospita l’API REST **Aspose.Cells Cloud**. L’immagine consente di eseguire l’intero motore di elaborazione di fogli di calcolo all’interno di un container, abilitando distribuzioni offline o in cloud privato senza dipendere dai servizi cloud pubblici di Aspose.  

**Ultimo aggiornamento:** 2026‑06‑30  

**Elenco di controllo per l’avvio rapido**

- Verifica che la versione di Docker Engine sia 20.10 o successiva.  
- Esegui il pull dell’immagine appropriata per il tuo sistema operativo (vedi le sezioni riportate di seguito).  
- Imposta le variabili di ambiente `ASPOSE_CLIENT_ID` e `ASPOSE_CLIENT_SECRET`.  
- Esegui il container mappando la porta 8080 alla porta interna 80.  

---  

## Prerequisiti  

| Requisito | Dettagli |
|-----------|----------|
| **Docker Engine** | Docker 20.10 o versione successiva installata sul sistema operativo host. |
| **Sistema operativo** | Windows Server 2016, Windows Server 2019 o qualsiasi distribuzione Linux moderna. |
| **Accesso a Docker Hub** | Un account Docker Hub attivo (opzionale ma consigliato per le immagini private). Esegui `docker login` se devi effettuare il pull da un repository privato. |
| **Credenziali Aspose Cloud** | `ASPOSE_CLIENT_ID` e `ASPOSE_CLIENT_SECRET` – ottienile dalla dashboard Aspose Cloud. |

> **Suggerimento:** Verifica l’installazione di Docker con `docker --version`.  

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

## Esecuzione del container  

```sh
docker run -d \
  -e ASPOSE_CLIENT_ID=YOUR_CLIENT_ID \
  -e ASPOSE_CLIENT_SECRET=YOUR_CLIENT_SECRET \
  -p 8080:80 \
  --name aspose-cells \
  aspose/cells-cloud:ltsc2019.21.9
```

* **Variabili di ambiente** – `ASPOSE_CLIENT_ID` e `ASPOSE_CLIENT_SECRET` forniscono le credenziali richieste dall’API.  
* **Mappatura porte** – Il container espone la porta 80; mappala a una porta host (ad esempio 8080) per accedere al servizio.  
* **Modalità detach (`-d`)** – Esegue il container in background.  

---  

## Versioni e aggiornamenti  

| Sistema operativo | Tag | Data di rilascio | Come ottenere la versione più recente |
|-------------------|-----|------------------|----------------------------------------|
| Windows Server 2016 | `ltsc2016.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:ltsc2016.latest` |
| Windows Server 2019 | `ltsc2019.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:ltsc2019.latest` |
| Linux | `linux.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:linux.latest` |

> **Nota:** Il tag `21.9` rappresenta la versione stabile attuale. Utilizza il tag `latest` o consulta le [note di rilascio di Aspose.Cells Cloud](/cells/release-notes/) per versioni più recenti.  

---  

## Verifica e sicurezza  

* **Controllo del digest dell’immagine**  

  ```sh
  docker image inspect aspose/cells-cloud:ltsc2019.21.9 --format='{{.RepoDigests}}'
  ```

* **Scansione vulnerabilità** (consigliata)  

  ```sh
  trivy image aspose/cells-cloud:ltsc2019.21.9
  ```

* **Best practice** – Mantieni Docker aggiornato, esegui i container con i minimi privilegi necessari e scansione regolarmente le immagini per CVE noti.  

* **Esempio di dati strutturati (JSON‑LD)**  

  ```html
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "SoftwareApplication",
    "name": "Immagine Docker di Aspose.Cells Cloud",
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

## Problemi comuni e risoluzione  

| Sintomo | Causa probabile | Soluzione |
|---------|-----------------|-----------|
| `docker: command not found` | Docker non installato o PATH non impostato | Installa Docker e riavvia il terminale. |
| Errore di autenticazione durante il pull | Assenza o errate credenziali `docker login` | Esegui `docker login` con credenziali Docker Hub valide. |
| Il container esce immediatamente | Variabili di ambiente obbligatorie mancanti | Fornisci `ASPOSE_CLIENT_ID` e `ASPOSE_CLIENT_SECRET` come mostrato nella sezione **Esecuzione del container**. |
| Conflitto di porta sull’host | Porta host già in uso | Scegli una porta host diversa (ad esempio `-p 8081:80`). |

---  

## Vedi anche  

* [Documentazione API Aspose.Cells Cloud](/cells/cloud/api/)  
* [Note di rilascio di Aspose.Cells Cloud](/cells/release-notes/) – log dettagliato delle modifiche per la versione 21.9 e successive.  
* [Funzionalità del container Docker di Aspose.Cells](/cells/docker/features/)  
* [Tag immagine Docker di Aspose.Cells](/cells/docker/tag-list/)  

---  

*Redatto dal team di ingegneria Aspose Cloud.*