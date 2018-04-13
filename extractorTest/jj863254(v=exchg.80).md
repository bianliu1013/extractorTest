---
title: "Errore durante l'esecuzione dello strumento Analizzatore connettività remota di Exchange per testare la connettività a Office 365: \"Per l'autenticazione a Office 365, è necessario immettere il proprio account Microsoft\""
TOCTitle: "Errore durante l'esecuzione dello strumento Analizzatore connettività remota di Exchange per testare la connettività a Office 365: \"Per l'autenticazione a Office 365, è necessario immettere il proprio account Microsoft\""
ms:assetid: 1f7414a1-1079-459a-ae72-3c431a01813e
ms:mtpsurl: https://technet.microsoft.com/it-it/library/JJ863254(v=EXCHG.80)
ms:contentKeyID: 50553805
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Errore durante l'esecuzione dello strumento Analizzatore connettività remota di Exchange per testare la connettività a Office 365: \"Per l'autenticazione a Office 365, è necessario immettere il proprio account Microsoft\"

 

_**Ultima modifica dell'argomento:** 2012-11-06_

Se si verifica un problema quando si tenta di eseguire lo strumento Analizzatore connettività remota di Microsoft Exchange per testare la connettività a Microsoft Office 365, è possibile che venga visualizzato il seguente messaggio di errore: Per l'autenticazione a Office 365, è necessario immettere il proprio account Microsoft. È il nome dell'entità utente e in molti casi sarà simile a utente@contoso.com.

Le seguenti sezioni possono essere utili per risolvere questo problema.

## Informazioni per gli utenti finali

Gli utenti di Office 365 che rilevano dei problemi quando eseguono lo strumento Analizzatore connettività remota di Microsoft Exchange possono utilizzare le informazioni nella tabella seguente per risolvere il problema.


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Possibile causa</th>
<th>Soluzione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Si sta utilizzando un nome utente non corretto.</p></td>
<td><p>Immettere l'ID utente di Office 365. L'ID utente di Office 365 è il nome dell'entità utente. Ad esempio, immettere <strong>jane@contoso.com</strong>.</p>
<p>Se non si conosce il proprio ID utente di Office 365, rivolgersi all'amministratore.</p></td>
</tr>
<tr class="even">
<td><p>La password è scaduta.</p></td>
<td><p>Contattare l'amministratore per reimpostare la password. Per ulteriori informazioni, fare riferimento all'articolo della Microsoft Knowledge Base <a href="http://go.microsoft.com/fwlink/?linkid=3052%26kbid=2606983">2606983: Un utente di Office 365 o un amministratore di Office 365 ha dimenticato la propria password</a>.</p></td>
</tr>
<tr class="odd">
<td><p>L'account utente di Office 365 non è stato attivato.</p></td>
<td><p>Per iniziare a utilizzare Office 365, è necessario attivare il proprio account. A questo scopo, accedere al portale di Office 365 (<a href="https://portal.microsoftonline.com" class="uri">https://portal.microsoftonline.com</a>) per la prima volta utilizzando la password temporanea e quindi creare una nuova password da utilizzare per l'accesso.</p>
<p>Per ulteriori informazioni, visitare uno dei seguenti siti Web Office 365:</p>
<ul>
<li>Se si utilizza Office 365 per le aziende: <a href="http://onlinehelp.microsoft.com/it-it/office365-enterprises/ff637578.aspx">Modifica della password</a><br />
</li>
<li>Se si utilizza Microsoft Office 365 per professionisti e piccole aziende: <a href="http://onlinehelp.microsoft.com/it-it/office365-smallbusinesses/ff637529.aspx">Modifica della password</a><br />
</li>
</ul></td>
</tr>
<tr class="even">
<td><p>L'account di accesso a Microsoft è bloccato.</p></td>
<td><p>Attendere 15 minuti e quindi tentare di accedere nuovamente. Se il problema persiste, l'amministratore potrebbe aver reimpostato la password per sbloccare l'account. Per ulteriori informazioni, fare riferimento all'articolo della Microsoft Knowledge Base <a href="http://go.microsoft.com/fwlink/?linkid=3052%26kbid=2412085">2412085: Impossibile accedere a Microsoft Online Services</a></p></td>
</tr>
</tbody>
</table>


## Informazioni per gli amministratori

Gli utenti di Office 365 che rilevano dei problemi quando eseguono lo strumento Analizzatore connettività remota di Microsoft Exchange possono utilizzare le informazioni nella tabella seguente per risolvere il problema.


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Possibile causa</th>
<th>Soluzione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Si sta utilizzando un nome utente non corretto.</p></td>
<td><p>Immettere l'ID utente di Office 365. L'ID utente di Office 365 è il nome dell'entità utente. Ad esempio, immettere <strong>jane@contoso.com</strong>.</p>
<p>Per ulteriori informazioni su come risolvere il problema, fare riferimento a <a href="http://onlinehelp.microsoft.com/it-it/office365-smallbusinesses/gg549202.aspx">Perché è necessario un ID utente?</a></p></td>
</tr>
<tr class="even">
<td><p>La password è scaduta.</p></td>
<td><p>Per informazioni su come risolvere questo problema, fare riferimento all'articolo della Microsoft Knowledge Base <a href="http://go.microsoft.com/fwlink/?linkid=3052%26kbid=2412085">2412085: Impossibile accedere a Microsoft Online Services</a>.</p>
<p>Fare inoltre riferimento ai seguenti articoli:</p>
<ul>
<li><a href="http://onlinehelp.microsoft.com/it-it/office365-smallbusinesses/ff637553.aspx">Reimpostazione della password di un utente</a><br />
</li>
<li><a href="http://onlinehelp.microsoft.com/it-it/office365-smallbusinesses/gg192871.aspx">Reimpostazione della password di un amministratore</a><br />
</li>
</ul></td>
</tr>
<tr class="odd">
<td><p>L'account utente di Office 365 non è stato attivato.</p></td>
<td><p>Per informazioni su come risolvere questo problema, fare riferimento all'articolo della Microsoft Knowledge Base <a href="http://go.microsoft.com/fwlink/?linkid=3052%26kbid=2412085">2412085: Impossibile accedere a Microsoft Online Services</a></p></td>
</tr>
<tr class="even">
<td><p>L'account di accesso a Microsoft è bloccato.</p></td>
<td><p>Attendere 15 minuti e quindi tentare di accedere nuovamente. Se il problema persiste, reimpostare la password per sbloccare l'account. Per ulteriori informazioni, fare riferimento all'articolo della Microsoft Knowledge Base <a href="http://go.microsoft.com/fwlink/?linkid=3052%26kbid=2412085">2412085: Impossibile accedere a Microsoft Online Services</a></p></td>
</tr>
</tbody>
</table>


## Ulteriori informazioni

Per ulteriori informazioni, visitare i seguenti siti Web Office 365:

  - [Accesso e password](http://onlinehelp.microsoft.com/it-it/office365-smallbusinesses/ff637538.aspx)  
  - [Account e autorizzazioni utente](http://onlinehelp.microsoft.com/it-it/office365-smallbusinesses/ff637545.aspx)

