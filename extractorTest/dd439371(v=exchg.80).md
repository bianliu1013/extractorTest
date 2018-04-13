---
title: Impossibile stabilire un'autenticazione reciproca
TOCTitle: Impossibile stabilire un'autenticazione reciproca
ms:assetid: 445d87c5-422f-4249-821b-0c805a058ff4
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439371(v=EXCHG.80)
ms:contentKeyID: 27341546
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Impossibile stabilire un'autenticazione reciproca

 

_**Ultima modifica dell'argomento:** 2009-09-01_

L'analizzatore di Microsoft Exchange negozia una connessione SSL con l'host remoto per recuperare varie proprietà dei certificati X509. L'Analizzatore connettività remota di Exchange esamina l'attributo Subject per identificare il nome di dominio completo (FQDN) o il nome comune assegnato al certificato (ad esempio, mail.contoso.com).

Se il nome comune non corrisponde alla stringa (msstd:) di autenticazione reciproca immessa nell'Analizzatore connettività remota di Exchange per la verifica della funzionalità di Outlook via Internet, l'Analizzatore connettività remota di Exchange visualizza il seguente messaggio di errore.

"Impossibile stabilire autenticazione reciproca."

La stringa di autenticazione reciproca corrisponde all'impostazione "Connetti solo a server proxy con il seguente nome entità nel certificato" in Impostazioni proxy Exchange di Outlook. Questo errore può verificarsi anche quando la stringa di autenticazione reciproca è valida, ma non lo è l'attributo CertPrincipalName dei provider Outlook EXPR in Active Directory.

Quelli elencati di seguito sono alcuni dei sintomi di questo problema:

  - Agli utenti vengono ripetutamente richieste le credenziali senza che riescano a connettersi a Exchange Server utilizzando Outlook via Internet.  
  - Quando si consente a Outlook 2007 di creare automaticamente il profilo Outlook 2007, si riceve il seguente messaggio di errore: "Non è disponibile alcuna connessione crittografata al server di posta elettronica. Fare clic su Avanti per tentare di utilizzare una connessione non crittografata."  

## Soluzione

Per risolvere il problema, fare quanto segue:

1.  Visualizzare il certificato del server Web installato sul server Accesso client Exchange 2007 e verificare il nome comune per l'emissione del certificato (ad esempio, mail.contoso.com).  

2.  Aprire Impostazioni proxy Exchange in Microsoft Outlook e verificare che il nome di dominio completo (FQDN) sia stato immesso correttamente nel campo Nome principale di autenticazione reciproca (ad esempio, msstd:mail.contoso.com).  

3.  Se necessario, utilizzare Exchange Management Shell per modificare l'attributo CertPrincipalName come indicato di seguito:  
    
        Set-OutlookProvider EXPR -CertPrincipalName:"msstd:mail.contoso.com"

## Per ulteriori informazioni

  - Per ulteriori informazioni sul nome principale di autenticazione reciproca, vedere [Nomi principali](http://go.microsoft.com/fwlink/?linkid=93417).  
  - Per ulteriori informazioni sui provider Outlook Exchange 2007, vedere [Il servizio di individuazione automatica e i provider Outlook - come funzionano](http://go.microsoft.com/fwlink/?linkid=161811) e [Set-OutlookProvider](http://go.microsoft.com/fwlink/?linkid=161815).  

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

