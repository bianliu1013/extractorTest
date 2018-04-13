---
title: Impossibile trovare una corrispondenza per il nome nell'elenco indirizzi
TOCTitle: Impossibile trovare una corrispondenza per il nome nell'elenco indirizzi
ms:assetid: 2268f80c-4f96-4612-85ee-99b5a0322f5d
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439366(v=EXCHG.80)
ms:contentKeyID: 27341527
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Impossibile trovare una corrispondenza per il nome nell'elenco indirizzi

 

***Ultima modifica dell'argomento:** 2009-08-18*

L'analizzatore di Microsoft Exchange utilizza le informazioni utente fornite e invia una richiesta NSPI ResolveNames (verifica nome) a Exchange Server (usando RPC su HTTP) per tentare di risolvere l'account utente nella rubrica. Se non vengono trovate elementi corrispondenti, l'Analizzatore connettività remota di Exchange visualizza il seguente messaggio di errore.

"Impossibile trovare una corrispondenza per il nome nell'elenco indirizzi."

Generalmente, questo problema si verifica quando l'account utente non è associato ad alcuna cassetta postale o è stato configurato maualmente in modo che risultasse nascosto dall'elenco indirizzi globale. Altre possibili cause sono la mancanza di autorizzazioni Active Directory per alcuni oggetti o problemi a livello di Servizio aggiornamento dei destinatari di Exchange. Oltre al precedente errore, gli utenti finali potrebbero non essere in grado di eseguire una verifica del nome, creare un profilo MAPI o connettersi a un server Exchange.

## Per ulteriori informazioni

Per risolvere questo problema, vedere l'articolo della Microsoft Knowledge Base che illustra come risolvere gli errori relativi alla verifca del nome ([http://go.microsoft.com/fwlink/?linkid=3052\&kbid=297801](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=297801)).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

