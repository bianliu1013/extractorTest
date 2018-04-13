---
title: L'account Act As potrebbe non avere le autorizzazioni per accedere a questa cartella
TOCTitle: L'account Act As potrebbe non avere le autorizzazioni per accedere a questa cartella
ms:assetid: 38d72b1a-7cd0-42a2-ad0e-3007b434fd2c
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Ee410521(v=EXCHG.80)
ms:contentKeyID: 27341537
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# L'account Act As potrebbe non avere le autorizzazioni per accedere a questa cartella

 

_**Ultima modifica dell'argomento:** 2012-05-23_

L'analizzatore di Microsoft Exchange invia una richiesta XML/HTTP [GetFolder](http://go.microsoft.com/fwlink/?linkid=161956) al servizio Servizi Web Exchange utilizzando l'API di Servizi Web Exchange per ottenere le informazioni su una cartella di una cassetta postale o una cartella pubblica. Quando nella risposta è presente un messaggio di errore che indica che è stato negato l'accesso, l'Analizzatore connettività remota di Exchange visualizza il seguente messaggio di errore.

"L'account Act As potrebbe non avere le autorizzazioni per accedere a questa cartella."

L'Analizzatore connettività remota di Exchange utilizza l'operazione [GetFolder](http://go.microsoft.com/fwlink/?linkid=161956) di Servizi Web Exchange per ottenere le informazioni su una cartella di una cassetta postale o una cartella pubblica per verificare se l'account specificato dispone delle autorizzazioni per leggere i dati della cartella, incluso il numero di elementi in essa contenuti.

L'account Act As è quello utilizzato da Exchange per autorizzare l'esecuzione dei comandi di Servizi Web Exchange. Nella maggior parte dei casi, si tratta dell'account che invia le richieste a Servizi Web Exchange. Tuttavia, se si utilizza [ExchangeImpersonation](http://go.microsoft.com/fwlink/?linkid=161948) (noto anche come [Autorizzazione Server-to-Server](http://go.microsoft.com/fwlink/?linkid=161951)), l'account rappresentato è Act As.

## Per ulteriori informazioni

Per risolvere questo problema, l'account Act As deve disporre delle autorizzazioni per leggere le informazioni per la cartella specificata. Per assegnare all'account Act As le autorizzazioni appropriate, fare quanto segue:

1.  Assegnare all'account Act As le autorizzazioni complete sulle cassette postali per la cartella utilizzando il comando [Add-MailboxPermission](http://go.microsoft.com/fwlink/?linkid=76497). In alternativa, vedere [Come consentire l'accesso a una cassetta postale](http://go.microsoft.com/fwlink/?linkid=76535).  
2.  Assegnare all'account Act As le autorizzazioni per leggere gli elementi nella cartella pubblica utilizzando il comando [Add-PublicFolderClientPermission](http://go.microsoft.com/fwlink/?linkid=123666). Inoltre, vedere [Configurazione delle autorizzazioni per le cartelle pubbliche](http://go.microsoft.com/fwlink/?linkid=161967).  
3.  Assegnare all'account Act As le autorizzazioni per leggere gli elementi nella cartella pubblica o cassetta postale specificata in Outlook modificando le [autorizzazioni per la cartella di Outlook](http://go.microsoft.com/fwlink/?linkid=86319).  

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

