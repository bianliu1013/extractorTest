---
title: Impossibile negoziare una versione Airsync appropriata con il server
TOCTitle: Impossibile negoziare una versione Airsync appropriata con il server
ms:assetid: b2b4c060-32c3-417e-840a-50981b455927
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439385(v=EXCHG.80)
ms:contentKeyID: 27341586
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Impossibile negoziare una versione Airsync appropriata con il server

 

***Ultima modifica dell'argomento:** 2009-08-18*

L'analizzatore di Microsoft Exchange invia una richiesta HTTP con il verbo OPTIONS alla directory virtuale Microsoft-Server-ActiveSync sul server e analizza le intestazioni HTTP nella risposta HTTP. Se l'intestazione MS-ASProtocolVersions non contiene 2.5 o 12.0, l'Analizzatore connettività remota di Exchange visualizza il seguente messaggio di errore:

"Impossibile negoziare una versione Airsync appropriata con il server."

## Per ulteriori informazioni

L'Analizzatore connettività remota di Exchange supporta al momento il protocollo Exchange ActiveSync versioni 2.5 e 12.0. Si si utilizza Exchange Server 2003 SP1 o precedenti, questo errore non indica necessariamente un problema. Al contrario, indica semplicemente che lo strumento non è in grado di analizzare adeguatamente il server. Aggiornare a Exchange Server 2003 Service Pack 2 per disporre della funzionalità ActiveSync v2.5.

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

