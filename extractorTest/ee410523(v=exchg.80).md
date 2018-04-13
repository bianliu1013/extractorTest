---
title: L'account del servizio specificato non dispone delle autorizzazioni di rappresentazione sull'account Act As specificato
TOCTitle: L'account del servizio specificato non dispone delle autorizzazioni di rappresentazione sull'account Act As specificato
ms:assetid: 847e2785-dfde-4810-84a9-a8aeb7efe29c
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Ee410523(v=EXCHG.80)
ms:contentKeyID: 27341561
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# L'account del servizio specificato non dispone delle autorizzazioni di rappresentazione sull'account Act As specificato

 

***Ultima modifica dell'argomento:** 2009-08-19*

L'analizzatore di Microsoft Exchange invia le richieste XML/HTTP al servizio Servizi Web Exchange con l'API Servizi Web Exchange. Quando queste richieste tentano di utilizzare Exchange Impersonation e nella risposta è presente un messaggio di errore, l'Analizzatore connettività remota di Exchange visualizza il seguente messaggio di errore.

"ErrorImpersonateUserDenied, questo codice di errore indica che l'account del servizio specificato non dispone dell'autorizzazione ms-Exch-EPI-May-Impersonate sull'account Act As che sta cercando di rappresentare"

L'Analizzatore connettività remota di Exchange utilizza l'intestazione SOAP [ExchangeImpersonation](http://go.microsoft.com/fwlink/?linkid=161948) di Servizi Web Exchange per specificare un account che deve essere rappresentato dall'account del servizio per verificare se l'account del servizio dispone delle autorizzazioni per rappresentare l'utente specificato con [ExchangeImpersonation](http://go.microsoft.com/fwlink/?linkid=161948) (noto anche come [Autorizzazione Server-to-Server](http://go.microsoft.com/fwlink/?linkid=161951)). L'account Act As è quello utilizzato da Exchange per autorizzare l'esecuzione dei comandi di Servizi Web Exchange; è l'account rappresentato.

## Per ulteriori informazioni

Per risolvere questo problema, all'account del servizio deve essere assegnata l'autorizzazione per rappresentare l'utente specificato. Per ulteriori informazioni, vedere [Configurazione di Exchange Impersonation (Servizi Web Exchange)](http://go.microsoft.com/fwlink/?linkid=161954).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

