---
title: Il token ADFS non viene accettato dalla piattaforma di autenticazione (per la versione successiva di RCA)
TOCTitle: Il token ADFS non viene accettato dalla piattaforma di autenticazione (per la versione successiva di RCA)
ms:assetid: 3134b441-17fa-44a9-a2e8-afea51b5a3b1
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Hh241331(v=EXCHG.80)
ms:contentKeyID: 42607543
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Il token ADFS non viene accettato dalla piattaforma di autenticazione (per la versione successiva di RCA)

 

_**Ultima modifica dell'argomento:** 2011-06-06_

L'Analizzatore connettività remota di Microsoft Exchange interroga la piattaforma di autenticazione nel cloud per individuare l'area di autenticazione. Al termine del processo la piattaforma di autenticazione passa al client richiedente l'URL dell'endpoint ADFS necessario per l'autenticazione del client. In alcuni casi, le informazioni di configurazione restituite inducono il server ADFS a rispondere con un token non valido, a causa della configurazione esistente nell'ambiente ADFS locale.

L'Analizzatore connettività remota visualizza un avviso quando nell'autorizzazione non viene indicato che il token non è stato accettato dalla piattaforma di autenticazione del cloud. Per risolvere il problema, correggere l'impostazione di configurazione errata nell'ambiente ADFS locale. Dopo la risoluzione del problema, è necessario aggiornare le impostazioni nella piattaforma di autenticazione del cloud. Questo problema interessa in genere i clienti che utilizzano ambienti federati con versioni precedenti dei servizi online.

## Ulteriori informazioni

Per informazioni su come risolvere questo problema, vedere l'articolo 2521057 della Microsoft Knowledge Base, [Come ristabilire la relazione di trust con il servizio Microsoft Online Services ID dopo il server 2. 0 di ADFS si blocca](http://support.microsoft.com/kb/2521057)

Per informazioni della Guida sull'aggiornamento dell'ambiente Exchange 2010 corrente, vedere [Assistente per la distribuzione di Exchange Server (in lingua inglese)](http://technet.microsoft.com/it-it/exdeploy2010/default.aspx).

