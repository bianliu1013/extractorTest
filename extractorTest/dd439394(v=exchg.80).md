---
title: Errore di attendibilità del certificato SSL
TOCTitle: Errore di attendibilità del certificato SSL
ms:assetid: e455c7b2-3e8e-4a45-83e7-09c55ff3b4ec
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439394(v=EXCHG.80)
ms:contentKeyID: 27341609
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Errore di attendibilità del certificato SSL

 

_**Ultima modifica dell'argomento:** 2011-06-21_

L'Analizzatore connettività remota Microsoft interroga l'oggetto Certificato server nel sistema Exchange Server per recuperare varie proprietà dei certificati X509. Per convalidare un determinato certificato X509, l'Analizzatore connettività remota deve considerare attendibile l'autorità di certificazione radice che ha emesso il certificato. Se lo strumento non riesce a seguire la catena dei certificati fino alla radice attendibile, visualizza un errore di certificato non attendibile.

Generalmente, questo problema si verifica quando il certificato del server Web sul Server Accesso client è un certificato autofirmato o è stato creato utilizzando una PKI privata o interna. Il problema può verificarsi anche quando i certificati sono concatenati a un server Accesso client da un altro certificato intermedio. Affinché il certificato possa essere considerato valido, deve essere valido ogni certificato lungo il percorso di certificazione.

I sintomi comuni di questo problema sono:

  - Gli utenti devono immettere ripetutamente le credenziali, ma non riescono a connettersi utilizzando Outlook via Internet.  
  - Quando un utente tenta di connettersi a Outlook Web Access, viene visualizzato il messaggio di errore seguente: È stato rilevato un problema relativo al certificato di sicurezza del sito Web.  

L'Analizzatore connettività remota è in grado di ignorare il requisito di attendibilità durante la convalida del certificato SSL per la maggior parte dei test. Tuttavia, i test di connettività di Outlook via Internet (RPC su HTTP) richiedono attualmente un certificato pubblico attendibile, che sia considerato attendibile anche dal server.

Se si esegue il test della funzionalità Single Sign-on per Microsoft Office 365, potrebbe verificarsi un problema analogo, in cui agli utenti vengono continuamente richieste le credenziali quando tentano di accedere ai servizi Office 365. L'Analizzatore connettività remota interroga la piattaforma di autenticazione del cloud per individuare l'area di autenticazione. Al termine del processo la piattaforma di autenticazione passa al client richiedente l'URL dell'endpoint ADFS necessario per l'autenticazione del client. Tale endpoint è una connessione SSL (Secure Sockets Layer) dotata di certificato. L'Analizzatore connettività remota valuta il nome di dominio completo (FQDN) assegnato al certificato. Lo strumento valuta ad esempio STS.Contoso.com.

L'Analizzatore connettività remota visualizza un avviso quando il certificato utilizzato per SSL non può essere considerato attendibile fino alla radice. Questo messaggio indica che il certificato non è considerato attendibile dall'ambiente Office 365. Questo errore è spesso dovuto al fatto che il certificato è autofirmato e non è pertanto valido per questo tipo di autenticazione. Per risolvere questo problema con il test della funzione Single Sign-On, vedere l'articolo 2523494 della Microsoft Knowledge Base, [Quando si tenta di accedere alle risorse di Microsoft Office 365 utilizzando un account federato identità, viene visualizzato un avviso di certificato](http://support.microsoft.com/kb/2523494)

## Per ulteriori informazioni

Per ulteriori informazioni su certificati e convalida, vedere i seguenti argomenti.

  - Per ulteriori informazioni sull'uso dei certificati per proteggere le comunicazioni tra un client e un server Accesso client, vedere [Concetti relativi a SSL per i server Accesso client](http://go.microsoft.com/fwlink/?linkid=115184).  
  - Per ulteriori informazioni sull'uso dei certificati in Exchange Server 2007, vedere [Utilizzo dei certificati in Exchange Server 2007](http://go.microsoft.com/fwlink/?linkid=119030).  
  - Per ulteriori informazioni sull'uso dei certificati autofirmati in Exchange Server 2007, vedere [Concetti relativi al certificato autofirmato in Exchange 2007](http://go.microsoft.com/fwlink/?linkid=161990).  
  - Per ulteriori informazioni sull'utilizzo delle autorità di certificazione private e non Microsoft quando si pianifica la distribuzione del servizio di individuazione automatica, vedere [White Paper: Servizio di individuazione automatica di Exchange 2007](http://go.microsoft.com/fwlink/?linkid=157773).

