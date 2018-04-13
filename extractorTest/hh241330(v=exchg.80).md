---
title: Attendibilità del certificato SSL di ADFS
TOCTitle: Attendibilità del certificato SSL di ADFS
ms:assetid: 19604d13-e410-4874-961c-1900ab391d66
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Hh241330(v=EXCHG.80)
ms:contentKeyID: 42607542
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Attendibilità del certificato SSL di ADFS

 

_**Ultima modifica dell'argomento:** 2011-06-06_

L'Analizzatore connettività remota di Microsoft Exchange interroga la piattaforma di autenticazione nel cloud per individuare l'area di autenticazione. Al termine del processo la piattaforma di autenticazione passa al client richiedente l'URL dell'endpoint ADFS necessario per l'autenticazione del client. Tale endpoint è una connessione SSL (Secure Sockets Layer) dotata di certificato. Lo strumento valuta il nome di dominio completo (FQDN) assegnato al certificato (ad esempio, STS.Contoso.com).

L'Analizzatore connettività remota visualizza un avviso quando il certificato utilizzato per SSL non può essere considerato attendibile fino alla radice. Questo problema indica che il certificato non è considerato attendibile dall'ambiente Office 365. Tale condizione è spesso dovuta al fatto che il certificato è autofirmato e non è pertanto valido per questa forma di autenticazione.

L'avviso relativo all'attendibilità del certificato indica che gli utenti potrebbero non essere autenticati correttamente nelle relative risorse Office 365. Se si verifica questo problema, con la modalità di accesso passiva (Internet Explorer) ai servizi di Office 365 viene visualizzato un avviso relativo al certificato quando l'utente accede ai servizi. Il client passivo può stabilire la connessione solo se l'avviso relativo al certificato viene accettato. Il client Outlook non riceve questo avviso di sicurezza relativo al certificato e non riesce a stabilire la connessione.

## Ulteriori informazioni

Per informazioni su come risolvere questo problema, vedere l'articolo della Microsoft Knowledge Base [Quando si tenta di accedere alle risorse di Microsoft Office 365 utilizzando un account federato identità, viene visualizzato un avviso di certificato](http://support.microsoft.com/kb/2523494)

Per ulteriori informazioni sulla pianificazione per la federazione delle identità, vedere [Preparazione dell'accesso Single Sign-On](http://onlinehelp.microsoft.com/it-it/office365-enterprises/ff652540.aspx)

Per informazioni della Guida sull'aggiornamento dell'ambiente Exchange 2010 corrente, vedere [Assistente per la distribuzione di Exchange Server (in lingua inglese)](http://technet.microsoft.com/it-it/exdeploy2010/default.aspx).

