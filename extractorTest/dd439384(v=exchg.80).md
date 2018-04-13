---
title: Impossibile trovare intestazione MS-Server-ActiveSync nella risposta OPTIONS
TOCTitle: Impossibile trovare intestazione MS-Server-ActiveSync nella risposta OPTIONS
ms:assetid: b13d5173-7491-4238-a513-6a7f2390aee3
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439384(v=EXCHG.80)
ms:contentKeyID: 27341584
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Impossibile trovare intestazione MS-Server-ActiveSync nella risposta OPTIONS

 

_**Ultima modifica dell'argomento:** 2009-08-18_

L'analizzatore di Microsoft Exchange invia una richiesta HTTP con il verbo OPTIONS alla directory virtuale Microsoft-Server-ActiveSync e analizza le intestazioni HTTP nella risposta. Se nella risposta HTTP manca l'intestazione MS-Server-ActiveSync, l'Analizzatore connettività remota di Exchange visualizza il seguente messaggio di errore:

"Impossibile trovare intestazione MS-Server-ActiveSync nella risposta OPTIONS."

Questo problema è in genere il risultato di un firewall o di un proxy inverso che non supporta il verbo OPTIONS o che non è configurato per inviarlo. Un'altra potenziale causa di questo problema è quando si installa URLScan e lo si configura per bloccare il verbo OPTIONS. In ogni caso, questo problema impedisce agli utenti di dispositivi mobili di connettersi a Exchange ActiveSync.

## Per ulteriori informazioni

Per correggere questo errore, effettuare una delle seguenti operazioni:

  - Se si utilizza Internet Security Acceleration (ISA) Server 2000, vedere l'articolo della Microsoft Knowledge Base "La risposta di ISA Server alle richieste di opzioni del client è limitata a un insieme predefinito" ([http://go.microsoft.com/fwlink/?linkid=3052\&kbid=304340](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=304340)).  
  - Se si utilizza un proxy inverso di terzi, contattare il produttore per verificare se il verbo OPTIONS è supportato o come configurarne il supporto.  
  - Per ulteriori informazioni sullo strumento URLScan, vedere l'articolo della Microsoft Knowledge Base "Come configurare lo strumento URLScan" ([http://go.microsoft.com/fwlink/?linkid=3052\&kbid=326444](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=326444)).  

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

