---
title: Intestazione prevista del servizio non ricevuta durante la connessione
TOCTitle: Intestazione prevista del servizio non ricevuta durante la connessione
ms:assetid: ca72939d-dd53-4939-900d-39fe412c220e
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439389(v=EXCHG.80)
ms:contentKeyID: 27341595
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Intestazione prevista del servizio non ricevuta durante la connessione

 

***Ultima modifica dell'argomento:** 2009-08-18*

L'analizzatore di Microsoft Exchange tenta di connettersi al server SMTP di Exchange. A connessione avvenuta, il server SMTP invia un'intestazione SMTP. Se questa intestazione non viene mai ricevuta a causa di un timeout o altro problema, viene visualizzato il seguente messaggio:

"Intestazione prevista del servizio non ricevuta durante la connessione."

## Per ulteriori informazioni

Se si utilizza un inoltro di posta elettronica o un filtro SMTP (disponibile su molti prodotti firewall), si consiglia di iniziare la diagnostica a partire da questi prodotti. Per eseguire la diagnostica, potrebbe essere necessario disabilitare o bypassare questi prodotti.

  - Se non si utilizza un inoltro di posta elettronica o un filtro SMTP, accertarsi che il processo appropriato sia in ascolto sulla porta 25 (SMTP). Utilizzare l'utilità netstat.exe per stabilire se il servizio appropriato è in realtà in ascolto sulla porta su cui si esegue la verifica seguendo la procedura riportata nell'articolo della Microsoft Knowledge Base, "Individuazione del programma che utilizza o blocca specifiche porte TCP in Windows Server 2003" ([http://go.microsoft.com/fwlink/?linkid=3052\&kbid=323352](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=323352)).  
  - Per Exchange Server 2003, il nome del processo deve essere inetinfo.exe. Per Exchange Server 2007, il nome del processo deve essere edgetransport.exe.  

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

