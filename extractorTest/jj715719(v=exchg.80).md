---
title: Il comando OPTIONS di ActiveSync ha restituito l'errore HTTP 401
TOCTitle: Il comando OPTIONS di ActiveSync ha restituito l'errore HTTP 401
ms:assetid: 0715cdea-acfa-4c0f-88da-16fde67ac3e6
ms:mtpsurl: https://technet.microsoft.com/it-it/library/JJ715719(v=EXCHG.80)
ms:contentKeyID: 49667042
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Il comando OPTIONS di ActiveSync ha restituito l'errore HTTP 401

 

_**Ultima modifica dell'argomento:** 2013-02-05_

Microsoft Exchange ActiveSync consente di eseguire la sincronizzazione delle informazioni della cassetta postale con i dispositivi mobili. A tale scopo, Exchange utilizza la directory virtuale Microsoft-Server-ActiveSync in Internet Information Services (IIS).

Quando Microsoft Best Practices Analyzer testa la connettività ActiveSync, il test di ActiveSync restituisce il seguente messaggio di errore:

    An ActiveSync session is being attempted with the server.
    Errors were encountered while testing the Exchange ActiveSync session.
    Test Steps
    Attempting to send the OPTIONS command to the server.
    Testing of the OPTIONS command failed. For more information, see Additional Details.
    Additional Details
    An HTTP 401 Unauthorized response was received from the remote IIS server. This is usually the result of an incorrect username or password. If you are attempting to log onto an Office 365 service, ensure you are using your full User Principal Name (UPN).

Generalmente questo errore si verifica in un ambiente Exchange 2010 o Exchange 2007 quando la cassetta postale di destinazione si trova su un server Exchange 2003 e sulla directory virtuale **Microsoft-Server-ActiveSync** è configurata l'autenticazione di base.

Quando Exchange 2010 o Exchange 2007 coesiste con Exchange 2003, sulla directory virtuale **Microsoft-Server-ActiveSync** ospitata sul server Cassette postali Exchange 2003 deve essere abilitata l'autenticazione integrata di Windows. Ciò consente al server Accesso client Exchange 2010 o Exchange 2007 e al server di back-end Exchange 2003 di comunicare utilizzando l'autenticazione Kerberos.

La causa più comune di questo errore è l'utilizzo di un nome utente o una password non corretta. Se si utilizza Office 365, accedere utilizzando il nome dell'entità utente (UPN). Ad esempio, accedere utilizzando utente@dominio.com. Se le informazioni di accesso sono corrette, è consigliabile utilizzare la seguente procedura per risolvere il problema.

<table>
<thead>
<tr class="header">
<th><img src="images/JJ715719.important(EXCHG.80).gif" title="important" alt="important" />Importante:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Utilizzare il Gestore di sistema di Exchange per regolare le impostazioni di autenticazione della directory virtuale di Exchange ActiveSync. Non utilizzare Gestione IIS per modificare l'impostazione di autenticazione della directory virtuale di Exchange ActiveSync perché Supervisore sistema Exchange sovrascrive le impostazioni archiviate in Active Directory.</td>
</tr>
</tbody>
</table>


**Per modificare le autorizzazioni sulla directory virtuale Microsoft-Server-ActiveSync nel Gestore di sistema di Exchange 2003**

1.  Installare il seguente aggiornamento rapido sul server Exchange 2003:  
      
    [ID evento 1036 registrato su un server Exchange 2007 che esegue il ruolo Accesso client quando i dispositivi mobili si connettono al server Exchange 2007 per accedere alle cassette postali su un server back-end di Exchange 2003](http://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=937031).

2.  Avviare il Gestore di sistema di Exchange sul server Cassette postali Exchange 2003.

3.  Espandere **Gruppi amministrativi**, **nome\_gruppo\_amministrativo** e infine **Server**.

4.  Espandere *NomeServer*, **Protocolli** e infine **HTTP**.

5.  Espandere **Server virtuale Exchange**, fare clic con il pulsante destro del mouse su **Microsoft-Server-ActiveSync**, quindi scegliere **Proprietà**.

6.  Fare clic sulla scheda **Accesso**, quindi scegliere **Autenticazione**.

7.  Fare clic per selezionare la casella di controllo **Autenticazione integrata di Windows**.

8.  Fare clic su **OK** due volte.

9.  Per verificare che i dati siano stati correttamente replicati nel metabase sul server Exchange, fare quanto segue:
    
    1.  Aprire Gestione Internet Information Services (IIS) in **Strumenti di amministrazione**.  
    2.  Espandere **NomeServer**, **Siti Web** e infine **Sito Web predefinito**.  
    3.  Fare clic con il pulsante destro del mouse su **Microsoft-Server-ActiveSync**, quindi scegliere **Proprietà**.  
    4.  Fare clic sulla scheda **Protezione directory**, quindi selezionare il pulsante **Modifica** sotto **Controllo autenticazione e accesso**.  
    5.  Verificare che la casella di controllo **Autenticazione integrata di Windows** sia selezionata.  

        > [!NOTA]
        > Se la casella di controllo è selezionata, la modifica apportata nel Gestore di sistema di Exchange è stata correttamente replicata nel metabase sul server Exchange.


    6.  Fare due volte clic su **Annulla** e uscire da Gestione Internet Information Services (IIS).  

Per ulteriori informazioni, vedere il passo 7 nella sezione relativa all'"installazione di Exchange 2010" nell'articolo nella TechNet sull' [aggiornamento da Accesso client Exchange 2003](http://go.microsoft.com/fwlink/p/?linkid=280550)

