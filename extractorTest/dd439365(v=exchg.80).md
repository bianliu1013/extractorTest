---
title: È stata restituita una risposta HTTP 403.4 in quanto si richiedeva SSL sulla directory virtuale
TOCTitle: È stata restituita una risposta HTTP 403.4 in quanto si richiedeva SSL sulla directory virtuale
ms:assetid: 1ce88d57-a5e6-4797-b3fe-1ba0f2410f11
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439365(v=EXCHG.80)
ms:contentKeyID: 27341526
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# È stata restituita una risposta HTTP 403.4 in quanto si richiedeva SSL sulla directory virtuale

 

***Ultima modifica dell'argomento:** 2011-01-21*

L'analizzatore di Microsoft Exchange tenta di eseguire la connessione e l'autenticazione presso il sito Web o la directory virtuale usando le credenziali e il protocollo forniti dall'utente. Se si tenta di eseguire la connessione con un protocollo non sicuro, la prova potrebbe avere esito negativo e restituire il seguente errore.

"È stata restituita una risposta HTTP 403.4 in quanto si richiedeva SSL sulla directory virtuale."

Questo problema si verifica se si tenta di eseguire una connessione utilizzando un protocollo non sicuro (HTTP), ma il server supporta solo connessioni HTTPS SSL (Secure Sockets Layer). Il caso più frequente in cui si verifica questo problema è quando si cerca di connettersi a un sito Web o a una directory virtuale utilizzando un protocollo HTTP invece che HTTPS.

## Per ulteriori informazioni

Per correggere questo errore, effettuare una delle seguenti operazioni:

  - Utilizzare il protocollo HTTPS per accedere al sito Web. In altre parole, verificare che l'URL inizi con "https://".  
  - Nelle impostazioni SSL per il sito Web, deselezionare la casella di controllo Richiedi SSL. Per fare ciò, procedere nel seguente modo.  

Per Windows 2003:

1.  Fare clic su **Start**, **Esegui**, digitare Inetmgr e quindi fare clic su **OK**.  
2.  In Gestione IIS (Internet Information Services), espandere Nome\_computer, espandere Siti Web e quindi fare clic con il pulsante destro del mouse sul sito Web da cui si desidera rimuovere la funzionalità SSL.  
3.  Fare clic su **Proprietà**.  
4.  Selezionare la scheda Protezione.  
5.  In Comunicazioni protette, fare clic sul pulsante **Modifica**.  
6.  Deselezionare le seguenti caselle di controllo:  
      - Richiedi un canale protetto per l'accesso a questa risorsa  
      - Richiedi crittografia a 128 bit  
7.  Fare clic su OK.  

Per Windows 2008:

1.  Fare clic su **Start**, **Esegui**, digitare Inetmgr e quindi fare clic su **OK**.  
2.  In Gestione IIS (Internet Information Services), espandere Nome\_computer, espandere Siti e quindi fare clic sul sito Web da cui si desidera rimuovere la funzionalità SSL.  
3.  Nel riquadro centrale della finestra, fare doppio clic su Impostazioni SSL.  
4.  Deselezionare le seguenti caselle di controllo:  
      - Richiedi un canale protetto per l'accesso a questa risorsa  
      - Richiedi crittografia a 128 bit  
5.  Fare clic su **Applica** nel riquadro a destra.  

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

