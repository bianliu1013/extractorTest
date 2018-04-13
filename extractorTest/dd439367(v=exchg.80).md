---
title: Connessione RPC su HTTP non consentita
TOCTitle: Connessione RPC su HTTP non consentita
ms:assetid: 227f8a97-18cc-41c2-a49c-f62919a8ace9
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439367(v=EXCHG.80)
ms:contentKeyID: 27341528
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Connessione RPC su HTTP non consentita

 

_**Ultima modifica dell'argomento:** 2011-02-10_

L'analizzatore di Microsoft Exchange tenta di accedere all'Archivio informazioni con RPC su HTTP. Se l'errore restituito dall'Archivio informazioni è ecRpcHttpDisallowed, l'Analizzatore connettività remota di Exchange restituisce il seguente messaggio di errore.

"Non sono consentite connessioni RPC su HTTP per questo client"

## Per ulteriori informazioni

L'errore generato dall'Analizzatore connettività remota di Exchange non è necessariamente indicativo di un problema. Impedire ai client di connettersi con RPC su HTTP è un'opzione di configurazione legittima. Tuttavia, se l'Analizzatore connettività remota di Exchange è stato eseguito perché vi sono client Outlook che non riescono a connettersi tramite RPC su HTTP o Outlook via Internet, sarà necessario modificare l'impostazione che impedisce ai client di connettersi utilizzando questo metodo.

Per stabilire se per la cassetta postale di Exchange 2007 o 2010 è abilitata la funzionalità RPC su HTTP o Outlook via Internet, eseguire il seguente comando da Exchange Management Shell:

`Get-CASMailbox MailboxName | FL MAPIBlockOutlookRpcHTTP`

Se il comando restituisce il valore $true, è necessario abilitare Outlook via Internet per la cassetta postale di Exchange 2007 utilizzando il seguente comando:

`Set-CASMailbox MailboxName -MAPIBlockOutlookRpcHTTP:$false  `

Per ulteriori informazioni, vedere [Quando si utilizza Outlook con una cassetta postale di Exchange 2007, non è possibile connettersi a Exchange 2007 e si riceve un messaggio di errore](http://go.microsoft.com/fwlink/?linkid=100100).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

## Vedere anche

#### Altre risorse

[Set-CASMailbox](http://technet.microsoft.com/it-it/library/bb125264.aspx)

