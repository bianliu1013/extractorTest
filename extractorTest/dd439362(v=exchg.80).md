---
title: È stata ricevuta una risposta di reindirizzamento imprevista
TOCTitle: È stata ricevuta una risposta di reindirizzamento imprevista
ms:assetid: 12995093-5ad0-467b-8566-6bfa98606f54
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439362(v=EXCHG.80)
ms:contentKeyID: 27341523
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# È stata ricevuta una risposta di reindirizzamento imprevista

 

***Ultima modifica dell'argomento:** 2009-08-18*

L'analizzatore di Microsoft Exchange invia una richiesta HTTP a Exchange Server per verificare che possa connettersi alle funzioni di Outlook Web Access, Exchange ActiveSync e Outlook via Internet. Una risposta positiva è indicata con HTTP 200 (o 207). Quando l'Analizzatore connettività remota di Exchange riceve una risposta di reindirizzamento (vale a dire 301, 302, 302) invece di 200 o 207, viene visualizzato il seguente messaggio di errore:

"È stata ricevuta una risposta di reindirizzamento imprevista."

Questo messaggio di errore indica che in IIS è configurato un reindirizzamento HTTP per una o più applicazioni Exchange in modo imprevisto o non supportato.

## Per ulteriori informazioni

  - Per informazioni su come configurare il reindirizzamento per Outlook Web Access, vedere [Come semplificare l'URL di Outlook Web Access](http://go.microsoft.com/fwlink/?linkid=130623).  
  - Per ulteriori informazioni su come configurare il reindirizzamento per l'individuazione automatica, vedere il [White Paper: Servizio di individuazione automatica di Exchange 2007](http://go.microsoft.com/fwlink/?linkid=85214).  

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

