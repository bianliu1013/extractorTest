---
title: Il server Active Directory Federation Services (ADFS) è inattivo o irraggiungibile
TOCTitle: Il server Active Directory Federation Services (ADFS) è inattivo o irraggiungibile
ms:assetid: 0e1b8934-b061-4763-b735-704b58dabeb5
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Hh241329(v=EXCHG.80)
ms:contentKeyID: 42607541
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Il server Active Directory Federation Services (ADFS) è inattivo o irraggiungibile

 

_**Ultima modifica dell'argomento:** 2011-06-06_

L'Analizzatore connettività remota di Microsoft Exchange interroga la piattaforma di autenticazione nel cloud utilizzando la federazione delle identità per simulare l'autenticazione nell'ambiente di Office 365. In alcuni casi, il server ADFS può risultare completamente irraggiungibile, ad esempio se i servizi ADFS subiscono un arresto anomalo o non possono essere avviati. Se si verifica questo problema, viene visualizzato un messaggio simile al seguente:


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Recupero di informazioni sui metadati di ADFS dall'URL di scambio metadati https://sts.Contoso.com/adfs/services/trust/mex</p></td>
</tr>
<tr class="even">
<td><p>Impossibile recuperare i metadati di ADFS.</p></td>
</tr>
<tr class="odd">
<td><p>Ulteriori dettagli</p></td>
</tr>
<tr class="even">
<td><p>Si è verificata un'eccezione Web in quanto è stata ricevuta una risposta HTTP 503 - ServiceUnavailable da Sconosciuto.</p></td>
</tr>
</tbody>
</table>


Se viene restituito questo errore, esaminare i servizi ADFS sul server ADFS e sul proxy ADFS. Se non è possibile avviare i servizi su uno dei server, viene generato lo stesso messaggio di errore. In tale caso, è necessario ricercare la causa dell'errore del servizio esaminando i registri eventi. Se non è possibile avviare i servizi e la causa dell'errore non è indicata nei registri, è necessario chiamare il supporto tecnico.

## Ulteriori informazioni

Per ulteriori informazioni sulla pianificazione per la federazione delle identità, vedere [Preparazione dell'accesso Single Sign-On](http://onlinehelp.microsoft.com/it-it/office365-enterprises/ff652540.aspx)

Per informazioni della Guida sull'aggiornamento dell'ambiente Exchange 2010 corrente, vedere [Assistente per la distribuzione di Exchange Server (in lingua inglese)](http://technet.microsoft.com/it-it/exdeploy2010/default.aspx).

