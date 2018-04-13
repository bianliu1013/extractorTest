---
title: Il dominio è un dominio federato ma l'utente <Utente>@contoso.com non è noto a Office 365
TOCTitle: Il dominio è un dominio federato ma l'utente <Utente>@contoso.com non è noto a Office 365
ms:assetid: 4c8a571d-d7e8-4316-8772-39b5db91566e
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Hh241332(v=EXCHG.80)
ms:contentKeyID: 42607544
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Il dominio è un dominio federato ma l'utente \<Utente\>@contoso.com non è noto a Office 365

 

***Ultima modifica dell'argomento:** 2011-10-25*

L'Analizzatore connettività remota Microsoft interroga la piattaforma di autenticazione nel cloud per individuare l'area di autenticazione. In alcuni casi, il processo di individuazione dell'area di autenticazione viene eseguito, ma viene comunque visualizzato un messaggio di avviso.

L'individuazione dell'area di autenticazione viene eseguita al fine di generare il provider di identità per l'utente. Se il nome del dominio supera il controllo di individuazione dell'area di autenticazione, viene eseguito un ulteriore processo per determinare se l'utente dispone di un account nell'ambiente Microsoft Office 365. Tale controllo aggiuntivo non impedisce il superamento del test, ma può causare un errore che determina la generazione di un avviso.

Se il dominio è federato ma l'account utente non è abilitato nell'ambiente Office 365, l'Analizzatore connettività remota visualizza l'avviso seguente:

###  

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Il dominio è un dominio federato ma l'utente apollo@contoso.com non è noto a Office 365.</p></td>
</tr>
</tbody>
</table>

Tale messaggio può essere ignorato.

## Ulteriori informazioni

Per ulteriori informazioni su come risolvere questo problema, vedere l'articolo 2523192 della Microsoft Knowledge Base, [I nomi principali utente (UPN), gli indirizzi di posta elettronica o gli indirizzi proxy di utenti contengono un dominio 365 Office dopo la sincronizzazione](http://support.microsoft.com/kb/2523192)

Per ulteriori informazioni sulla pianificazione per la federazione delle identità, vedere [Preparazione dell'accesso Single Sign-On](http://onlinehelp.microsoft.com/it-it/office365-enterprises/ff652540.aspx)

Per informazioni della Guida sull'aggiornamento dell'ambiente Exchange 2010 corrente, vedere [Assistente per la distribuzione di Exchange Server (in lingua inglese)](http://technet.microsoft.com/it-it/exdeploy2010/default.aspx).

