---
title: Message Header Analyzer
TOCTitle: Message Header Analyzer
ms:assetid: 671e8f3c-5c12-478e-b091-e693af554321
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dn133083(v=EXCHG.80)
ms:contentKeyID: 54781692
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Message Header Analyzer

 

***Ultima modifica dell'argomento:** 2013-03-29*

Se si è già dovuto risolvere problemi all'interno di un sistema di posta elettronica, indipendentemente dal servizio utilizzato, l'utente potrebbe conoscere le intestazioni del messaggio. Le intestazioni del messaggio contengono informazioni sul percorso di un messaggio, oltre ad altri metadati importanti.

L'intestazione è in grado di rispondere a diverse domande su un messaggio, quali:

  - Perché il messaggio impiega così tanto ad arrivare?  
  - Perché il messaggio è finito nella cartella Posta indesiderata?  
  - Quali passaggi ha superato il messaggio per arrivare nella casella Posta in arrivo?  

Gli analizzatori dell'intestazione, ad esempio quello incluso nell'Analizzatore connettività remota Microsoft, consentono di visualizzare e analizzare le intestazioni dei messaggi mostrando le informazioni in modo semplice ed evidenziando diversi problemi, come ad esempio ritardi di consegna sospetti che potrebbero richiedere attenzione.

Le intestazioni del messaggio sono più utili quando è possibile leggere la copia di un messaggio del destinatario. Le intestazioni nella copia del mittente non sono necessariamente utili. Se si desidera ricevere le intestazioni del messaggio, il destinatario dovrà estrarre le intestazioni o inoltrare il messaggio di posta elettronica originale come allegato. La maggior parte dei client di posta elettronica offrono questa funzionalità come opzione, ma non per impostazione predefinita.

Dopo aver ottenuto le intestazioni del messaggio, incollarle in Message Header Analyzer, quindi fare clic su **Analizza**. L'Analizzatore mostra un'analisi di ogni passaggio compiuto dal messaggio e i dettagli relativi ai messaggi non ricevuti.

<table>
<thead>
<tr class="header">
<th><img src="images/Dd439361.note(EXCHG.80).gif" title="note" alt="note" />Nota:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Se un messaggio non è mai giunto a destinazione, sarà necessario provare un metodo diverso per ottenere queste informazioni, ad esempio utilizzando le funzionalità di verifica dei messaggi offerte da Microsoft Exchange Server o Microsoft Exchange Online. Tali funzionalità mantengono un registro di tutti i messaggi gestiti dal sistema. Generalmente, in questa situazione sarà necessario lavorare con il supporto tecnico o l'amministratore di sistema.</td>
</tr>
</tbody>
</table>

## Visualizzazione delle intestazioni del messaggio

Per istruzioni su come visualizzare le intestazioni del messaggio, visitare le seguenti sezioni, a seconda dei client di posta elettronica utilizzati:

  - Outlook 2013, Outlook 2010 oppure Outlook 2007  
  - Outlook Web App  
  - App Windows Mail  
  - Windows Mail (desktop)  
  - Client Thunderbird (IMAP)  
  - Dispositivi mobili (Windows Phone, iPhone, iPad e così via)  
  - Outlook.com  
  - Apple Mail  
  - Gmail.com  

## Outlook 2013, Outlook 2010 oppure Outlook 2007

Nonostante queste versioni di Outlook siano leggermente diverse, la procedura per visualizzare le intestazioni del messaggio è fondamentalmente la stessa. Per qualsiasi versione, attenersi alla seguente procedura:

1.  Aprire il messaggio.  
2.  Nella scheda **File**, selezionare **Proprietà** nella sezione **Informazioni**.  
    In alternativa, fare clic sul pulsante di visualizzazione della finestra di dialogo nell'angolo inferiore destro del gruppo **Tag** della barra multifunzione.  
3.  Nella finestra di dialogo **Proprietà**, individuare le intestazioni del messaggio nella sezione **Intestazioni Internet**.  

Per ulteriori informazioni, vedere l'articolo relativo alla [visualizzazione delle intestazioni del messaggio di posta elettronica](http://office.microsoft.com/it-it/outlook-help/view-e-mail-message-headers-ha001230300.aspx)

## Outlook Web App

  - **Exchange Server 2007 (OWA)**   Aprire il messaggio, quindi fare clic sull'icona "Dettagli messaggio". Nella finestra di dialogo **Dettagli messaggio** , individuare le intestazioni del messaggio nella sezione **Intestazioni posta Internet**.  
  - **Exchange Server 2013 OWA**   Scaricare l'app [Message Headers Analyzer](http://office.microsoft.com/en-us/store/message-header-analyzer-wa104005406.aspx?queryid=69795c55-fbb0-4a0d-8ec3-d779b421a7ea%26css=headers%26ctt=1) dall'app store di Office.  

## App Windows Mail

Al momento, l'app Windows 8 Mail non offre questa funzionalità.

## Windows Mail (desktop)

1.  Nella cartella Posta in arrivo, fare clic con il pulsante destro del mouse sul messaggio, quindi scegliere **Proprietà**.  
2.  Fare clic sulla scheda **Dettagli** per visualizzare le intestazioni del messaggio.  

## Client Thunderbird (IMAP)

1.  Fare doppio clic per aprire il messaggio.  
2.  Scegliere **Intestazione completa** dal menu **Visualizza**. Le intestazioni del messaggio vengono visualizzate in una nuova finestra nell'intestazione completa.  

## Dispositivi mobili (Windows Phone, iPhone, iPad e così via)

Alcune app per dispositivi mobili offrono questa funzionalità. Tuttavia, la maggior parte dei dispositivi mobili non presenta un metodo valido per recuperare le intestazioni del messaggio. Per il momento, si consiglia di utilizzare un computer per accedere al proprio client di posta elettronica Web che offre questa funzionalità.

## Outlook.com

In qualsiasi cartella, fare clic con il pulsante destro del mouse su un messaggio, quindi fare clic su **Visualizza intestazione completa**. Le intestazioni del messaggio e tutte le intestazioni complete vengono visualizzate in una finestra del browser.

## Apple Mail

Per le versioni correnti di Apple Mail, attenersi alla seguente procedura:

1.  Fare clic sul messaggio.  
2.  Dal menu **Visualizza** fare clic su **Messaggio**.  
3.  Fare clic su **Intestazioni lunghe**. Individuare le intestazioni del messaggio nella finestra sotto la cartella Posta in arrivo.  

## Gmail.com

1.  Aprire il messaggio.  
2.  Nella parte superiore del messaggio, fare clic sulla freccia in giù accanto a **Rispondi**, quindi fare clic su **Mostra originale**. Individuare le intestazioni complete nella nuova finestra del browser che si apre.

