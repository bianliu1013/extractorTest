---
title: Impossibile risolvere il nome dell'endpoint HTTP di Active Directory Federation Services (ADFS)
TOCTitle: Impossibile risolvere il nome dell'endpoint HTTP di Active Directory Federation Services (ADFS)
ms:assetid: 71fdd487-1725-4343-89ef-b52b76a6defc
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Hh241336(v=EXCHG.80)
ms:contentKeyID: 42607548
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Impossibile risolvere il nome dell'endpoint HTTP di Active Directory Federation Services (ADFS)

 

***Ultima modifica dell'argomento:** 2011-06-21*

L'Analizzatore connettività remota Microsoft interroga la piattaforma di autenticazione nel cloud per eseguire una simulazione del processo di recupero dei token dal server ADFS locale. Per eseguire il test, lo strumento interroga l'endpoint STS ricevuto nel passaggio di individuazione dell'area di autenticazione del dominio eseguito in precedenza. Tale operazione viene eseguita per assicurare che venga impostata una voce DNS esterna per l'endpoint STS, di modo che i client esterni possano risolvere l'endpoint.

Se non è possibile restituire la voce DNS per l'endpoint STS, l'Analizzatore connettività remota restituisce l'avviso seguente:

###  

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Impossibile risolvere il nome host in DNS.</p></td>
</tr>
</tbody>
</table>

Tale messaggio potrebbe indicare uno dei problemi seguenti:

  - Il record host dell'endpoint STS (Security Token Service) non è stato aggiunto al registrar DNS esterno.  
  - Il record host dell'endpoint STS non è ancora stato replicato.  

## Azioni correttive

  - Utilizzare nslookup per verificare che il record Host (A) esista sul server DNS. Per ulteriori informazioni, vedere [Per verificare l'esistenza di record di risorse A nel sistema DNS](http://go.microsoft.com/fwlink/?linkid=63001).  
  - Se il record di risorse host (A) non esiste o non è corretto, aggiungerlo o modificarlo manualmente. Se la zona DNS esterna è ospitata da un provider di terze parti, potrebbe essere necessario contattare tale società o utilizzare strumenti personalizzati per apportare le modifiche al DNS.  

## Ulteriori informazioni

Per ulteriori informazioni sulla risoluzione dei problemi del servizio DNS, vedere la [Risoluzione dei problemi relativi al servizio DNS](http://go.microsoft.com/fwlink/?linkid=63003).

In alcuni casi è necessario verificare l'URL utilizzato dall'endpoint ADFS per la federazione delle identità di Office 365. Per la procedura da seguire per determinare il valore su cui è attualmente impostato l'endpoint, vedere al sezione "Ulteriori informazioni" dell'articolo [Impossibile visualizzare la pagina Web del portale Office 365 in Internet Explorer quando un utente federato tenta di accedere](http://support.microsoft.com/kb/2419389).

