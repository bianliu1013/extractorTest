---
title: Problemi relativi al nome principale dell'utente (UPN) durante l'autenticazione
TOCTitle: Problemi relativi al nome principale dell'utente (UPN) durante l'autenticazione
ms:assetid: f8ebfa55-7b2c-4bb4-902e-e457dc22b4d9
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Hh241340(v=EXCHG.80)
ms:contentKeyID: 42607554
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Problemi relativi al nome principale dell'utente (UPN) durante l'autenticazione

 

_**Ultima modifica dell'argomento:** 2012-02-24_

L'Analizzatore connettività remota di Microsoft Exchange interroga la piattaforma di autenticazione del cloud per simulare il processo di autenticazione utilizzato da un client per autenticarsi tramite la federazione delle identità. A volte si verifica un problema che si manifesta in genere con un client Outlook che richiede continuamente l'immissione delle credenziali da parte degli utenti.

Il client Outlook può richiedere ripetutamente l'autenticazione a causa di molti problemi diversi. Questo sintomo può verificarsi quando un utente federato utilizza un UPN che non fa riferimento a un dominio federato.

L'Analizzatore connettività remota visualizza un avviso se l'autenticazione non riesce. In alcune situazioni, tuttavia, tale messaggio può essere generico e non specificare la causa dell'errore. In tali casi, sono possibili molte soluzioni diverse. Tuttavia, tutte le soluzioni a questi problemi sono correlate alla configurazione ADFS locale.

## Ulteriori informazioni

Per ulteriori informazioni su come risolvere il problema, vedere [Un utente federato richieste le credenziali o Impossibile accedere a Microsoft Online Services configurazione single sign-on per un'organizzazione](http://support.microsoft.com/kb/2392130).

Per ulteriori informazioni sulla pianificazione per la federazione delle identità, vedere [Preparazione dell'accesso Single Sign-On](http://onlinehelp.microsoft.com/it-it/office365-enterprises/ff652540.aspx).

Per informazioni della Guida sull'aggiornamento dell'ambiente Exchange 2010 corrente, vedere [Assistente per la distribuzione di Exchange Server (in lingua inglese)](http://technet.microsoft.com/it-it/exdeploy2010/default.aspx).

