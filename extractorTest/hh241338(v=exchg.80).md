---
title: Il certificato SSL di ADFS è scaduto
TOCTitle: Il certificato SSL di ADFS è scaduto
ms:assetid: a72ff2d6-ca43-473e-9fa4-30ff00fe275d
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Hh241338(v=EXCHG.80)
ms:contentKeyID: 42607550
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Il certificato SSL di ADFS è scaduto

 

***Ultima modifica dell'argomento:** 2011-06-13*

L'Analizzatore connettività remota Microsoft interroga la piattaforma di autenticazione del cloud per individuare l'area di autenticazione. Al termine del processo la piattaforma di autenticazione passa al client richiedente l'URL dell'endpoint ADFS necessario per l'autenticazione del client. Tale endpoint è una connessione SSL (Secure Sockets Layer) dotata di certificato. Lo strumento valuta il nome di dominio completo (FQDN) assegnato al certificato (ad esempio, STS.Contoso.com).

L'Analizzatore connettività remota visualizza un avviso relativo all'attendibilità del certificato quando il certificato utilizzato per SSL è scaduto. Questo problema indica che il certificato non è valido o che gli utenti non verranno autenticati correttamente nelle relative risorse Office 365. Se si verifica questo problema, non è possibile connettersi ai servizi di Office 365 utilizzando la modalità di accesso passiva (Internet Explorer) e viene generato un avviso analogo quando l'utente tenta di accedere a una pagina Web.

## Ulteriori informazioni

Per informazioni su come risolvere questo problema, vedere l'articolo 2523494 della Microsoft Knowledge Base, [Quando si tenta di accedere alle risorse di Microsoft Office 365 utilizzando un account federato identità, viene visualizzato un avviso di certificato](http://support.microsoft.com/kb/2523494)

Per ulteriori informazioni sulla pianificazione per la federazione delle identità, vedere [Preparazione dell'accesso Single Sign-On](http://onlinehelp.microsoft.com/it-it/office365-enterprises/ff652540.aspx)

Per informazioni della Guida sull'aggiornamento dell'ambiente Exchange 2010 corrente, vedere [Assistente per la distribuzione di Exchange Server (in lingua inglese)](http://technet.microsoft.com/it-it/exdeploy2010/default.aspx)

