---
title: Il certificato di firma dei token è scaduto
TOCTitle: Il certificato di firma dei token è scaduto
ms:assetid: 56574861-b444-487c-a2c9-b33b0e4e2830
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Hh241334(v=EXCHG.80)
ms:contentKeyID: 42607545
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Il certificato di firma dei token è scaduto

 

_**Ultima modifica dell'argomento:** 2011-06-06_

L'Analizzatore connettività remota di Microsoft Exchange interroga la piattaforma di autenticazione del cloud per simulare il processo di autenticazione utilizzato da un client per autenticarsi tramite la federazione delle identità. A volte un client Outlook o una connessione di Microsoft Internet Explorer non riesce a causa di un certificato di firma dei token scaduto.

Quando si verifica questo problema, se si utilizza la modalità di autenticazione passiva viene visualizzato un errore simile al seguente (Internet Explorer)

Problema durante l'accesso al sito. Provare di nuovo a esplorare il sito. Se il problema persiste, contattare l'amministratore del sito e specificare il numero di riferimento per identificare il problema. Numero di riferimento: \<GUID\>

L'Analizzatore connettività remota visualizza un avviso se l'autenticazione non riesce. Il problema può essere dovuto a un certificato di firma dei token scaduto. Questa situazione può presentarsi perché, per impostazione predefinita, ADFS può rinnovare automaticamente un certificato autofirmato per la firma dei token. Tale funzionalità riduce al minimo la manutenzione richiesta dall'ambiente ADFS, ma può influire sulla federazione delle identità, perché la piattaforma di autenticazione del cloud non è a conoscenza del nuovo certificato di firma dei token.

## Ulteriori informazioni

Per ulteriori informazioni su come risolvere questo problema, vedere l'articolo 2383983 della Microsoft Knowledge Base, [Come aggiornare i certificati di Active Directory Federation Services 2.0](http://support.microsoft.com/kb/2383983).

Per ulteriori informazioni sulla pianificazione per la federazione delle identità, vedere [Preparazione dell'accesso Single Sign-On](http://onlinehelp.microsoft.com/it-it/office365-enterprises/ff652540.aspx)

Per informazioni della Guida sull'aggiornamento dell'ambiente Exchange 2010 corrente, vedere [Assistente per la distribuzione di Exchange Server (in lingua inglese)](http://technet.microsoft.com/it-it/exdeploy2010/default.aspx).

