---
title: Exchange ActiveSync ha restituito l'errore HTTP 451
TOCTitle: Exchange ActiveSync ha restituito l'errore HTTP 451
ms:assetid: 523005ac-9c43-438d-ba56-a7af11975084
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439372(v=EXCHG.80)
ms:contentKeyID: 27341547
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Exchange ActiveSync ha restituito l'errore HTTP 451

 

***Ultima modifica dell'argomento:** 2009-08-18*

L'analizzatore di Microsoft Exchange invia un comando Exchange ActiveSync FolderSync all'URL specificato. Se il server invia il codice HTTP 451, l'Analizzatore connettività remota di Microsoft Exchange Server restituisce il seguente errore.

"Exchange ActiveSync ha restituito una risposta HTTP 451. (Dispositivo non configurato correttamente)."

## Per ulteriori informazioni

Exchange 2007 restituisce una risposta HTTP 451 al client Exchange ActiveSync quando rileva che il dispositivo dovrebbe utilizzare un server Accesso client "migliore" per la connettività ActiveSync. La logica utilizzata per stabilire se un server Accesso client è quello "migliore" per un dispositivo si basa sui siti Active Directory e sul fatto se un server Accesso client è considerato esposto a Internet. Se viene specificata la proprietà ExternalUrl nella directory virtuale Microsoft-Server-ActiveSync, il server Accesso client è considerato esposto a Internet per la connettività Microsoft ActiveSync.

Se la cassetta postale utente da verificare non si trova nello stesso sito Active Directory del server Accesso client a cui si accede, potrebbe esservi un server Accesso client nel sito con il server di posta elettronica che ha la proprietà ExternalUrl impostata. Se si tenta di configurare ActiveSync come proxy da un sito esposto a Internet a un secondo sito (Intranet), accertarsi che la proprietà ExternalUrl non sia impostata nella directory virtuale Microsoft-Server-ActiveSync nel sito Intranet.

Per ulteriori informazioni sulla configurazione dei server Accesso client per proxy e reindirizzamento, vedere [Concetti relativi all'inoltro e al reindirizzamento](http://go.microsoft.com/fwlink/?linkid=105411).

Se vi sono più server Accesso client nello stesso sito Active Directory come server Accesso client da verificare, accertarsi che il parametro ExternalUrl sia impostato su ciascuna delle directory virtuali Microsoft-Server-ActiveSync. Se la proprietà ExternalUrl manca dal server Accesso client da verificare, potrebbe verificarsi questo errore.

Per ulteriori informazioni sull'impostazione dell'attributo ExternalUrl nella directory virtuale ActiveSync, vedere [Set-ActiveSyncVirtualDirectory](http://go.microsoft.com/fwlink/?linkid=161796).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

