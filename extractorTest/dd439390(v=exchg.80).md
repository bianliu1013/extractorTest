---
title: Elemento EXPR mancante nella risposta XML del servizio di individuazione automatica
TOCTitle: Elemento EXPR mancante nella risposta XML del servizio di individuazione automatica
ms:assetid: cdd6809e-b5dc-49e5-b977-750ccec1e1eb
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439390(v=EXCHG.80)
ms:contentKeyID: 27341597
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Elemento EXPR mancante nella risposta XML del servizio di individuazione automatica

 

_**Ultima modifica dell'argomento:** 2011-02-10_

L'analizzatore di Microsoft Exchange interroga la risposta HTTP del servizio di individuazione automatica per individuare gli attributi contenuti nell'XML all'interno della risposta. Nell'XML si trovano in genere due provider di Outlook e relativi attributi:

  - **Provider EXCH**  
    Le impostazioni della connessione e gli URL dei servizi Exchange utilizzati quando Outlook si connette con RPC.

<!-- end list -->

  - **Provider EXPR**  
    Le impostazioni della connessione e gli URL dei servizi Exchange utilizzati quando Outlook si connette con HTTP (Outlook via Internet).

Se nella risposta XML del servizio di individuazione automatica manca l'elemento EXPR, l'Analizzatore connettività remota di Exchange visualizza il seguente messaggio di errore:

"Elemento EXPR mancante nella risposta XML del servizio di individuazione automatica."

Questo in genere significa che Outlook via Internet non è abilitato o non è configurato correttamente.

## Per ulteriori informazioni

  - Per ulteriori informazioni sull'implementazione di Outlook via Internet, vedere [Implementazione di Outlook via Internet](http://go.microsoft.com/fwlink/?linkid=80831).  
  - Per ulteriori informazioni sui provider di Outlook, vedere [Il servizio di individuazione automatica e i provider di Outlook: come funzionano?](http://go.microsoft.com/fwlink/?linkid=161811)  

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

