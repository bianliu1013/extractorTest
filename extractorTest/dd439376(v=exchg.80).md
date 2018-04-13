---
title: Il provider del servizio di individuazione automatica di MobileSync ha restituito uno stato di errore nella risposta XML
TOCTitle: Il provider del servizio di individuazione automatica di MobileSync ha restituito uno stato di errore nella risposta XML
ms:assetid: 7216a11c-7e3b-42b2-86d3-73a467780eb1
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439376(v=EXCHG.80)
ms:contentKeyID: 27341556
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Il provider del servizio di individuazione automatica di MobileSync ha restituito uno stato di errore nella risposta XML

 

_**Ultima modifica dell'argomento:** 2009-08-19_

L'analizzatore di Microsoft Exchange invia una richiesta XML/HTTP di individuazione automatica al servizio di individuazione automatica di Exchange utilizzando lo schema del provider di MobileSync per individuare le impostazioni del dispositivo mobile per l'utente specificato. Quando nella risposta è presente un messaggio di errore, l'Analizzatore connettività remota di Exchange visualizza il seguente messaggio di errore:

"Il provider del servizio di individuazione automatica di MobileSync ha restituito uno stato di errore nella risposta XML."

## Per ulteriori informazioni

Il provider di individuazione automatica di Exchange ActiveSync (MobileSync) può restituire i seguenti messaggi di errore:

  - "Active Directory non disponibile"  
  - "Impossibile trovare la cassetta postale per i dispositivi mobili"  
  - "Il servizio di individuazione automatica non è in grado di elaborare l'indirizzo di posta elettronica specificato. Solo le cassette postali e i contatti possono essere utilizzati per MobileSync."  
  - "Impossibile trovare l'indirizzo di posta elettronica"  

In Exchange Server 2007 è presente un problema noto che causa l'errore "Active Directory non disponibile" quando nei siti Active Directory sono presenti server Accesso client che non sono esposti a Internet. I server Accesso client esposti a Internet sono riconoscibili dalla presenza dell'attributo ExternalUrl sulla directory virtuale ActiveSync. Se l'attributo ExternalUrl non è impostato, il sever Accesso client (CAS) non viene considerato "esposto a Internet". Questo problema è stato corretto in Exchange 2007 SP1 RU4. Per ulteriori informazioni su questo specifico problema, vedere l'articolo della Microsoft Knowledge Base che illustra come il servizio di individuazione automatica per ActiveSync in un ambiente Exchange 2007 non funzioni correttamente per gli utenti in siti dove l'attributo ExternalURL non è impostato correttamente ([Il servizio di individuazione automatica per ActiveSync in un ambiente Exchange 2007 non funziona per gli utenti in siti dove l'attributo ExternalURL non è impostato correttamente](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=952152)).

Per ulteriori informazioni sui server Accesso client esposti o meno a Internet, vedere [Concetti relativi all'inoltro e al reindirizzamento](http://go.microsoft.com/fwlink/?linkid=105411).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

