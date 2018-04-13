---
title: Errore con l'ora di sistema
TOCTitle: Errore con l'ora di sistema
ms:assetid: d444776a-2a72-4185-8979-bd786390b38f
ms:mtpsurl: https://technet.microsoft.com/it-it/library/JJ710174(v=EXCHG.80)
ms:contentKeyID: 49378895
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Errore con l'ora di sistema

 

_**Ultima modifica dell'argomento:** 2012-11-06_

Lo strumento Analizzatore connettività remota di Microsoft Exchange individua eventuali problemi che hanno per oggetto le query sulla disponibilità tra una cassetta postale di Office 365 e una cassetta postale locale. Questo controllo dello stato verifica anche l'ora di sistema del server Exchange locale. Come nel caso dei problemi che possono interessare il protocollo Kerberos, se si riscontra uno scostamento superiore ai 5 minuti dell'ora di sistema sul server locale che comunica con Microsoft Federation Gateway, quando il server richiede un token di delega riceve un errore di accesso negato.

L'errore di accesso negato provoca problemi che interessano le ricerche sui dati di disponibilità cross-premise, oltre ad altri problemi a livello di altre funzionalità cross-premise. Per risolvere questo problema, utilizzare un orologio affidabile per i server nell'ambiente e impostare l'ora di sistema sui valori corretti.


> [!NOTA]
> Se si sta creando una relazione di trust federativa, per gli stessi motivi indicati in precedenza è possibile che si riceva il seguente messaggio di errore: 1007 AccessDenied: Accesso negato.



Generalmente, questo messaggio di errore è un indicatore attendibile di questo problema. Tuttavia, se non si è certi che si tratti proprio di questo problema, connettersi a Exchange Management Shell sul server Exchange locale e utilizzare il seguente cmdlet: **Test-FederationTrust ValidMailbox -userIdentity –Verbose**.

## Ulteriori informazioni

Per informazioni su come risolvere questo problema, vedere [Sincronizzazione del server di riferimento ora per il controller di dominio con un orologio esterno](http://technet.microsoft.com/it-it/library/cc784553\(ws.10\).aspx).

Si consiglia di consultare le seguenti risorse prima di scegliere come configurare un server Exchange cross-premise:

  - [Assistente per la distribuzione di Exchange Server](http://technet.microsoft.com/it-it/exdeploy2010/default.aspx)  
  - Articolo della Microsoft Knowledge Base [Come risolvere i problemi di disponibilità quando si utilizza la federazione di Exchange in Microsoft Office 365 per l'ambiente aziendale](http://support.microsoft.com/kb/2555008)  

L'Analizzatore connettività remota di Exchange è un nuovo strumento per cui è attualmente disponibile documentazione limitata. Per migliorare la documentazione relativa a ciascun errore che può verificarsi, Microsoft ha scelto di affidarsi alla community per ottenere ulteriori informazioni. Utilizzare la sezione Contenuti Community in questo argomento per segnalare eventuali errori riscontrati fino a questo punto. Se è necessario richiedere assistenza tecnica, contattare il [supporto](http://go.microsoft.com/fwlink/?linkid=8158) oppure creare una nuova segnalazione nel forum dedicato allo strumento Analizzatore connettività remota su TechNet. Sebbene il forum sia stato sospeso, gli argomenti in esso pubblicati restano attivi in [Versioni precedenti di Exchange - Componenti, strumenti e utilità estesi](http://social.technet.microsoft.com/forums/it-it/exchangesvr3rdpartyappslegacy).

