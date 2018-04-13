---
title: Endpoint EWS con puntamento a un server legacy locale
TOCTitle: Endpoint EWS con puntamento a un server legacy locale
ms:assetid: acc50014-a6c7-4453-9167-2eb6f034a45b
ms:mtpsurl: https://technet.microsoft.com/it-it/library/JJ710172(v=EXCHG.80)
ms:contentKeyID: 49378892
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Endpoint EWS con puntamento a un server legacy locale

 

***Ultima modifica dell'argomento:** 2012-11-06*

Lo strumento Analizzatore connettività remota di Microsoft Exchange consente di individuare eventuali problemi che hanno per oggetto le query sulla disponibilità tra una cassetta postale di Office 365 e una cassetta postale locale. Questo controllo dello stato verifica anche che il server Exchange locale soddisfi i requisiti minimi per la versione. Affinché una query sulla disponibilità cross-premise funzioni, il server che ospita l'individuazione automatica e gli endpoint EWS devono utilizzare Microsoft Exchange Server 2010 SP1 o una versione successiva.

È frequente che nelle organizzazioni gli endpoint rivolti verso l'esterno (ad esempio, autodiscover.contoso.com e mail.contoso.com) puntino erroneamente a versioni precedenti di Exchange Server (“server legacy”) perché i record DNS non vengono aggiornati affinché puntino a un server su cui è installato Exchange Server 2010 SP1 o una versione successiva.

Per il corretto funzionamento delle funzionalità di distribuzione ibrida e disponibilità, è necessario Exchange Server 2010 SP1 o una versione successiva. I server legacy non dispongono della logica necessaria per gestire i complessi requisiti del flusso di lavoro di autenticazione associati a una richiesta federata.

Per risolvere questo problema, verificare che i record DNS esterni per l'individuazione automatica ed EWS puntino al server con connessione Internet su cui è in esecuzione Exchange Server 2010 SP1 o una versione successiva.

## Ulteriori informazioni

Per informazioni su come risolvere i problemi di disponibilità federata, fare riferimento all'articolo della Microsoft Knowledge Base [2555008: Come risolvere i problemi di disponibilità quando si utilizza la federazione di Exchange in Microsoft Office 365 per l'ambiente aziendale](http://support.microsoft.com/kb/2555008).

Si consiglia di consultare le seguenti risorse prima di scegliere come configurare un server Exchange cross-premise:

  - [Assistente per la distribuzione di Exchange Server](http://technet.microsoft.com/it-it/exdeploy2010/default.aspx)  
  - Articolo della Microsoft Knowledge Base [2555008: Come risolvere i problemi di disponibilità quando si utilizza la federazione di Exchange in Microsoft Office 365 per l'ambiente aziendale](http://support.microsoft.com/kb/2555008)  

## Altre risorse

L'Analizzatore connettività remota di Exchange è un nuovo strumento per cui è attualmente disponibile documentazione limitata. Per migliorare la documentazione relativa a ciascun errore che può verificarsi, Microsoft ha scelto di affidarsi alla community per ottenere ulteriori informazioni. Utilizzare la sezione Contenuti Community in questo argomento per segnalare eventuali errori riscontrati fino a questo punto. Se è necessario richiedere assistenza tecnica, contattare il [supporto](http://go.microsoft.com/fwlink/?linkid=8158) oppure creare una nuova segnalazione nel forum dedicato allo strumento Analizzatore connettività remota su TechNet. Sebbene il forum sia stato sospeso, gli argomenti in esso pubblicati restano attivi in [Versioni precedenti di Exchange - Componenti, strumenti e utilità estesi](http://social.technet.microsoft.com/forums/it-it/exchangesvr3rdpartyappslegacy).

