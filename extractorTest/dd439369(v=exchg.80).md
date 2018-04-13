---
title: Il formato dell'URL esterno di ActiveSync non è quello previsto
TOCTitle: Il formato dell'URL esterno di ActiveSync non è quello previsto
ms:assetid: 33a8eb0f-4dfd-4b4d-a79a-f2e7c0740a43
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439369(v=EXCHG.80)
ms:contentKeyID: 27341535
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Il formato dell'URL esterno di ActiveSync non è quello previsto

 

***Ultima modifica dell'argomento:** 2009-09-01*

L'analizzatore di Microsoft Exchange invia una richiesta HTTP al provider del servizio di individuazione automatica MobileSync sul server Accesso client per ottenere un URL esterno per i dispositivi ActiveSync da utilizzare nella connessione a Exchange. Il formato di questo URL deve essere https://{nomehost}/Microsoft-Server-ActiveSync (dove {nomehost} è il nome di dominio completo (FQDN) del DNS esterno usato dai dispostivi mobili per connettersi ad Exchange ActiveSync). Quando l'URL restituito non ha il formato previsto, l'Analizzatore connettività remota di Exchange visualizza il seguente messaggio di errore.

"Formato URL di ActiveSync non valido. Dovrebbe essere https://host/Microsoft-Server-ActiveSync. L'URL era \<URL visualizzato\>."

## Per ulteriori informazioni

Per risolvere il problema, verificare l'impostazione ExternalUrl sulla directory virtuale Microsoft-Server-ActiveSync in Exchange Management Console.

1.  Espandere il nodo Configurazione server.  
2.  Selezionare il nodo Accesso client.  
3.  Selezionare il server Accesso client appropriato.  
4.  Selezionare la scheda Exchange ActiveSync.  
5.  Selezionare la directory virtuale Microsoft-Server-ActiveSync.  
6.  Fare clic su Proprietà per la directory virtuale.  
7.  Verificare che il formato dell'URL esterno sia: https://host/Microsoft-Server-ActiveSync.  

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

