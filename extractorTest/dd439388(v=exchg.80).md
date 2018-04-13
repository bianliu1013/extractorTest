---
title: Il provider del servizio di individuazione automatica di Outlook ha restituito uno stato di errore nella risposta XML
TOCTitle: Il provider del servizio di individuazione automatica di Outlook ha restituito uno stato di errore nella risposta XML
ms:assetid: c303f114-a284-4ba9-a324-a5764b241cd4
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439388(v=EXCHG.80)
ms:contentKeyID: 27341593
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Il provider del servizio di individuazione automatica di Outlook ha restituito uno stato di errore nella risposta XML

 

_**Ultima modifica dell'argomento:** 2012-02-24_

L'analizzatore di Microsoft Exchange invia una richiesta XML/HTTP di individuazione automatica al servizio di individuazione automatica di Exchange utilizzando lo schema del provider di Outlook per individuare le impostazioni di Outlook per l'utente specificato. Quando nella risposta è presente un messaggio di errore, l'Analizzatore connettività remota di Exchange visualizza il seguente messaggio di errore:

"Il provider del servizio di individuazione automatica di Outlook ha restituito un messaggio di errore nella risposta XML."

Il servizio di individuazione automatica viene utilizzato da Microsoft Office Outlook 2007 e versioni successive per configurare automaticamente le impostazioni di connessione e individuare gli URL per i servizi Exchange tra cui il servizio Disponibilità, Assistente fuori sede, rubriche offline distribuite su Web e messaggistica unificata. Se Outlook non riesce a connettersi al servizio di individuazione automatica, non sarà possibile creare automaticamente le impostazioni del profilo o connettersi ai servizi Exchange.

## Per ulteriori informazioni

Il servizio di individuazione automatica di Exchange potrebbe visualizzare i seguenti messaggi di errore:

  - "L'individuazione automatica non può elaborare l'indirizzo di posta elettronica specificato. Sono consentiti solo le cassette postali e i contatti."  
  - "Impossibile trovare l'indirizzo di posta elettronica."  
  - "Le cassette postali client devono trovarsi in un Exchange 2007 Server o versione successiva."  

Per risolvere questo problema, verificare che l'account che si utilizza abbia una cassetta postale Exchange 2007 e che sia associato ad un indirizzo di posta elettronica valido.

Per ulteriori informazioni sul servizio di individuazione automatica, vedere il [White Paper: Servizio di individuazione automatica di Exchange 2007](http://go.microsoft.com/fwlink/?linkid=157773).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

