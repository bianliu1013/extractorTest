---
title: Autenticazione anonima abilitata per la directory virtuale
TOCTitle: Autenticazione anonima abilitata per la directory virtuale
ms:assetid: ed0d4b63-43b8-4a06-bb01-ee7ec1fd9650
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439395(v=EXCHG.80)
ms:contentKeyID: 27341611
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Autenticazione anonima abilitata per la directory virtuale

 

***Ultima modifica dell'argomento:** 2009-08-18*

L'analizzatore di Microsoft Exchange invia una richiesta HTTP anonima dal server remoto all'URL in fase di verifica. Se la richiesta ha esito positivo, ma l'accesso anonimo non è consentito a questa directory virtuale, l'Analizzatore connettività remota di Exchange visualizza il seguente messaggio di errore.

"Autenticazione anonima abilitata per la directory virtuale".

Outlook Web Access, Exchange ActiveSync, Outlook via Internet o RPC su HTTPS, Individuazione automatica e altri Servizi Web Exchange incluso Servizio Disponibilità e Rubrica offline distribuite su Web necessitano di specifici metodi di autenticazione. Se l'accesso anonimo è consentito in sostituzione o in aggiunta ad altri metodi di autenticazione richiesti, il server non è sicuro e potrebbero verificarsi dei risultati inaspettati.

## Per ulteriori informazioni

Per risolvere questo problema, fare riferimento alla seguente documentazione e verificare che nelle directory virtuali sul server Exchange siano stati abilitati i metodi di autenticazione corretti per ogni applicazione o servizio.

  - Per vedere l'elenco dei metodi di autenticazione predefiniti per le applicazioni e i servizi di Exchange Server 2007, vedere [Impostazioni predefinite per le directory virtuali di Exchange in Exchange Server 2007](http://go.microsoft.com/fwlink/?linkid=161402) sul blog di Microsoft.  
  - Per informazioni sui metodi di autenticazione supportati disponibili per gestire le applicazioni Exchange presenti su un server Accesso client di Exchange 2007, fare riferimento alla seguente documentazione su TechNet: [Gestione della protezione dell'accesso client](http://go.microsoft.com/fwlink/?linkid=100585).  
  - Per ulteriori informazioni sulla configurazione dell'autenticazione specifica per Outlook via Internet in Exchange 2007, vedere [Come configurare l'autenticazione per Outlook via Internet](http://go.microsoft.com/fwlink/?linkid=161403).  
  - Per informazioni sulla configurazione dell'autenticazione per le applicazioni Web su Exchange Server 2003 e Exchange 2000 Server, vedere [Guida alla topologia dei server front-end e back-end per Microsoft Exchange Server 2003 e Exchange 2000 Server](http://go.microsoft.com/fwlink/?linkid=161404).  

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

