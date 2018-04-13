---
title: Impossibile trovare il record posizione servizio (SRV) di individuazione automatica nel DNS
TOCTitle: Impossibile trovare il record posizione servizio (SRV) di individuazione automatica nel DNS
ms:assetid: f7432938-9087-4033-9648-224565858a5d
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439398(v=EXCHG.80)
ms:contentKeyID: 27341615
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Impossibile trovare il record posizione servizio (SRV) di individuazione automatica nel DNS

 

***Ultima modifica dell'argomento:** 2009-08-18*

L'analizzatore di Microsoft Exchange interroga il DNS per stabilire se esistono record posizione servizio (SRV) per l'individuazione automatica. Questa query per la posizione servizio DNS è in formato "\_autodiscover.\_tcp.\<smtpDomain\>" dove \<smtpDomain\> corrisponde alla parte destra dell'indirizzo SMTP principale dell'utente. Se l'Analizzatore connettività remota di Exchange non è in grado di individuare tutti i record SRV per l'individuazione automatica in quello spazio dei nomi, viene visualizzato il seguente errore:

"Impossibile trovare i record SRV per l'individuazione automatica nel DNS".

I client Microsoft Office Outlook 2007 tentano di connettersi al servizio di individuazione automatica utilizzando quattro metodi. Se un metodo fallisce, si passa al successivo nel seguente ordine:

1.  Utilizzo di un oggetto del punto di connessione del servizio (SCP) in Active Directory  
2.  Utilizzo del DNS  
3.  Utilizzo di un reindirizzamento HTTP  
4.  Utilizzo di un record SRV  

<table>
<thead>
<tr class="header">
<th><img src="images/Dd439361.note(EXCHG.80).gif" title="note" alt="note" />Nota:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Questo deve essere considerato solo un errore se si intende configurare il proprio ambiente in modo che il percorso di individuazione automatica della directory virtuale sul server Accesso client venga trovato tramite un record SRV.</td>
</tr>
</tbody>
</table>

## Per ulteriori informazioni

Le seguenti risorse dovrebbe essere consultate prima di decidere come configurare l'individuazione automatica:

  - Per ulteriori informazioni su Outlook 2007 e l'interoperabilità del servizio di individuazione automatica, compresa la descrizione dei metodi che possono essere utilizzati per trovare il servizio di individuazione automatica, vedere [White Paper: Servizio di individuazione automatica di Exchange 2007](http://go.microsoft.com/fwlink/?linkid=85214).  
  - Per ulteriori informazioni sull'abilitazione di Outlook 2007 per l'utilizzo dei record SRV per trovare il servizio di individuazione automatica, vedere l'articolo di Microsoft Knowledge Base, "È disponibile una nuova funzionalità che consente ad Outlook 2007 di utilizzare i record di posizione servizio DNS (SRV) per individuare il servizio di individuazione automatica di Exchange" ([http://go.microsoft.com/fwlink/?LinkId=3052\&kbid=940881](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=940881)).  

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

