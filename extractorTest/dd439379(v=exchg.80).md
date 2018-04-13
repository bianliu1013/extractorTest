---
title: Le versioni del server e del client non sono compatibili
TOCTitle: Le versioni del server e del client non sono compatibili
ms:assetid: 8b6b8e13-6973-469d-a13b-983fa365d2be
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439379(v=EXCHG.80)
ms:contentKeyID: 27341566
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Le versioni del server e del client non sono compatibili

 

_**Ultima modifica dell'argomento:** 2011-02-10_

L'analizzatore di Microsoft Exchange tenta di connettersi a Exchange Server tramite RCP su HTTP (Outlook via Internet). Se la versione del client Outlook che sta tentando la connessione non è compatibile o non è supportata da Exchange Server, potrebbe comparire il seguente messaggio di errore.

"Le versioni del server e del client non sono compatibili. La versione del protocollo del client è precedente a quella richiesta dal server."

## Per ulteriori informazioni

Teoricamente, se si utilizza l'Analizzatore connettività remota di Exchange, questo errore non dovrebbe comparire. L'Analizzatore connettività remota di Exchange emula una connessione da parte del client basata sulla versione 12.0.4228.0. Se l'errore compare, è possibile che nel Registro di sistema del server Exchange il seguente valore sia stato modificato e impostato su un numero superiore a 12.0.4228.0. Se la modifica è stata apportata intenzionalmente, tenere presente che questo errore comparirà ogni volta che si utilizza l'Analizzatore connettività remota di Exchange e un qualsiasi client Outlook con una versione di protocollo inferiore.

HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\MSExchangeIS\\ParametersSystem

Valore DWORD: disabilita client MAPI

Per ulteriori informazioni, vedere l'articolo della Microsoft Knowledge Base che illustra come disabilitare l'accesso client MAPI per un computer con Exchange Server ([http://go.microsoft.com/fwlink/?LinkId=3052\&kbid=288894](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=288894)).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

