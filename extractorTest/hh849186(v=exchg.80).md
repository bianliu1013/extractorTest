---
title: Elemento EXCH mancante nella risposta XML del servizio di individuazione automatica
TOCTitle: Elemento EXCH mancante nella risposta XML del servizio di individuazione automatica
ms:assetid: 6fbe75af-f438-4b46-84e8-55d14a5ae69c
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Hh849186(v=EXCHG.80)
ms:contentKeyID: 45478515
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Elemento EXCH mancante nella risposta XML del servizio di individuazione automatica

 

***Ultima modifica dell'argomento:** 2012-02-07*

L'analizzatore connettività remota di Microsoft Exchange interroga la risposta HTTP del servizio di individuazione automatica per individuare gli attributi contenuti nell'XML all'interno della risposta. Nell'XML si trovano in genere i seguenti provider di Microsoft Office Outlook e loro relativi attributi.

  -  **Provider EXCH**   
    Le impostazioni di connessione e gli URL dei servizi Exchange utilizzati quando Outlook viene connesso tramite RPC su TCP

<!-- end list -->

  -  **Provider EXPR**   
    Le impostazioni di connessione e gli URL dei servizi Exchange utilizzati quando Outlook viene connesso tramite RPC su HTTP (Outlook via Internet)

Se nella risposta XML del servizio di individuazione automatica manca l'elemento EXCH, l'analizzatore connettività remota visualizza il seguente messaggio di errore:

Elemento EXCH mancante nella risposta XML del servizio di individuazione automatica

## Per ulteriori informazioni

L'elemento EXCH nell'XML dell'individuazione automatica contiene informazioni che vengono utilizzate dal client Outlook per stabilire le connessioni RPC su TCP al server su cui è in esecuzione Exchange Server. In genere, queste connessioni sono interne alla rete aziendale. Tuttavia, è necessaria anche la sezione EXCH quando la connessione viene stabilita tramite RPC su HTTP (Outlook via Internet).

Se manca l'elemento EXCH, l'accesso MAPI potrebbe non essere abilitato per l'utente. Per verificare se un utente è abilitato per l'accesso MAPI alla cassetta postale, eseguire questo comando in Exchange Management Shell:

    Get-CASMailbox MailboxName | fl MapiEnabled

Se il comando restituisce il valore $false, è necessario abilitare la funzionalità MAPI per la cassetta postale o selezionare un metodo di connessione alternativo. Per abilitare la funzionalità MAPI per la cassetta postale, eseguire il comando riportato di seguito:

    Set-CASMailbox MailboxName -MapiEnabled:$true

L'analizzatore connettività remota di Exchange è un nuovo strumento per cui è attualmente disponibile una documentazione limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati fino a questo punto. Se è necessaria assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

## Vedere anche

#### Concetti

[Elemento EXPR mancante nella risposta XML del servizio di individuazione automatica](dd439390\(v=exchg.80\).md)  
[Connessioni MAPI non consentite](dd439370\(v=exchg.80\).md)  

#### Altre risorse

[Set-CasMailbox](http://technet.microsoft.com/it-it/library/bb125264.aspx)

