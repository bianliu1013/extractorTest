---
title: Crittografia RPC obbligatoria
TOCTitle: Crittografia RPC obbligatoria
ms:assetid: cf3a5af1-52ae-4509-8793-84e98f81ec22
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439391(v=EXCHG.80)
ms:contentKeyID: 27341599
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Crittografia RPC obbligatoria

 

_**Ultima modifica dell'argomento:** 2011-05-19_

Lo strumento Microsoft Exchange Best Practices Analyzer interroga il server che esegue Exchange Server e tenta di effettuare l'accesso tramite RPC su HTTP. Se in Exchange Server è richiesta la crittografia RPC, lo strumento potrebbe visualizzare l'avviso seguente:


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>L'accesso archivio ha restituito ecNotEncrypted 2416. Il server richiede la crittografia RPC.</p></td>
</tr>
</tbody>
</table>


Per impostazione predefinita, Microsoft Office Outlook 2007 è configurato con l'opzione **Crittografa dati trasferiti tra Microsoft Office Outlook e Microsoft Exchange Server** abilitata. Tuttavia, nella configurazione predefinita di Microsoft Outlook 2003 tale opzione non è abilitata. Se si utilizza il cmdlet **Set-MailboxServer** per forzare le connessioni crittografate nelle cassette postali degli utenti e nel client Outlook l'impostazione **Crittografa dati trasferiti tra Microsoft Office Outlook e Microsoft Exchange Server** è disattivata, gli utenti che tentano di connettersi alle proprie cassette postali in Exchange riceveranno il messaggio seguente.


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>L'amministratore di Microsoft Exchange ha bloccato la versione di Outlook che si sta utilizzando. Per richiedere assistenza, contattare l'amministratore.</p></td>
</tr>
</tbody>
</table>


Gli utenti di Outlook 2003 che si connettono a Exchange possono ricevere uno dei messaggi di errore seguenti:


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Impossibile avviare Microsoft Office Outlook. Impossibile aprire la finestra di Outlook. Impossibile aprire il gruppo di cartelle.</p></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Impossibile aprire le cartelle di posta elettronica predefinite. Il computer che esegue Microsoft Exchange Server non è disponibile. È probabile che vi siano problemi di rete o che il computer che esegue Microsoft Exchange Server sia inattivo per manutenzione.</p></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>La connessione a Microsoft Exchange Server non è disponibile. Per completare l'operazione, è necessario che Outlook sia in rete o connesso.</p></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Impossibile aprire le cartelle di posta elettronica predefinite. Impossibile aprire l'archivio informazioni.</p></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Impossibile effettuare l'accesso. Verificare la connessione di rete e il nome del server e della cassetta postale. La connessione a Microsoft Exchange Server non è disponibile. Per completare l'operazione, è necessario che Outlook sia in rete o connesso.</p></td>
</tr>
</tbody>
</table>


Quando Outlook 2003 è configurato in modo da utilizzare la modalità cache di Exchange, in Outlook non viene visualizzato alcun messaggio di errore, ma l'applicazione viene avviata in modalità disconnessa.

## Per ulteriori informazioni

Per risolvere questo problema, eseguire una o più delle operazioni seguenti:

  - Determinare se il server cassette postali di Exchange 2007 richiede la crittografia RPC. A tale scopo, eseguire il cmdlet seguente in Exchange Management Shell:  
    
        Get-MailboxServer <ServerName>
    
    Se MAPIEncryptionRequired ha valore True, nel client Outlook connesso a Exchange l'opzione **Crittografa dati trasferiti tra Microsoft Office Outlook e Microsoft Exchange Server** deve essere abilitata.  

  - Determinare se il server Accesso client di Exchange 2010 richiede la crittografia RPC. A tale scopo, eseguire il cmdlet seguente in Exchange Management Shell:  
    
        Get-RpcClientAccess | fl Server,EncryptionRequired
    
    Se EncryptionRequired ha valore True, nel client Outlook connesso a Exchange l'opzione **Crittografa dati trasferiti tra Microsoft Office Outlook e Microsoft Exchange Server** deve essere abilitata.  

  - Verificare che l'opzione **Crittografa dati trasferiti tra Microsoft Office Outlook e Microsoft Exchange Server** sia abilitata in ogni profilo di Outlook. A tale scopo, seguire questa procedura:  
    
    1.  Aprire **Posta elettronica** nel Pannello di controllo, quindi fare clic su **Account di posta elettronica**.  
    2.  Selezionare l'account Exchange, quindi fare clic su **Cambia**.  
    3.  Scegliere **Altre impostazioni**, quindi fare clic sulla scheda **Sicurezza**.  
    4.  Selezionare la casella di controllo **Crittografa dati trasferiti tra Microsoft Office Outlook e Microsoft Exchange Server** e quindi fare clic su **OK** .  
    5.  Scegliere **Avanti**, quindi **Fine**.  

  - In alternativa, è possibile rimuovere il requisito di Exchange per la crittografia delle comunicazioni RPC. A tale scopo, seguire questa procedura.  
    

    > [!NOTA]
    > <STRONG>Nota</STRONG> In Exchange Server 2010 Service Pack 1 (SP1) il requisito per la crittografia delle comunicazioni RPC è disattivato per impostazione predefinita.

    
      - Per un server cassette postali Exchange 2007 eseguire il comando indicato di seguito in Exchange Management Shell:  
        
            Set-MailboxServer <ServerName> -MapiEncryptionRequired:$false
    
      - Per un server di Accesso client di Exchange 2010 eseguire il comando indicato di seguito in Exchange Management Shell:  
        
            Set-RpcClientAccess -Server <ServerName> -EncryptionRequired $False

Per ulteriori informazioni su altri problemi che potrebbero causare gli errori indicati in questo argomento, vedere l'articolo 924625 della Microsoft Knowledge Base, [Quando si utilizza Outlook con una cassetta postale di Exchange 2007, non è possibile connettersi a Exchange 2007 e si riceve un messaggio di errore](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=924625).

Per ulteriori informazioni sulla connettività di Outlook 2003 con Exchange Server 2010, inclusi ulteriori metodi di risoluzione, vedere l'articolo della Microsoft Knowledge Base [Problemi di connessione di Outlook con cassette postali di Exchange 2010 a causa dei requisiti di crittografia RPC](http://support.microsoft.com/kb/2006508).

Per informazioni sul cmdlet Set-MailboxServer cmdlet e l'attributo MAPIEncryptionRequired, vedere [Set- MailboxServer](http://go.microsoft.com/fwlink/?linkid=161822).

Per ulteriori informazioni sulla distribuzione di Exchange 2010 con client Outlook 2003, vedere [Problema: la presenza di client Outlook 2003 può impedire la distribuzione di Exchange 2010? (informazioni in lingua inglese)](http://social.technet.microsoft.com/wiki/contents/articles/concern-is-having-outlook-2003-clients-going-to-prevent-me-from-deploying-exchange-2010.aspx).

