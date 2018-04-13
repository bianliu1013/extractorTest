---
title: Il nome del certificato SSL di ADFS non corrisponde
TOCTitle: Il nome del certificato SSL di ADFS non corrisponde
ms:assetid: 71a8dad5-2f56-41c6-97e1-48c8bee3e4bd
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Hh241335(v=EXCHG.80)
ms:contentKeyID: 42607546
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Il nome del certificato SSL di ADFS non corrisponde

 

_**Ultima modifica dell'argomento:** 2011-06-06_

L'Analizzatore connettività remota di Microsoft Exchange interroga la piattaforma di autenticazione nel cloud per individuare l'area di autenticazione. Al termine del processo la piattaforma di autenticazione passa al client richiedente il nome dell'endpoint ADFS necessario per l'autenticazione del client. Tale endpoint è una connessione SSL (Secure Sockets Layer) dotata di certificato. Lo strumento valuta il nome di dominio completo (FQDN) assegnato al certificato (ad esempio, STS.Contoso.com).

Se il nome di dominio completo non corrisponde all'indirizzo o all'URL dell'host che il client utilizza per eseguire una connessione con il server, l'Analizzatore connettività remota di Microsoft Exchange restituisce l'avviso seguente.


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Nome certificato SSL non corrispondente</p></td>
</tr>
</tbody>
</table>


Un avviso di nome non corrispondente indica che gli utenti potrebbero non essere autenticati correttamente nelle relative risorse Office 365. Se si verifica questo problema, con la modalità di accesso passiva (Internet Explorer) ai servizi di Office 365 viene visualizzato un avviso relativo al certificato quando l'utente accede ai servizi. Il client passivo può stabilire la connessione solo se l'avviso relativo al certificato viene accettato. Il client Outlook non riceve questo avviso di sicurezza relativo al certificato e non riesce a stabilire la connessione.

## Ulteriori informazioni

Per informazioni su come risolvere questo problema, vedere l'articolo 2523494 della Microsoft Knowledge Base, [Quando si tenta di accedere alle risorse di Microsoft Office 365 utilizzando un account federato identità, viene visualizzato un avviso di certificato](http://support.microsoft.com/kb/2523494)

Per ulteriori informazioni sulla pianificazione per la federazione delle identità, vedere [Preparazione dell'accesso Single Sign-On](http://onlinehelp.microsoft.com/it-it/office365-enterprises/ff652540.aspx)

Per informazioni della Guida sull'aggiornamento dell'ambiente Exchange 2010 corrente, vedere [Assistente per la distribuzione di Exchange Server (in lingua inglese)](http://technet.microsoft.com/it-it/exdeploy2010/default.aspx).

