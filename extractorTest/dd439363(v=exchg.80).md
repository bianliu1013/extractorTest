---
title: Nessun record MX trovato per il dominio SMTP specificato
TOCTitle: Nessun record MX trovato per il dominio SMTP specificato
ms:assetid: 1309d583-594e-4a6f-9bd0-41834f86b115
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439363(v=EXCHG.80)
ms:contentKeyID: 27341524
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Nessun record MX trovato per il dominio SMTP specificato

 

***Ultima modifica dell'argomento:** 2009-11-18*

L'analizzatore di Microsoft Exchange esegue una ricerca in DNS per trovare un elenco dei record MX (Mail Exchanger) che corrispondono al dominio da verificare. Se nell'elenco restituito non sono presenti record MX, la verifica avrà esito negativo con il seguente messaggio di errore:  
  
"Nessun record MX trovato in DNS per il dominio SMTP (nome dominio)"

Se la zona DNS per il dominio non include record MX, la posta SMTP in ingresso potrebbe non essere recapitata correttamente per quel dominio SMTP.

La ricerca in DNS dei record MX per il dominio SMTP potrebbe avere esito negativo perché sul server DNS potrebbero non esserci record MX.

## Per ulteriori informazioni

**Per correggere questo errore**

1.  Utilizzare nslookup.exe per verificare che il record MX (Mail Exchanger) esista sul server DNS.

2.  Se il record di risorse MX non esiste, aggiungerlo manualmente. Se la zona DNS esterna si trova su un server host di terzi, potrebbe essere necessario contattare quella società o utilizzare strumenti personalizzati per apportare queste modifiche DNS.

Per informazioni sulla risoluzione dei problemi del DNS, vedere "Risoluzione dei problemi relativi al servizio DNS" all'indirizzo [http://go.microsoft.com/fwlink/?LinkId=63003](http://go.microsoft.com/fwlink/?linkid=63003).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

