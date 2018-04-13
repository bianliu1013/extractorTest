---
title: Errore Server RPC non disponibile generato dal runtime RPC
TOCTitle: Errore Server RPC non disponibile generato dal runtime RPC
ms:assetid: db543644-c252-47ee-a70b-4f60770083dc
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439392(v=EXCHG.80)
ms:contentKeyID: 27341605
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Errore Server RPC non disponibile generato dal runtime RPC

 

_**Ultima modifica dell'argomento:** 2010-08-20_

Lo strumento Microsoft Exchange Best Practices Analyzer invia un comando RPCPing a diversi endpoint Exchange Server per simulare le connessioni che vengono stabilite quando un client Microsoft Outlook si connette a Microsoft Exchange Server 2007 tramite Outlook via Internet o a Microsoft Exchange Server 2003 tramite RPC su HTTP. Per connettersi, il client deve essere prima in grado di connettersi agli endpoint HTTP dell'Archivio informazioni di Microsoft Exchange, al servizio di riferimento DSProxy all'interno del servizio Supervisore sistema di Microsoft Exchange e al servizio DSProxy all'interno del servizio Supervisore sistema di Microsoft Exchange tramite le porte 6001, 6002 e 6004, rispettivamente. Se il test ha esito negativo, l'Analizzatore connettività remota di Exchange genera il messaggio di errore seguente:

Errore (1722) "Server RPC non disponibile" generato dal runtime RPC

Il problema può essere dovuto a una delle condizioni seguenti:

  - Errori nella risoluzione dei nomi DNS  
  - Chiave ValidPorts mancante o non valida nel Registro di sistema del server Accesso client Exchange 2007 con accesso a Internet o del server Exchange 2003  
  - Servizi di Exchange non in ascolto sugli endpoint richiesti  
  - Firewall che bloccano le porte richieste  

## Per ulteriori informazioni

Per risolvere il problema, fare quanto segue:

  - Risolvere i problemi relativi alla risoluzione dei nomi e verificare che il server utilizzato come proxy RPC sia in grado di risolvere correttamente il nome di dominio completo (FQDN) interno del server cassette postali o di Exchange 2003.  
  - Aprire l'Editor del Registro di sistema nel server Accesso client o nel server front-end e verificare che il valore ValidPorts del Registro di sistema esista nella chiave HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Rpc\\Rpcproxy. Verificare inoltre che la chiave includa il nome NetBIOS e il nome di dominio completo (FQDN) per tutti i server cassette postali e per ogni porta richiesta (ovvero, per le porte 6001, 6002 e 6004).  
  - Per verificare la connettività agli endpoint, aprire una sessione Telnet sul server Accesso client o sul server front-end, quindi stabilire una connessione Telnet con ogni porta dei server cassette postali (ovvero, per le porte 6001, 6002 e 6004). Se non è possibile stabilire correttamente una connessione Telnet a una delle porte e i server sono separati da un firewall, controllare la configurazione del firewall.  
  - Se si riceve l'errore sulla porta 6004 e si utilizza Exchange 2007 su Windows Server 2008, verificare che sia installato Exchange 2007 SP1 RU4 o versione successiva. È infatti presente un problema di IPv6 che può impedire l'esecuzione delle richieste DSProxy e generare questo errore. Per ulteriori informazioni su questo specifico problema, vedere Articolo della Microsoft Knowledge Base, "[Vengono chieste le credenziali dell'utente tre volte e viene visualizzato un messaggio di errore quando si utilizza la funzione Outlook via Internet per connettersi a un server di Exchange Server 2007 Service Pack 1 su cui è in esecuzione Windows Server 2008](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=950138)".  


> [!NOTA]
> La modifica del valore ValidPorts non si applica a Microsoft Exchange Server 2010. In Exchange 2010, il valore del Registro di sistema è ValidPorts_Exchange. Tale valore non deve essere modificato manualmente, perché viene creato dalla configurazione automatica nelle impostazioni del server Accesso Client.



## Risorse aggiuntive

  - Per ulteriori informazioni sulla risoluzione dei problemi del servizio DNS, vedere la [Risoluzione dei problemi relativi al servizio DNS](http://go.microsoft.com/fwlink/?linkid=63003).  
  - Per ulteriori informazioni su Outlook via Internet in Exchange 2007 e la chiave ValidPorts, vedere [Funzionamento di Outlook via Internet e problemi nel funzionamento (le informazioni potrebbero essere in lingua inglese)](http://go.microsoft.com/fwlink/?linkid=148104)  
  - Per ulteriori informazioni su RPC su HTTP in Exchange 2003 e la chiave ValidPorts, vedere [Interazioni di RPC su HTTP nel server proxy RPC](http://go.microsoft.com/fwlink/?linkid=161819).  
  - Per verificare un'altra opzione per la soluzione dei problemi di connettività di Outlook via Internet con Exchange 2007 SP1 su Windows Server 2008, vedere [Problemi di connettività del client Outlook via Internet a causa di TCP/IPv6](http://go.microsoft.com/fwlink/?linkid=161821).  

L'Analizzatore connettività remota di Exchange è un nuovo strumento per cui è attualmente disponibile documentazione limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per fornire informazioni sugli errori riscontrati fino a questo punto. Se è necessaria assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

