---
title: Elemento AuthPackage mancante nella risposta XML del servizio di individuazione automatica
TOCTitle: Elemento AuthPackage mancante nella risposta XML del servizio di individuazione automatica
ms:assetid: 5ffece69-b240-4d37-ab6a-7b257c03cb7f
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439374(v=EXCHG.80)
ms:contentKeyID: 27341551
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Elemento AuthPackage mancante nella risposta XML del servizio di individuazione automatica

 

_**Ultima modifica dell'argomento:** 2009-09-01_

L'analizzatore di Microsoft Exchange invia una richiesta di individuazione automatica XML al server Accesso client di Exchange 2007 remoto e analizza la risposta. Se nella risposta XML proveniente dal servizio di individuazione automatica non è presente alcun elemento AuthPackage, l'Analizzatore connettività remota di Exchange visualizza il seguente messaggio di errore:

"Elemento AuthPackage mancante nella risposta XML del servizio di individuazione automatica"

Generalmente, questo errore si verifica quando l'attributo Server non è impostato correttamente per il provider Outlook EXPR. Se per il valore dell'attributo è specificata un'impostazione diversa da quella predefinita (NULL), agli utenti finali potrebbe venire richiesto di immettere le loro credenziali quando si connettono usando Outlook via Internet, anche se per l'autenticazione NTLM (NT LAN Manager) sono state configurate le impostazioni proxy di Exchange in Outlook 2007.

## Per ulteriori informazioni

EXPR è uno dei provider Outlook che è possibile gestire utilizzando i cmdlet Get-OutlookProvider e Set-OutlookProvider in Exchange Management Shell. Per l'attributo Server dell'oggetto OutlookProvider deve essere mantenuta l'impostazione predefinita $null. È possibile controllare il valore dell'attributo Server eseguendo il cmdlet Get-OutlookProvider (Get-OutlookProvider Identity | elenco formati).

Per ulteriori informazioni, incluse le istruzione su come modificare l'attributo Server, vedere [Il servizio di individuazione automatica restituisce valori imprevisti per le impostazioni proxy di Outlook via Internet](http://go.microsoft.com/fwlink/?linkid=161812).

Per ulteriori informazioni sulla modifica dei provider Outlook, vedere [Quando, se e come modificare i provider Outlook](http://go.microsoft.com/fwlink/?linkid=160947)

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

