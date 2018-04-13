---
title: Certificati radice di Windows Mobile
TOCTitle: Certificati radice di Windows Mobile
ms:assetid: 9a1ec840-5bff-4add-b20a-8e5970c885fe
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Ee410525(v=EXCHG.80)
ms:contentKeyID: 27341575
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Certificati radice di Windows Mobile

 

_**Ultima modifica dell'argomento:** 2009-09-01_

L'analizzatore di Microsoft Exchange interroga l'oggetto Certificato server nel sistema Exchange Server per recuperare varie proprietà dei certificati X509. Per convalidare un determinato certificato X509, l'Analizzatore connettività remota di Exchange deve considerare attendibile l'autorità di certificazione radice che ha emesso il certificato. Se l'Analizzatore connettività remota di Exchange non riesce a seguire la catena dei certificati fino a risalire alla radice affidabile, visualizza il seguente messaggio di errore.

"Certificato di protezione sul server non valido. Codice supporto: 0x80072f0d."

Generalmente, questo problema si verifica quando il certificato del server Web sul server Accesso client Exchange 2007 è un certificato autofirmato o creato utilizzando una PKI privata o interna. Se si utilizza un certificato autofirmato o creato utilizzando una PKI interna, è necessario installare il certificato radice sul dispositivo mobile. Se questa operazione è già stata eseguita, è possibile scegliere l'opzione "Ignora attendibilità per SSL" nell'Analizzatore connettività remota di Exchange per ignorare questa verifica.

Questo problema può insorgere anche quando la catena di certificati non termina in un certificato radice attendibile nella versione di Windows Mobile in uso.

La tabella che segue mostra quali certificati radice emessi da autorità di certificazione pubbliche vengono forniti con ciascuna versione di Windows Mobile.


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Autorità di certificazione</th>
<th>5.0</th>
<th>5.0 + MSFP</th>
<th>6.0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Thawte Server CA</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Thawte Premium Server CA</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>GTE CyberTrust Root</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>GTE CyberTrust Global Root</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Secure Server Certification Authority (RSA)</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>GlobalSign Root CA</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Entrust.net Secure Server Certification Authority</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Entrust.net Certification Authority (2048)</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Verisign Class 3 Public Primary Certification Authority</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Verisign Class 2 Public Primary Certification Authority</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Equifax Secure Certificate Authority</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>ValiCert Class 2 Policy Validation Authority</p></td>
<td><p>No</p></td>
<td><p>Sì</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>AAA Certificate Services (Comodo CA Limited)</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>AddTrust External CA Root</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Baltimore CyberTrust Root</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="even">
<td><p>Go Daddy Class 2 Certification Authority</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>Sì</p></td>
</tr>
<tr class="odd">
<td><p>Starfield Class 2 Certification Authority</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>Sì</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> Alcune delle autorità di certificazione riportate nella tabella hanno certificati CA firmati da un'altra autorità di certificazione. Sebbene alcuni certificati radice non siano riconosciuti come affidabili sulle versioni meno recenti di Windows Mobile, ciò non significa che i certificati emessi da una determinata società non possano concatenarsi con un certificato radice affidabile su una di quelle versioni di Windows Mobile. Contattare l'autorità di certificazione per sapere a quali certificati radice può concatenarsi il proprio certificato.



## Per ulteriori informazioni

Per ulteriori informazioni sui certificati e le convalide, vedere i seguenti argomenti:

  - Per ulteriori informazioni sull'uso dei certificati per proteggere le comunicazioni tra un client e un server Accesso client, vedere [Concetti relativi a SSL per i server Accesso client](http://go.microsoft.com/fwlink/?linkid=115184).  
  - Per ulteriori informazioni sull'uso dei certificati in Exchange Server 2007, vedere [Utilizzo dei certificati in Exchange Server 2007](http://go.microsoft.com/fwlink/?linkid=119030).  
  - Per ulteriori informazioni sull'uso dei certificati autofirmati in Exchange Server 2007, vedere [Concetti relativi al certificato autofirmato in Exchange 2007](http://go.microsoft.com/fwlink/?linkid=161990).  
  - Per ulteriori informazioni sull'installazione dei certificati radice digitali sui dispositivi mobili, vedere [Come installare certificati in una periferica con tecnologia Windows Mobile](http://go.microsoft.com/fwlink/?linkid=161942).  

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

