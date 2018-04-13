---
title: Autenticazione reciproca definita dal nome alternativo oggetto
TOCTitle: Autenticazione reciproca definita dal nome alternativo oggetto
ms:assetid: a15f34b1-a7bf-4f44-9142-0c5c3174cb0f
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Hh849187(v=EXCHG.80)
ms:contentKeyID: 45478516
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Autenticazione reciproca definita dal nome alternativo oggetto

 

***Ultima modifica dell'argomento:** 2012-02-07*

L'analizzatore connettività remota di Microsoft Exchange negozia una connessione SSL con l'host remoto per recuperare varie proprietà dei certificati X509. Lo strumento valuta l'attributo Oggetto e l'estensione Nome alternativo oggetto per identificare i nomi entità assegnati al certificato (ad esempio, mail.contoso.com).

Se il nome comune del certificato non corrisponde alla stringa di autenticazione reciproca (msstd:), ottenuta dall'analizzatore connettività remota durante il test funzionale di Microsoft Outlook via Internet, ma una delle estensioni del nome alternativo oggetto corrisponde alla stringa di autenticazione reciproca, lo strumento visualizza il seguente messaggio di errore:

"Il nome comune del certificato non corrisponde alla stringa di autenticazione reciproca fornita; tuttavia, è stata rilevata una corrispondenza nell'estensione del nome alternativo oggetto."

La stringa di autenticazione reciproca corrisponde all'impostazione "Connetti solo a server proxy con il seguente nome entità nel certificato" nella finestra di dialogo **Impostazioni proxy Exchange** di Outlook. Il componente RPC (Remote Procedure Call) di Windows utilizza questo valore per convalidare il certificato. Prima di Windows Vista Service Pack 1, la piattaforma Windows convalidava la stringa di autenticazione reciproca solo rispetto al nome comune del certificato e non rispetto ai nomi alternativi oggetto.

Con questa configurazione, potrebbero insorgere i seguenti sintomi sui client Windows XP e Windows Vista RTM.

  - Agli utenti vengono ripetutamente richieste le credenziali senza che riescano a connettersi a Microsoft Exchange Server tramite Outlook via Internet.  
  - Se si consente ad Outlook 2007 di creare un profilo Outlook tramite l'individuazione automatica, viene visualizzato il seguente messaggio di errore:  
    Non è disponibile alcuna connessione crittografata al server di posta elettronica. Fare clic su Avanti per tentare di utilizzare una connessione non crittografata.

Se si decide di supportare solo i client con Windows Vista Service Pack 1 e le versioni più recenti di Windows, è possibile ignorare questo avviso.

## Per ulteriori informazioni

  - Per ulteriori informazioni su questo problema, vedere [Impossibile stabilire un'autenticazione reciproca](dd439371\(v=exchg.80\).md).  
  - Per ulteriori informazioni sui nomi entità dell'autenticazione reciproca, vedere [Nomi entità](http://go.microsoft.com/fwlink/?linkid=93417).  
  - Per informazioni aggiuntive sui provider di Exchange 2007 Outlook, vedere il seguente argomento e relativo articolo sul blog del team di Microsoft Exchange:  
      - [Set-OutlookProvider](http://go.microsoft.com/fwlink/?linkid=161815)  
      - [Funzionamento del servizio di individuazione automatica e dei provider di Outlook](http://go.microsoft.com/fwlink/?linkid=161811)  

L'Analizzatore connettività remota di Exchange è un nuovo strumento per cui è attualmente disponibile documentazione limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

