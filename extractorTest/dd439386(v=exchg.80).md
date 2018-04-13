---
title: Si è verificato un errore di rete durante la comunicazione con l'host remoto
TOCTitle: Si è verificato un errore di rete durante la comunicazione con l'host remoto
ms:assetid: b2e81fe1-5a94-4d07-9d58-ad483268a72a
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439386(v=EXCHG.80)
ms:contentKeyID: 27341588
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Si è verificato un errore di rete durante la comunicazione con l'host remoto

 

_**Ultima modifica dell'argomento:** 2009-11-18_

L'analizzatore di Microsoft Exchange tenta di effettuare una connessione TCP con l'host fornito durante la prova. Se l'analizzatore connettività remota di Exchange non è in grado di stabilire una connessione TCP sulla porta 80 e sulla porta 443 con l'host, viene visualizzato il seguente messaggio di errore:

"Si è verificato un errore di rete durante la comunicazione con l'host remoto: '0'"

Dove "0" indica informazioni aggiuntive che descrivono il motivo per cui la connessione non è riuscita.

ExRCA deve essere in grado di stabilire una sessione TCP sulle porte 25, 80 e 443 durante le varie prove eseguite dallo strumento.

## Per ulteriori informazioni

Gli errori di connessione di questo tipo sono causati in genere dai seguenti motivi:

  - Il server non è attivo.  
  - La porta specificata non è in ascolto delle connessioni TCP.  
  - Un firewall, server proxy o dispositivo hardware blocca la connessione con il server.  
  - La rete è congestionata.  

**Per correggere questo errore**

1.  Accertarsi che il server sia attivo e disponibile sulla rete seguendo la procedura riportata nell'articolo 323388 della Microsoft Knowledge Base, "Diagnosi e verifica del funzionamento di connessioni di rete TCP/IP o NetBIOS in Windows Server 2003" ([http://go.microsoft.com/fwlink/?LinkId=3052\&kbid=323388](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=323388)).

2.  Utilizzare l'utilità netstat.exe per stabilire se il servizio appropriato è in realtà in ascolto sulla porta su cui si esegue la verifica seguendo la procedura riportata nell'articolo 323352 della Microsoft Knowledge Base, "Individuazione del programma che utilizza o blocca specifiche porte TCP in Windows Server 2003" ([http://go.microsoft.com/fwlink/?LinkId=3052\&kbid=323352](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=323352)).

3.  Utilizzare lo strumento Portqry.exe per verificare la connettività TCP da diversi punti all'interno e all'esterno della rete per stabilire se un dispositivo di rete blocca la connettività con la porta specificata. Per ulteriori informazioni, vedere l'articolo della Microsoft Knowledge Base, "Utilizzo di Portqry.exe per risolvere problemi di connettività di Microsoft Exchange Server" ([http://go.microsoft.com/fwlink/?LinkId=3052\&kbid=310298](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=310298)).

4.  Utilizzare Network Monitor per acquisire il traffico di rete e risolvere il problema. Per ulteriori informazioni, vedere l'articolo della Microsoft Knowledge Base, "Informazioni su Network Monitor 3.2 in Windows Vista" ([http://go.microsoft.com/fwlink/?LinkId=3052\&kbid=955998](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=955998)).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

