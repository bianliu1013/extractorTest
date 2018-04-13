---
title: Nessun metodo di autenticazione supportato trovato nella risposta
TOCTitle: Nessun metodo di autenticazione supportato trovato nella risposta
ms:assetid: ef9f2062-3376-42da-9bd1-a333278449b6
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439397(v=EXCHG.80)
ms:contentKeyID: 27341613
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Nessun metodo di autenticazione supportato trovato nella risposta

 

***Ultima modifica dell'argomento:** 2012-05-21*

L'analizzatore di Microsoft Exchange invia una richiesta HTTP per verificare i metodi di autenticazione del servizio specificato. Se riceve una risposta di mancata autorizzazione 401, l'Analizzatore connettività remota di Exchange si aspetta che nella risposta compaiano determinate intestazioni WWW-Authenticate. Queste intestazioni indicano i metodi di autenticazione supportati per il servizio. Se non vengono ricevute intestazioni WWW-Authenticate, l'Analizzatore connettività remota di Exchange genera il seguente messaggio di errore:

"Nessun metodo di autenticazione supportato trovato nella risposta"

Questo problema impedisce agli utenti il collegamento al servizio specificato.

## Per ulteriori informazioni

Per risolvere il problema, fare quanto segue:

1\. Verificare che siano selezionati i metodi di autenticazione adeguati per le directory virtuali in IIS.

  - Per vedere l'elenco dei metodi di autenticazione predefiniti per le applicazioni e i servizi di Exchange Server 2007, vedere [Impostazioni predefinite per le directory virtuali di Exchange in Exchange Server 2007](http://go.microsoft.com/fwlink/?linkid=161402) sul blog di Microsoft.  
  - Per informazioni sui metodi di autenticazione supportati disponibili per la gestione delle applicazioni di Exchange residenti su un server Accesso client di Exchange 2007, vedere [Gestione della protezione dell'accesso client](http://go.microsoft.com/fwlink/?linkid=100585).  
  - Per ulteriori informazioni sulla configurazione dell'autenticazione specifica per Outlook via Internet in Exchange 2007, vedere [Come configurare l'autenticazione per Outlook via Internet](http://go.microsoft.com/fwlink/?linkid=161403).  
  - Per informazioni sulla configurazione dell'autenticazione per le applicazioni Web su Exchange Server 2003 e Exchange 2000 Server, vedere [Guida alla topologia dei server front-end e back-end per Microsoft Exchange Server 2003 e Exchange 2000 Server](http://go.microsoft.com/fwlink/?linkid=161404).  

2\. Se il punto di ingresso al Server Exchange è ISA Server 2006, controllare la regola di pubblicazione per stabilire se la regola è configurata per non consentire tutte le autenticazioni. Andare alla scheda Delega e visualizzare l'elenco a discesa sotto "Metodo utilizzato da ISA Server per autenticare il server Web pubblicato". L'opzione "Nessuna delega e Client possono essere autenticati direttamente" disabilita qualsiasi autenticazione sulla regola. Dato che tutti i servizi di Exchange richiedono un certo tipo di autenticazione, scegliere dal menu a discesa un metodo diverso di delega adatto al proprio ambiente.

Per ulteriori informazioni sulla pubblicazione dei servizi Exchange 2007 tramite Microsoft ISA Server 2006, vedere [Utilizzo di ISA Server 2006 con Exchange 2007](http://go.microsoft.com/fwlink/?linkid=161829).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

