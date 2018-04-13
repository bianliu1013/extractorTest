---
title: Controllo di preautenticazione del firewall
TOCTitle: Controllo di preautenticazione del firewall
ms:assetid: cba32708-7292-4504-9663-42786a381bdd
ms:mtpsurl: https://technet.microsoft.com/it-it/library/JJ710173(v=EXCHG.80)
ms:contentKeyID: 49378893
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Controllo di preautenticazione del firewall

 

***Ultima modifica dell'argomento:** 2013-03-21*

Lo strumento Analizzatore connettività remota di Microsoft Exchange (RCA) esegue delle query per stabilire se i record DNS puntano all'endpoint di individuazione automatica. Una volta eseguita la ricerca, lo strumento RCA esegue altre query per verificare se l'autenticazione è stata configurata correttamente. Succede spesso che un dispositivo perimetrale quale Microsoft Threat Management Gateway (TMG) non sia configurato correttamente.

Spesso gli utenti scelgono di utilizzare la preautenticazione per il dispositivo perimetrale. Questa soluzione è corretta per applicazioni quali Outlook Anywhere e OWA, ma può causare dei problemi con la distribuzione ibrida di Office 365. È necessario impostare l'autenticazione pass-through per alcuni endpoint che utilizzano l'autorizzazione basata su token piuttosto che le opzioni di autenticazione integrate/base standard.

La soluzione è semplice. Creare una regola che utilizza lo stesso listener di altri componenti di Exchange, ma fornisce anche percorsi espliciti per gli endpoint che necessitano dell'autenticazione pass-through. Configurare la nuova regola in modo che esegua la preautenticazione sul dispositivo perimetrale. Se la regola viene implementata correttamente, è possibile continuare a utilizzare sul medesimo listener lo stesso indirizzo IP esterno e la stessa porta (443) per entrambe le regole.

## Ulteriori informazioni

Per informazioni su come configurare TMG per le distribuzioni ibride di Office 365 e una regola per percorsi specifici che richiedono un'autenticazione pass-through, vedere l'articolo su [come configurare TMG per le distribuzioni ibride di Office 365 (Exchange)](http://go.microsoft.com/fwlink/p/?linkid=241473).

Prima di decidere come configurare Autodiscover, si consiglia di scaricare e leggere l'articolo relativo alla [pubblicazione di Exchange Server 2010 con Forefront Unified Access Gateway 2010 e Forefront Threat Management Gateway 2010](http://go.microsoft.com/fwlink/p/?linkid=197136).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per cui è attualmente disponibile documentazione limitata. Per migliorare la documentazione relativa a ciascun errore che può verificarsi, Microsoft ha scelto di affidarsi alla community per ottenere ulteriori informazioni. Utilizzare la sezione Contenuti Community in questo argomento per segnalare eventuali errori riscontrati fino a questo punto. Se è necessario richiedere assistenza tecnica, contattare il [supporto Microsoft](http://go.microsoft.com/fwlink/?linkid=8158) oppure creare una nuova segnalazione nel forum dedicato allo strumento RCA su TechNet. Sebbene il forum sia stato sospeso, gli argomenti in esso pubblicati restano attivi nella sezione relativa alle [versioni precedenti di Exchange - Componenti, strumenti e utilità estesi](http://go.microsoft.com/fwlink/p/?linkid=288878).

