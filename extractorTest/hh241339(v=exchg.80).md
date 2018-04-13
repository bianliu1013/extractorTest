---
title: Nome utente sconosciuto o password errata
TOCTitle: Nome utente sconosciuto o password errata
ms:assetid: ae77f86b-1d8e-45e4-a751-b001b23a8e8f
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Hh241339(v=EXCHG.80)
ms:contentKeyID: 42607551
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Nome utente sconosciuto o password errata

 

***Ultima modifica dell'argomento:** 2011-06-06*

L'Analizzatore connettività remota di Microsoft Exchange interroga la piattaforma di autenticazione del cloud per simulare il processo di recupero dei token dal server ADFS locale. Per eseguire il test, è necessario digitare il nome utente e la password appropriati, in modo che lo strumento recuperi correttamente il token per conto dell'utente.

Se l'utente non viene autenticato correttamente, l'Analizzatore connettività remota visualizza l'avviso seguente:

###  

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Il servizio token di sicurezza ha indicato che l'autenticazione non è riuscita. Controllare nome utente e password e riprovare.</p></td>
</tr>
</tbody>
</table>

Tale messaggio indica un errore di accesso quando si tenta di eseguire l'autenticazione nell'endpoint ADFS. Questo evento può verificarsi per uno qualsiasi dei motivi seguenti:

  - Gli utenti hanno immesso una password errata  
  - Gli utenti hanno immesso un nome utente errato  
  - Il dominio configurato per la federazione delle identità non è impostato come UPN degli utenti  

Tali problemi possono essere risolti nello snap-in MMC Utenti e computer di Active Directory del sistema locale.

## Ulteriori informazioni

Per ulteriori informazioni sulla pianificazione per la federazione delle identità, vedere [Preparazione dell'accesso Single Sign-On](http://onlinehelp.microsoft.com/it-it/office365-enterprises/ff652540.aspx)

Per informazioni della Guida sull'aggiornamento dell'ambiente Exchange 2010 corrente, vedere [Assistente per la distribuzione di Exchange Server (in lingua inglese)](http://technet.microsoft.com/it-it/exdeploy2010/default.aspx).

