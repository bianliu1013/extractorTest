---
title: Rilevato un metodo di autenticazione non supportato
TOCTitle: Rilevato un metodo di autenticazione non supportato
ms:assetid: 1260976c-1b9f-4eae-b805-94fabcc4d39c
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439361(v=EXCHG.80)
ms:contentKeyID: 27341514
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Rilevato un metodo di autenticazione non supportato

 

_**Ultima modifica dell'argomento:** 2009-08-18_

L'analizzatore di Microsoft Exchange invia una richiesta HTTP GET per verificare i metodi di autenticazione del servizio specificato utilizzando l'URL immesso durante la prova. Quando Exchange Server riceve la richiesta, risponde con un elenco di metodi di autenticazione accettati. L'elenco è contenuto nel campo WWW-Authenticate dell'intestazione della risposta. Se in questo elenco è riportato un metodo di autenticazione non supportato, potrebbe essere visualizzato il seguente messaggio di errore:

"Il metodo di autenticazione "0" è abilitato, ma non è un metodo di autenticazione consentito per questo servizio."

Dove "0" indica il metodo o i metodi di autenticazione non supportati che sono stati trovati.

Questo errore impedisce agli utenti di connettersi al servizio specificato.

## Per ulteriori informazioni

Il motivo principale per cui viene segnalato questo errore è quando si esegue la verifica Exchange ActiveSync e Autenticazione integrata di Windows è annunciata dal server. Autenticazione integrata di Windows non è un metodo di autenticazione supportato per Exchange ActiveSync e può impedire ai dispositivi Windows Mobile precedenti a Windows Mobile 6.0 di connettersi.


> [!NOTE]
> Se si utilizza ISA Server per eseguire la preautenticazione, Autenticazione integrata potrebbe essere abilitata su Listener Web. Se non si prevede di supportare dispositivi precedenti a Windows Mobile 6.0 (o se non si riscontrano problemi), questo errore può essere ignorato.



**Per correggere questo errore**

1.  Verificare che siano selezionati i metodi di autenticazione adeguati per le directory virtuali in IIS.

2.  Per vedere l'elenco dei metodi di autenticazione predefiniti per le applicazioni e i servizi di Exchange Server 2007, vedere [Impostazioni predefinite per le directory virtuali di Exchange in Exchange Server 2007](http://go.microsoft.com/fwlink/?linkid=161402)

3.  Per informazioni sui metodi di autenticazione supportati disponibili per la gestione delle applicazioni di Exchange residenti su un server Accesso client di Exchange 2007, vedere [Gestione della protezione dell'accesso client](http://go.microsoft.com/fwlink/?linkid=100585).

4.  Per ulteriori informazioni sulla configurazione dell'autenticazione specifica per Outlook via Internet in Exchange 2007, vedere [Come configurare l'autenticazione per Outlook via Internet](http://go.microsoft.com/fwlink/?linkid=161403).

5.  Per ulteriori informazioni sulla configurazione dell'autenticazione per le applicazioni Web su Exchange Server 2003 e Exchange 2000 Server, vedere [Guida alla topologia dei server front-end e back-end per Exchange Server 2003 ed Exchange 2000 Server](http://go.microsoft.com/fwlink/?linkid=161404).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

