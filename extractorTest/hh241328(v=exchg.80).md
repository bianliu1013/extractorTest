---
title: Lo spazio dei nomi non è federato
TOCTitle: Lo spazio dei nomi non è federato
ms:assetid: 08199ae2-2469-4f5f-aba5-aa4744ac7ebf
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Hh241328(v=EXCHG.80)
ms:contentKeyID: 42607540
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Lo spazio dei nomi non è federato

 

_**Ultima modifica dell'argomento:** 2011-06-22_

L'Analizzatore connettività remota Microsoft interroga la piattaforma di autenticazione nel cloud per individuare l'area di autenticazione. Al termine del processo la piattaforma di autenticazione passa al client richiedente l'URL dell'endpoint ADFS necessario per l'autenticazione del client. Se l'identità specificata non corrisponde al nome di un dominio configurato per la federazione delle identità, la ricerca non riesce.

Quando la parte del nome relativa al dominio non è configurata per la federazione delle identità, l'Analizzatore connettività remota restituisce l'avviso seguente:


<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Il dominio non è un dominio federato.</p></td>
</tr>
</tbody>
</table>


Questo messaggio indica un errore del processo di individuazione dell'area di autenticazione. Tale processo esegue il controllo iniziale del nome del dominio, per determinare se nella piattaforma di autenticazione del cloud tale dominio risulta configurato per la federazione delle identità. L'errore del processo può essere dovuto a un nome principale utente (UPN) non digitato correttamente oppure indicare che la federazione delle identità non è ancora stata configurata.

Per verificare se il dominio è configurato per la federazione delle identità, procedere come segue:

1.  Accedere al portale Microsoft Online come amministratore tenant.  
2.  Nel riquadro di spostamento, in **Gestione** fare clic su **Domini**.  
3.  Individuare il dominio corrispondente all'UPN immesso per il test.  
4.  Verificare che il tipo di dominio sia **configurato per il single sign-on**.  

## Ulteriori informazioni

Per ulteriori informazioni sulla pianificazione per la federazione delle identità, vedere [Preparazione dell'accesso Single Sign-On](http://onlinehelp.microsoft.com/it-it/office365-enterprises/ff652540.aspx)

Per informazioni della Guida sull'aggiornamento dell'ambiente Exchange 2010 corrente, vedere [Assistente per la distribuzione di Exchange Server (in lingua inglese)](http://technet.microsoft.com/it-it/exdeploy2010/default.aspx)

