---
title: Errore HTTP 500 restituito a ISA perché il certificato sul server pubblicato non corrisponde al nome specificato nella regola di pubblicazione
TOCTitle: Errore HTTP 500 restituito a ISA perché il certificato sul server pubblicato non corrisponde al nome specificato nella regola di pubblicazione
ms:assetid: a19d636c-616d-4843-a48f-7b0dff02f0ef
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439382(v=EXCHG.80)
ms:contentKeyID: 27341578
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Errore HTTP 500 restituito a ISA perché il certificato sul server pubblicato non corrisponde al nome specificato nella regola di pubblicazione

 

_**Ultima modifica dell'argomento:** 2009-08-18_

L'analizzatore di Microsoft Exchange invia un richiesta HTTP(s) all'URL richiesto. Se si riceve una risposta HTTP 500 e la pagina riporta il codice di errore -2146893022, l'Analizzatore connettività remota di Microsoft Exchange Server restituisce il seguente errore:

"È stata restituita una risposta HTTP 500 a ISA, in quanto il certificato sul server pubblicato non corrisponde al nome nella regola di pubblicazione."

L'Analizzatore connettività remota di Microsoft Exchange Server genera un errore quando si usa Microsoft Internet Security e Acceleration (ISA) Server 2006 oppure ISA Server 2004 per pubblicare un sito Web che richiede una connessione SSL (Secure Sockets Layer) e la richiesta client SSL inviata da ISA Server non corrisponde al nome comune specificato nel certificato del sito Web. Il sintomo più comune si ha quando gli utenti ricevono il seguente messaggio quando tentano di connettersi al sito Web.

"Codice di errore 500 - Errore interno del server.  
Nome principale di destinazione non corretto. (-2146893022)."

## Soluzione

Controllare che i nomi dei certificati siano conformi alle seguenti specifiche:

  - Per il certificato sul computer ISA Server, il nome deve corrispondere al nome che i client esterni specificano per raggiungere il sito.  
  - Per il certificato sul server Web pubblicato, il nome deve corrispondere al nome che appare sulla scheda A della regola.  
  - Nel caso del certificato sul server Web in uno scenario di pubblicazione del server, il certificato deve avere il nome che gli utenti utilizzeranno per connettersi al server.  

Per la soluzione del problema, ottenere un nuovo certificato corrispondente al nome richiesto oppure modificare il nome richiesto in modo che corrisponda al nome comune del certificato. Inoltre, accertarsi che ISA Server possa risolvere il nome nell'indirizzo IP del sito Web pubblicato. Se si modifica il nome sulla scheda A, per assicurarsi che il nome possa essere risolto è possibile aggiungere una voce al file Hosts sul computer ISA Server (WINNT\\system32\\drivers\\etc\\hosts) per associare il nome e l'indirizzo IP del sito pubblicato.

## Per ulteriori informazioni

Per ulteriori informazioni su come risolvere i problemi relativi ai certificati SSL quando si utilizza ISA Server, vedere "[Soluzione dei problemi relativi ai certificati SSL nella pubblicazione su ISA Server 2004](http://go.microsoft.com/fwlink/?linkid=48904)."

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

