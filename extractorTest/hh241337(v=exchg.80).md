---
title: Problemi generali che possono verificarsi per uno o tutti gli utenti
TOCTitle: Problemi generali che possono verificarsi per uno o tutti gli utenti
ms:assetid: 823ee906-50fb-4354-b748-fd0672ebbaec
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Hh241337(v=EXCHG.80)
ms:contentKeyID: 42607549
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Problemi generali che possono verificarsi per uno o tutti gli utenti

 

***Ultima modifica dell'argomento:** 2012-02-24*

L'Analizzatore connettività remota di Microsoft Exchange interroga la piattaforma di autenticazione nel cloud per individuare l'area di autenticazione. Al termine del processo la piattaforma di autenticazione passa al client richiedente l'URL dell'endpoint ADFS necessario per l'autenticazione del client. Lo strumento esegue l'autenticazione per conto dell'utente, per simulare l'autenticazione nell'ambiente di Office 365.

Se in questa fase l'Analizzatore connettività remota restituisce un avviso, il messaggio può indicare molti problemi diversi. Poiché il processo di autenticazione richiede numerosi passaggi, la soluzione da applicare quando viene restituito un errore o un avviso non è sempre ovvia. Potrebbe essere ad esempio visualizzato uno dei messaggi seguenti:

###  

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Problema durante l'accesso al sito. Provare di nuovo a esplorare il sito.</p></td>
</tr>
<tr class="even">
<td><p>L'organizzazione non è in grado di connettere l'utente al servizio.</p></td>
</tr>
</tbody>
</table>

Questi errori generici potrebbero essere causati ad esempio dai problemi seguenti:

  - Informazioni di federazione delle identità non aggiornate nell'ambiente Office 365  
  - Informazioni di federazione delle identità errate nell'ambiente Office 365  
  - Problemi dovuti alla recente modifica degli UPN  
  - Varie impostazioni del firewall nell'endpoint ADFS  

Poiché questi errori sono piuttosto generici, le soluzioni possono essere molto diverse. Nella sezione "Ulteriori informazioni" sono illustrati vari metodi per risolvere tali problemi.

## Ulteriori informazioni

Per ulteriori informazioni sulla risoluzione di problemi che hanno cause non identificate, vedere i seguenti articoli di Microsoft Knowledge Base:

  - [2521057: Come ristabilire la relazione di trust con la piattaforma di autenticazione Office 365 dopo il blocco di AD FS 2.0](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=2521057)  
  - [2535789: Risoluzione dei problemi dei servizi AD FS 2.0 pubblicati direttamente su Internet tramite un dispositivo firewall invece che tramite un server proxy ADFS](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=2535789)  
  - [2535191: il messaggio di errore "l'organizzazione potrebbe non accedere a questo servizio" si verifica quando un utente tenta di accedere al portale 365 Office come un utente federato](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=2535191)  
  - [2392130: a un utente federato sono state richieste le credenziali oppure è stato negato l'accesso a Microsoft Online Services dopo aver impostato Single Sign-On per un'organizzazione](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=2392130)  

Per ulteriori informazioni sulla pianificazione per la federazione delle identità, vedere [Preparazione dell'accesso Single Sign-On](http://onlinehelp.microsoft.com/it-it/office365-enterprises/ff652540.aspx)

Per informazioni della Guida sull'aggiornamento dell'ambiente Exchange 2010 corrente, vedere [Assistente per la distribuzione di Exchange Server (in lingua inglese)](http://technet.microsoft.com/it-it/exdeploy2010/default.aspx).

