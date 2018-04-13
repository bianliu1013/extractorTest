---
title: Nome certificato SSL non corrispondente
TOCTitle: Nome certificato SSL non corrispondente
ms:assetid: dc668c92-13d9-4c90-9078-1e08971cde45
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439393(v=EXCHG.80)
ms:contentKeyID: 27341607
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Nome certificato SSL non corrispondente

 

***Ultima modifica dell'argomento:** 2011-06-13*

L'Analizzatore Microsoft interroga l'oggetto Certificato server nel sistema Exchange Server per recuperare varie proprietà dei certificati X509. Per ciascun certificato SSL rilevato, l'Analizzatore connettività remota esamina il nome di dominio completo (FQDN) assegnato al certificato. Lo strumento valuta ad esempio www.microsoft.com.

L'Analizzatore connettività remota di Exchange visualizza il seguente avviso se il nome di dominio completo non corrisponde all'indirizzo o all'URL dell'host che il client utilizza per eseguire una connessione con il server.

###  

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Nome certificato SSL non corrispondente</p></td>
</tr>
</tbody>
</table>

L'avviso di nome non corrispondente indica che gli utenti potrebbero non essere in grado di connettersi alle proprie cassette postali utilizzando Outlook via Internet o Exchange ActiveSync per Exchange Server 2007. Se si verifica questo problema, i client di Microsoft Office Outlook 2007 potrebbero ricevere il seguente avviso relativo ai certificati:

###  

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Il nome del certificato di sicurezza non è valido o non corrisponde al nome del sito di destinazione.</p></td>
</tr>
</tbody>
</table>

I dispositivi mobili in genere ricevono un messaggio di errore simile al seguente:

###  

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Certificato di protezione sul server non valido. Codice supporto: 0x80072f0d</p></td>
</tr>
</tbody>
</table>

È possibile ricevere un analogo avviso relativo ai certificati anche durante il test della funzione Single Sign-On in Analizzatore connettività remota. Lo strumento interroga la piattaforma di autenticazione del cloud per individuare l'area di autenticazione. Al termine del processo la piattaforma di autenticazione passa al client richiedente l'URL dell'endpoint ADFS necessario per l'autenticazione del client. Tale endpoint è una connessione SSL (Secure Sockets Layer) dotata di certificato. L'Analizzatore connettività remota valuta il nome di dominio completo (FQDN) assegnato al certificato. Lo strumento valuta ad esempio STS.Contoso.com.

Questo test riguarda il certificato di protezione delle comunicazioni, che non deve essere confuso con il certificato di firma dei token o il certificato di decrittografia dei token utilizzato per la federazione delle identità. Il certificato di firma dei token o il certificato di decrittografia dei token non viene utilizzato per le comunicazioni su SSL. Inoltre, tali certificati possono essere autofirmati. Nella maggior parte dei casi, per consentire il funzionamento del processo di Single Sign-On è necessario che il certificato di protezione delle comunicazioni sia stato emesso da terze parti.

L'Analizzatore connettività remota visualizza l'avviso relativo al certificato se il nome di dominio completo non corrisponde all'indirizzo o all'URL dell'host che il client utilizza per eseguire una connessione con il server. Per risolvere questo problema con Microsoft Office 365, vedere l'articolo 2523494 della Microsoft Knowledge Base, [Quando si tenta di accedere alle risorse di Microsoft Office 365 utilizzando un account federato identità, viene visualizzato un avviso di certificato](http://support.microsoft.com/kb/2523494)

## Per ulteriori informazioni

  - Per ulteriori informazioni sull'effetto di questo errore nei client Outlook 2007, vedere l'articolo 940726 della Microsoft Knowledge Base, [Messaggio di avviso quando si avvia Outlook 2007 e poi ci si connette a una cassetta postale su un server che esegue Exchange Server 2007 o Exchange Server 2010: "Il nome del certificato di sicurezza non è valido o non corrisponde al nome del sito di destinazione" (le informazioni potrebbero essere in lingua inglese)](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=940726).  
  - Per ulteriori informazioni sull'effetto di questo errore sui dispositivi mobili connessi utilizzando Exchange ActiveSync, vedere [Installazione dei certificati SSL su un dispositivo mobile Windows](http://go.microsoft.com/fwlink/?linkid=161942).  
  - Per informazioni sull'utilizzo dei certificati con server virtuali in Exchange Server 2003, vedere l'articolo 823024 della Microsoft Knowledge Base, [Utilizzo dei certificati con server virtuali in Exchange Server 2003 (le informazioni potrebbero essere in lingua inglese)](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=823024).  
  - Per ulteriori informazioni su come utilizzare i certificati SSL con i server Accesso client Exchange 2007, vedere [White Paper: Accesso client di Exchange 2007 e i certificati SSL](http://go.microsoft.com/fwlink/?linkid=161943).  

L'Analizzatore connettività remota di Exchange è un nuovo strumento per cui è attualmente disponibile documentazione limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati fino a questo punto. Se è necessaria assistenza tecnica, creare un post nel forum appropriato dell'[Analizzatore connettività remota](http://go.microsoft.com/fwlink/?linkid=73420) oppure contattare il Servizio Supporto Tecnico Clienti Microsoft in [Correggere un problema tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

