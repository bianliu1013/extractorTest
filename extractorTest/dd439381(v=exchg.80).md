---
title: Inoltro aperto rilevato
TOCTitle: Inoltro aperto rilevato
ms:assetid: 94007fb7-3f2a-43b4-a4b8-20efed3db232
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439381(v=EXCHG.80)
ms:contentKeyID: 27341573
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Inoltro aperto rilevato

 

_**Ultima modifica dell'argomento:** 2009-08-18_

L'analizzatore di Microsoft Exchange tenta di inviare un messaggio di prova utilizzando l'indirizzo di un destinatario che non appartiene all'organizzazione di Exchange. Se l'operazione riesce, il server SMTP opera come punto di inoltro aperto e la prova visualizza il seguente messaggio:

"Messaggio di prova di inoltro aperto recapitato correttamente a Admin@TestExchangeConnectivity.com"

Anche se è possibile configurare un computer con Microsoft Exchange 2000 Server, Exchange Server 2003 o Exchange Server 2007 come inoltro di posta elettronica, non è comunque consigliato.

Un computer Exchange configurato come inoltro aperto di posta elettronica può essere utilizzato per inviare posta commerciale indesiderata (spam). Se altri server di posta elettronica individuano il computer Exchange come server di posta elettronica commerciale indesiderata, il computer Exchange potrebbe essere aggiunto agli elenchi Blocca.

## Per ulteriori informazioni

Per risolvere questo problema, vedere il seguente articolo di Exchange Best Practices Analyzer [Il server SMTP non ha eseguito correttamente la prova di inoltro aperto](http://go.microsoft.com/fwlink/?linkid=161823).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

