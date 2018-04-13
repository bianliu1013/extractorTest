---
title: Connessioni MAPI non consentite
TOCTitle: Connessioni MAPI non consentite
ms:assetid: 443715ec-0a7c-470f-ac15-7433441de3ec
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439370(v=EXCHG.80)
ms:contentKeyID: 27341543
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Connessioni MAPI non consentite

 

***Ultima modifica dell'argomento:** 2010-06-21*

L'analizzatore di Microsoft Exchange interroga Exchange Server e tenta di connettersi con RPC su HTTP. Se le connessioni MAPI sono disabilitate su Exchange Server 2007 o 2010, potrebbe verificarsi l'errore seguente:

"All'utente non è consentito accedere al server tramite l'interfaccia del protocollo MAPI."

Questa funzionalità potrebbe essere importante per i provider di servizi di hosting che desiderano indurre gli utenti finali a connettersi a Exchange con Outlook Web Access, ma non con Outlook (tramite normale connessione MAPI oppure RPC su HTTP). Tuttavia, se questa funzionalità è abilitata, l'Analizzatore connettività remota di Microsoft Exchange (ExRCA) non funzionerà durante la prova delle connessioni RPC su HTTP o Outlook via Internet.

Se il server Exchange 2007 o 2010 è stato configurato per impedire le connessioni MAPI, gli utenti finali potrebbero ricevere il messaggio di errore seguente:

"L'amministratore di Exchange Server ha bloccato la versione di Outlook che si sta utilizzando. Contattare l'amministratore per richiedere assistenza."

## Per ulteriori informazioni

L'errore generato dall'Analizzatore connettività remota di Exchange non è necessariamente indicativo di un problema. Impedire ai client di connettersi con MAPI è un'opzione di configurazione legittima. Tuttavia, se l'Analizzatore connettività remota di Exchange è stato eseguito perché vi sono client Outlook che non riescono a connettersi, sarà necessario modificare l'impostazione che impedisce ai client MAPI di connettersi.

Per determinare se la funzionalità MAPI è disabilitata per la cassetta postale, eseguire il comando riportato di seguito:

    Get-CASMailbox MailboxName | FL mapienabled

Se il comando restituisce il valore $false, è necessario abilitare la funzionalità MAPI per la cassetta postale o scegliere un metodo di connessione alternativo. Per abilitare la funzionalità MAPI per la cassetta postale, eseguire il comando riportato di seguito:

    Set-CASMailbox MailboxName -mapienabled:$true

Per ulteriori informazioni, vedere [Quando si utilizza Outlook con una cassetta postale di Exchange 2007, non è possibile connettersi a Exchange 2007 e si riceve un messaggio di errore](http://go.microsoft.com/fwlink/?linkid=100100).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

## Vedere anche

#### Altre risorse

[Set-CASMailbox](http://technet.microsoft.com/it-it/library/bb125264.aspx)

