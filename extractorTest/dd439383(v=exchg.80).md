---
title: Modalità cache obbligatoria per questa cassetta postale
TOCTitle: Modalità cache obbligatoria per questa cassetta postale
ms:assetid: b06310b2-a2ca-4011-b023-de01ad71842f
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439383(v=EXCHG.80)
ms:contentKeyID: 27341581
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Modalità cache obbligatoria per questa cassetta postale

 

_**Ultima modifica dell'argomento:** 2011-02-10_

L'analizzatore di Microsoft Exchange interroga Exchange Server e tenta di connettersi all'Archivio informazioni in modalità online. L'Analizzatore connettività remota di Exchange visualizza il seguente avviso quando il server Exchange è stato configurato per forzare le connessioni con la modalità cache.

"L'accesso archivio ha restituito ecCachedModeRequired 1249. Per questa cassetta postale è richiesta la modalità cache."

Gli amministratori di Exchange 2007 e 2010 possono impedire agli utenti di connettersi con la modalità online utilizzando il cmdlet Set-CasMailbox per impostare su True l'attributo MAPIBlockOutlookNonCachedMode. Se è richiesta la modalità cache, gli utenti che tentano di connettersi con il profilo Outlook configurato per la modalità online riceveranno il seguente messaggio di errore:

"L'amministratore di Exchange Server ha bloccato la versione di Outlook che si sta utilizzando. Contattare l'amministratore per richiedere assistenza."

## Per ulteriori informazioni

L'avviso generato dall'Analizzatore connettività remota di Exchange non è necessariamente indicativo di un problema. La forzatura della modalità cache è un'opzione di configurazione legittima. Tuttavia, se l'Analizzatore connettività remota di Exchange è stato eseguito perché vi sono client Outlook che non riescono a connettersi, sarà necessario verificare se quei client possono connettersi con la modalità cache.

**Per verificare le impostazioni del profilo per Outlook e controllare se la casella Modalità cache è selezionata**

1.  Fare clic su Start, fare clic su Esegui, digitare control, quindi fare clic su OK.

2.  Fare doppio clic su Posta, quindi fare clic su Mostra profili.

3.  Selezionare il profilo, quindi fare clic su Proprietà.

4.  Fare clic su Account di posta elettronica, selezionare Visualizza o cambia gli account di posta elettronica esistenti, quindi fare clic su Avanti.

5.  Selezionare l'account Exchange, quindi fare clic su Cambia.

6.  Fare clic per selezionare la casella Usa modalità cache.

**Per stabilire se per la cassetta postale è richiesta la modalità cache con Exchange Management Shell**

1.  Eseguire il comando indicato di seguito:
    
        Get-CasMailbox MailboxName | fl MapiBlockOutlookNonCachedMode

Se questo comando restituisce True, è necessario connettersi a Exchange 2007 o 2010 con la modalità cache di Exchange. In alternativa, è possibile disabilitare il requisito che impone all'utente l'utilizzo della modalità cache.

**Per consentire a un utente di connettersi senza la modalità cache con Exchange Management Shell**

1.  Eseguire il comando indicato di seguito:
    
        Set-CasMailbox MailboxName -MapiBlockOutlookNonCachedMode:$false

Per ulteriori informazioni, vedere l'articolo della Microsoft Knowledge Base, "Quando si utilizza Outlook con una cassetta postale di Exchange 2007, non è possibile connettersi a Exchange 2007 e si riceve un messaggio di errore" ([http://go.microsoft.com/fwlink/?linkid=3052\&kbid=924625](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=924625)).

Per informazioni sul cmdlet Set-CasMailbox, vedere [Set-CASMailbox](http://technet.microsoft.com/it-it/library/bb125264.aspx)

