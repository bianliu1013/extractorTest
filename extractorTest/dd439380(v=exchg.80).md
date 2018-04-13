---
title: Ricevuta risposta HTTP positiva diversa da risposta di reindirizzamento
TOCTitle: Ricevuta risposta HTTP positiva diversa da risposta di reindirizzamento
ms:assetid: 933f43be-6a74-4d3d-b702-f327d33408f5
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439380(v=EXCHG.80)
ms:contentKeyID: 27341570
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Ricevuta risposta HTTP positiva diversa da risposta di reindirizzamento

 

***Ultima modifica dell'argomento:** 2009-08-17*

L'analizzatore di Microsoft Exchange invia una richiesta HTTP al server Accesso client mentre tenta di contattare il servizio di individuazione automatica tramite il metodo di reindirizzamento HTTP. Durante questa verifica, l'unico tipo di risposta accettata è un reindirizzamento HTTP; qualsiasi altro codice di stato indica un problema. Una risposta di reindirizzamento prevista avrà il codice di stato 301, 302 o 307. Se si riceve una qualsiasi altra risposta, l'Analizzatore connettività remota di Exchange visualizza il seguente messaggio di errore:

"Ricevuta risposta HTTP positiva diversa da risposta di reindirizzamento."

## Per ulteriori informazioni

  - Per informazioni su come configurare il reindirizzamento per Outlook Web Access, vedere "Come semplificare l'URL di Outlook Web Access" (<http://go.microsoft.com/fwlink/?linkid=130623>).  

Per ulteriori informazioni su come configurare il reindirizzamento per l'individuazione automatica, vedere "White Paper: Servizio di individuazione automatica di Exchange 2007" (<http://go.microsoft.com/fwlink/?linkid=85214>).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

