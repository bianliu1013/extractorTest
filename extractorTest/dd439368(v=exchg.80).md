---
title: Impossibile risolvere il nome host in DNS
TOCTitle: Impossibile risolvere il nome host in DNS
ms:assetid: 2d3fbf36-47f3-4a7b-ab7f-4f426c070991
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439368(v=EXCHG.80)
ms:contentKeyID: 27341529
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Impossibile risolvere il nome host in DNS

 

_**Ultima modifica dell'argomento:** 2011-11-09_

L'Analizzatore Microsoft esegue una ricerca DNS (Domain Name System) per recuperare il record host (A) per il nome host specificato. Se la ricerca in DNS non restituisce un indirizzo IP, l'Analizzatore connettività remota di Exchange visualizza il seguente messaggio di errore:

"Impossibile risolvere il nome host in DNS."

## Per ulteriori informazioni

Per correggere l'errore, fare quanto segue.

  - Utilizzare nslookup per verificare che il record Host (A) esista sul server DNS. Per ulteriori informazioni, vedere [Per verificare l'esistenza di record di risorse A nel sistema DNS](http://go.microsoft.com/fwlink/?linkid=63001).  
  - Se il record di risorse Host (A) non esiste o non è corretto, aggiungerlo o modificarlo manualmente. Se la zona DNS esterna si trova su un server host di terzi, potrebbe essere necessario contattare quella società o utilizzare strumenti personalizzati per apportare queste modifiche DNS.  

Per ulteriori informazioni sulla risoluzione dei problemi del servizio DNS, vedere la [Risoluzione dei problemi relativi al servizio DNS](http://go.microsoft.com/fwlink/?linkid=63003).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

In alcuni casi è necessario verificare l'URL utilizzato dall'endpoint ADFS per la federazione delle identità di Office 365. Per la procedura da seguire per determinare il valore su cui è attualmente impostato l'endpoint, vedere la sezione "Ulteriori informazioni" dell'articolo [Impossibile visualizzare la pagina Web del portale Office 365 in Internet Explorer quando un utente federato tenta di accedere](http://support.microsoft.com/kb/2419389).

