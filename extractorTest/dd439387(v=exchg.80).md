---
title: Ricevuto errore HTTP 403 perché il server ISA ha negato l'URL specificato
TOCTitle: Ricevuto errore HTTP 403 perché il server ISA ha negato l'URL specificato
ms:assetid: b4a20f57-ae2c-4526-83e8-5a179066ae96
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439387(v=EXCHG.80)
ms:contentKeyID: 27341591
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Ricevuto errore HTTP 403 perché il server ISA ha negato l'URL specificato

 

_**Ultima modifica dell'argomento:** 2009-11-17_

L'analizzatore di Microsoft Exchange invia una richiesta HTTP e convalida la risposta ricevuta per verificare la connettività. Se il punto di ingresso a Server Exchange è un server ISA e le regole di pubblicazione sul server ISA non sono configurate correttamente, ISA potrebbe inviare una risposta HTTP 403 non consentita. Se ISA invia una risposta HTTP 403, lo strumento connettività remota di Microsoft Exchange visualizza il seguente messaggio:

"Il server ha rifiutato l'Uniform Resource Locator (URL) specificato."

Gli utenti finali non potranno connettersi alle applicazioni e ai servizi Exchange.

## Per ulteriori informazioni

I motivi di questo errore potrebbero essere molteplici, ma il più probabile potrebbe essere un server ISA non configurato correttamente.


> [!NOTE]
> Se si utilizza ISA 2000, si raccomanda di aggiornare a ISA 2006. Se non è possibile effettuare l'aggiornamento, sulla regola di pubblicazione sul Web OWA è necessario rimuovere tutte le voci Path e sostituirle solo con "/*".



**Per correggere questo errore**

1.  Seguire la procedura riportata nell'articolo della Microsoft Knowledge Base, "Pubblicazione di un server Microsoft Exchange per Outlook Web Access in ISA Server 2006 o in ISA Server 2004" ([http://go.microsoft.com/fwlink/?LinkID=3052\&kbid=837354](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=837354)).

2.  Se è stata applicata la procedura riportata nell'articolo precedente e si continua a ricevere lo stesso errore, vedere l'articolo della Microsoft Knowledge Base "Un utente non può accedere a un sito Web pubblicato in ISA Server 2006 utilizzando la delega vincolata Kerberos, se l'utente non si trova nello stesso dominio del computer ISA Server" ([http://go.microsoft.com/fwlink/?LinkId=3052\&kbid=942637](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=942637)) e "Messaggio di errore quando un utente visita il sito Web che viene pubblicata utilizzando Microsoft ISA Server con l'autenticazione dei certificati client: Codice errore: 403 negato" ([http://go.microsoft.com/fwlink/?LinkId=3052\&kbid=947124](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=947124)).

Se il punto di ingresso al Server Exchange è ISA Server 2006, controllare la regola di pubblicazione per stabilire se la regola è configurata per non consentire tutte le autenticazioni. Andare alla scheda Delega e visualizzare l'elenco a discesa sotto "Metodo utilizzato da ISA Server per autenticare il server Web pubblicato". L'opzione "Nessuna delega e Client possono essere autenticati direttamente" disabilita qualsiasi autenticazione sulla regola. Dato che tutti i servizi di Exchange richiedono un certo tipo di autenticazione, scegliere dal menu a discesa un metodo diverso di delega adatto al proprio ambiente.


> [!NOTE]
> Questo problema può anche essere legato a un problema relativo al set di destinazione. Verificare che il set di destinazione punti all'indirizzo IP esterno.



Esempio:

Nome set di destinazione: OWA

Descrizione: Outlook Web Access

SingleIP: \<IP interno del server Exchange\> (cambiare in IP esterno su ISA)

Path: /exchange\*

SingleIP: \<IP interno del server Exchange\> (cambiare in IP esterno su ISA)

Path: /exchweb\*

SingleIP: \<IP interno del server Exchange\> (cambiare in IP esterno su ISA)

Path: /public\*

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

