---
title: Certificati intermedi mancanti nella catena
TOCTitle: Certificati intermedi mancanti nella catena
ms:assetid: 91978f64-5800-4514-8c0d-52f1cc57ff71
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Ee410524(v=EXCHG.80)
ms:contentKeyID: 27341568
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Certificati intermedi mancanti nella catena

 

***Ultima modifica dell'argomento:** 2009-09-01*

L'analizzatore di Microsoft Exchange interroga l'oggetto Certificato del server nel sistema di Exchange Server per recuperare varie proprietà dei certificati X509. Per convalidare un determinato certificato X509, l'Analizzatore connettività remota di Exchange deve considerare attendibile l'autorità di certificazione radice che ha emesso il certificato. Se l'Analizzatore connettività remota di Exchange non riesce a seguire la catena dei certificati fino a risalire alla radice affidabile, visualizza un errore di non affidabilità del certificato.

Questo problema potrebbe verificarsi perché manca un certificato intermedio di un'autorità di certificazione sul dispositivo o su Exchange Server con cui è in corso la sincronizzazione.

Questo problema si verifica in genere con i certificati Go Daddy, in quanto manca il certificato CA radice o il certificato CA intermedio dall'archivio certificati sul server con Windows Server 2003 o Windows Server 2008. Questo problema si verifica spesso anche con i certificati VeriSign, in quanto il certificato CA intermedio nell'archivio certificati su Windows Server è scaduto.

I sintomi comuni di questo problema sono:

Quando si cerca di sincronizzare un dispositivo Microsoft Windows Mobile con Exchange ActiveSync per Microsoft Exchange Server 2003 o per Microsoft Exchange Server 2007, la sincronizzazione non riesce e si riceve uno dei seguenti messaggi di errore.

  - Sincronizzazione non riuscita. Il certificato di protezione sul server è scaduto. Controllare che la data e l'ora sul dispositivo siano corrette e riprovare. Codice di errore: 80072f05 o 0x80072f05.  
  - Certificato di protezione sul server non valido. Per installare un certificato valido sul server, rivolgersi all'amministratore di Exchange Server a al provider di servizi Internet. Codice supporto: 80072F0D o 0x80072f0d.  

## Per ulteriori informazioni

È possibile utilizzare l'utilità SSLChainSaver per controllare quali sono i certificati mancanti. Per ulteriori informazioni sull'utilità SSLChainSaver, fare riferimento ai seguenti argomenti:

  - Per avere ulteriori informazioni sull'utilità SSLChainSaver dal team Windows Mobile, vedere i post del blog del team Windows Mobile, "[Introduzione a SslChainSaver](http://go.microsoft.com/fwlink/?linkid=161816)" e "[SSLChainSaver v2](http://go.microsoft.com/fwlink/?linkid=161817)."  
  - Fare clic [qui](http://go.microsoft.com/fwlink/?linkid=161818) per scaricare Windows Mobile SSLChainSaver dal sito di sito di download di Microsoft.  
  - Per ulteriori informazioni su questo problema, vedere l'articolo della Microsoft Knowledge Base, ["Messaggio di errore quando si tenta di sincronizzare un dispositivo Windows Mobile con Exchange ActiveSync per Exchange 2003 o Exchange 2007: 'Sincronizzazione non riuscita'](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=927465)."  

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

