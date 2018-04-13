---
title: Risposta XML non valida, impossibile recuperare le impostazioni di disponibilità o fuori sede
TOCTitle: Risposta XML non valida, impossibile recuperare le impostazioni di disponibilità o fuori sede
ms:assetid: 30bf8fea-d51f-4b7e-a964-66877cd4ce10
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Ee410520(v=EXCHG.80)
ms:contentKeyID: 27341533
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Risposta XML non valida, impossibile recuperare le impostazioni di disponibilità o fuori sede

 

***Ultima modifica dell'argomento:** 2009-08-18*

L'analizzatore di Microsoft Exchange invia delle richieste XML/HTTP GetUserOofSettings e GetUserAvailability al servizio Servizi Web Exchange utilizzando l'API di Servizi Web Exchange per verificare le operazioni utilizzate dalle applicazioni personalizzate e dai client Exchange. Quando nella risposta è presente un XML non valido, l'Analizzatore connettività remota di Exchange visualizza il seguente messaggio di errore.

"Risposta XML non valida, impossibile recuperare le impostazioni di disponibilità o fuori sede."

L'Analizzatore connettività remota di Exchange utilizza l'[operazione GetUserOofSettings](http://go.microsoft.com/fwlink/?linkid=85951) e l'[operazione GetUserAvailability](http://go.microsoft.com/fwlink/?linkid=85950) per recuperare, rispettivamente, le impostazioni di fuori sede e di disponibilità nel calendario di un utente. Queste operazioni vengono utilizzate dai client (ad esempio, Microsoft Office Outlook 2007) così come dalle applicazioni personalizzate.

## Per ulteriori informazioni

Per correggere questo errore, vedere "Outlook 2007 si blocca o non è possibile accedere alle impostazioni di fuori sede dopo l'installazione di un pacchetto che contiene .NET Framework 3.5 con SP1 e .NET Framework 2.0 con SP2 su un server Accesso client Exchange 2007" ([http://go.microsoft.com/fwlink/?linkid=3052\&kbid=958934](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=958934)).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

