---
title: All'indirizzo IP non corrisponde un record PTR nel DNS
TOCTitle: All'indirizzo IP non corrisponde un record PTR nel DNS
ms:assetid: 14280637-0bb4-42dd-8ecc-0f6802a4d16d
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Ff796197(v=EXCHG.80)
ms:contentKeyID: 34993392
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# All'indirizzo IP non corrisponde un record PTR nel DNS

 

***Ultima modifica dell'argomento:** 2011-01-25*

Lo strumento Microsoft Exchange Best Practices Analyzer esegue una ricerca DNS inversa (PTR) dell'indirizzo IP in uscita utilizzato per inviare messaggi di posta elettronica su Internet. Se non è possibile trovare una voce DNS per tale indirizzo IP, verrà generato il messaggio di errore seguente:

###  

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>L'indirizzo IP X.X.X.X non dispone di un record PTR in DNS</p></td>
</tr>
</tbody>
</table>

## Per ulteriori informazioni

Le zone di ricerca inversa hanno il formato seguente: inverso dell'indirizzo IP in notazione con punti.in-addr.arpa.

Se ad esempio si specifica A.B.C.D come indirizzo IP in uscita, il formato della query sarà D.C.B.A.in-addr.arpa. La query non trova alcuna voce nella zona di ricerca inversa del DNS.

In genere, le zone di ricerca inversa vengono gestite dall'ISP.

## Significato dell'errore per l'amministratore

Alcuni server di posta elettronica cercano un record inverso come procedura di controllo base per la protezione dalla posta indesiderata. È pertanto consigliabile creare un record inverso corrispondente al proprio record A. Tali server di posta elettronica possono rifiutare i messaggi provenienti dal dominio dell'utente oppure contrassegnare i messaggi come posta indesiderata se non riescono a individuare un record PTR valido per l'host che effettua l'invio.

Per ulteriori informazioni sulla ricerca DNS inversa, vedere i seguenti articoli nel sito Web degli strumenti di IETF (informazioni in lingua inglese):

<http://tools.ietf.org/html/rfc1912>

<http://tools.ietf.org/html/rfc2317>

L'Analizzatore connettività remota di Exchange è un nuovo strumento per cui è attualmente disponibile documentazione limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community in fondo a questa pagina per specificare ulteriori motivi per cui la ricerca inversa non è riuscita in questa fase. Se è necessaria assistenza tecnica, creare un post nel [forum TechNet per Microsoft Exchange Server](http://go.microsoft.com/fwlink/?linkid=73420) appropriato o contattare il [Servizio Supporto Tecnico Clienti Microsoft](http://go.microsoft.com/fwlink/?linkid=8158).

