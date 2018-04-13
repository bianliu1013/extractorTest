---
title: L'indirizzo IP è stato trovato in un elenco di indirizzi bloccati
TOCTitle: L'indirizzo IP è stato trovato in un elenco di indirizzi bloccati
ms:assetid: 44b89c4f-e186-4b21-8a92-7edecf5d3c2a
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Ff796198(v=EXCHG.80)
ms:contentKeyID: 34993393
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# L'indirizzo IP è stato trovato in un elenco di indirizzi bloccati

 

***Ultima modifica dell'argomento:** 2012-03-26*

Microsoft Exchange Best Practices Analyzer Tool confronta l'indirizzo IP in uscita con vari elenchi di indirizzi bloccati in tempo reale, nell'ambito del test SMTP in uscita. Se l'indirizzo IP specificato viene trovato in uno o più elenchi di indirizzi bloccati, viene visualizzato il messaggio di errore seguente:

###  

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>L'indirizzo IP X.X.X.X è stato trovato nell'elenco Blocca. Codice di stato: X</p></td>
</tr>
</tbody>
</table>

## Per ulteriori informazioni

Gli elenchi di indirizzi bloccati sono noti anche come elenchi di blocco basati su DNS o elenchi blackhole, perché sono basati sul noto protocollo DNS. Gli elenchi di indirizzi bloccati sono elenchi di indirizzi IP pubblicati tramite DNS e considerati origini note di posta indesiderata, attivamente, a causa di una configurazione non corretta, a causa di un'infezione dovuta a malware o per altri motivi.

Su Internet esistono molte entità che pubblicano e aggiornano tali elenchi per consentire agli utenti di difendersi dalla posta indesiderata. Tali elenchi possono essere tuttavia individuati involontariamente.

Nell'ambito del test SMTP in uscita l'Analizzatore connettività remota di Exchange (ExRCA) confronta l'indirizzo IP dell'utente con alcuni elenchi di indirizzi bloccati noti per verificare se è incluso. Se l'indirizzo IP dell'utente è incluso nell'elenco, ExRCA restituisce un messaggio di errore simile a quello riportato nella sezione introduttiva. Tale messaggio include il nome dell'elenco di indirizzi bloccati e il codice di stato.

I server di elenchi di indirizzi bloccati restituiscono in genere un codice di errore sotto forma di indirizzo di loopback, ad esempio 127.0.0.2. L'ultimo ottetto dell'indirizzo di loopback definisce il codice di errore, che in questo caso è "2". Il significato dei codici varia in base al provider di elenchi di indirizzi bloccati. Per determinare il significato esatto del codice, è necessario cercarlo nel sito Web del provider di elenchi. È necessario visitare il sito Web del provider anche per richiedere la rimozione del proprio indirizzo dall'elenco di indirizzi bloccati.

I tipi di codici includono i seguenti:

  - **127.0.0.2** - server di inoltro aperto conosciuto  
  - **127.0.0.3** - indirizzo generato da connessione remota o DHCP  

## Significato dell'errore per l'amministratore

Molti server di posta elettronica utilizzano noti elenchi di indirizzi bloccati come unica difesa contro la posta indesiderata. Se l'indirizzo IP del computer Exchange Server in uso compare in uno degli elenchi di indirizzi bloccati a cui è sottoscritto il server di destinazione, i messaggi di posta elettronica provenienti dal proprio dominio potrebbero essere rifiutati o contrassegnati come posta indesiderata. Questo è il motivo per cui ExRCA tenta di individuare gli indirizzo IP immessi dall'utente in uno o più elenchi di indirizzi bloccati noti.

Per alcuni esempi di elenchi di indirizzi bloccati noti, visitare i siti Web seguenti (in lingua inglese):

  - <http://www.dnsbl.info/dnsbl-details.php?dnsbl=pbl.spamhaus.org>  
  - <http://www.au.sorbs.net/>  
  - <http://www.spamcop.net/>  

Per ulteriori informazioni sugli elenchi di indirizzi bloccati, vedere [Configurazione dei filtri e controllo della posta indesiderata](http://technet.microsoft.com/it-it/library/aa997261\(exchg.65\).aspx) e visitare il seguente sito Web di collegamenti relativi alla posta indesiderata:

  - <http://spamlinks.net/filter-dnsbl-lists.htm>

