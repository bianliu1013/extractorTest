---
title: Impossibile trovare tutti i metodi di autenticazione richiesti
TOCTitle: Impossibile trovare tutti i metodi di autenticazione richiesti
ms:assetid: 8b5d0ae9-fa46-498f-8d90-94e9195388c6
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439378(v=EXCHG.80)
ms:contentKeyID: 27341563
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Impossibile trovare tutti i metodi di autenticazione richiesti

 

***Ultima modifica dell'argomento:** 2009-11-18*

L'analizzatore di Microsoft Exchange invia una richiesta HTTP per verificare i metodi di autenticazione del servizio specificato. Se riceve una risposta di mancata autorizzazione 401, l'Analizzatore connettività remota di Exchange si aspetta che nella risposta compaiano determinate intestazioni WWW-Authenticate. Alcuni servizio quali Exchange ActiveSync e Outlook via Internet (RPC su HTTP) non negoziano alcun metodo di autenticazione con il server remoto. Questi client dispongono di un metodo di autenticazione predefinito che viene inviato con ciascuna richiesta. Se il metodo di autenticazione non è abilitato sul server remoto, l'Analizzatore connettività remota di Exchange genera il seguente messaggio di errore:

"Impossibile trovare tutti i metodi di autenticazione richiesti."

Se il metodo di autenticazione predefinito non è abilitato sul server remoto, si potrebbero verificare i seguenti problemi:

  - Gli utenti con dispositivi mobili che utilizzano Exchange ActiveSync non possono connettersi.  
  - Gli utenti di Microsoft Office Outlook potrebbero non essere in grado di connettersi usando Outlook via Internet.  

## Per ulteriori informazioni

**Per correggere questo errore**

1.  Verificare che l'autenticazione di base sia abilitata sulla directory virtuale di Exchange ActiveSync in Exchange Management Console e in IIS sulla directory virtuale di Microsoft-Server-ActiveSync

2.  Per gli utenti di Outlook via Internet, verificare le seguenti impostazioni per server e client:
    
    1.  Verificare che l'autenticazione Windows integrata e/o l'autenticazione di base siano abilitate sulla directory virtuale /Rpc in IIS. Notare che questi metodi di autenticazione devono essere gestiti tramite il cmdlet Set-OutlookAnywhere e non direttamente in IIS.  

3.  Verificare che l'autenticazione di base o l'autenticazione NTLM (NT LAN Manager) sia selezionata in Impostazioni proxy Exchange in Microsoft Outlook. Questa impostazione deve corrispondere al metodo di autenticazione abilitato in IIS. Se questa impostazione è stata ottenuta tramite il servizio di identificazione automatica, verificare che il metodo ClientAuthenticationMethod o DefaultAuthenticationMethod sia specificato correttamente nella configurazione di Outlook via Internet.

Per ulteriori informazioni, fare riferimento alla seguente documentazione e verificare che nelle directory virtuali sul server Exchange siano stati abilitati i metodi di autenticazione corretti per ogni applicazione o servizio:

  - Per vedere l'elenco dei metodi di autenticazione predefiniti per le applicazioni e i servizi di Exchange Server 2007, fare riferimento al post [Impostazioni predefinite per le directory virtuali di Exchange in Exchange Server 2007](http://go.microsoft.com/fwlink/?linkid=161402) sul blog di Microsoft.  
  - Per informazioni sui metodi di autenticazione supportati disponibili per la gestione delle applicazioni di Exchange residenti su un server Accesso client di Exchange 2007, vedere [Gestione della protezione dell'accesso client](http://go.microsoft.com/fwlink/?linkid=100585).  
  - Per i dettagli sulla configurazione dell'autenticazione specifica per Outlook via Internet in Exchange 2007, fare riferimento alla seguente documentazione su TechNet: [Come configurare l'autenticazione per Outlook via Internet](http://go.microsoft.com/fwlink/?linkid=161403).  
  - Per informazioni sulla configurazione dell'autenticazione per le applicazioni Web su Exchange Server 2003 e Exchange 2000 Server, vedere [Guida alla topologia dei server front-end e back-end per Microsoft Exchange Server 2003 e Exchange 2000 Server](http://go.microsoft.com/fwlink/?linkid=161404).  

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

