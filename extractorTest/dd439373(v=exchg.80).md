---
title: Errore "Accesso negato" generato dal runtime RPC
TOCTitle: Errore "Accesso negato" generato dal runtime RPC
ms:assetid: 5aca79d9-1348-4390-ad70-9ff424ed7052
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439373(v=EXCHG.80)
ms:contentKeyID: 27341548
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# Errore "Accesso negato" generato dal runtime RPC

 

***Ultima modifica dell'argomento:** 2010-08-26*

Lo strumento Microsoft Exchange Best Practices Analyzer invia un ping RPC a ogni interfaccia RPC utilizzata da Microsoft Office Outlook per connettersi al server cassette postali. Quando la richiesta ping RPC ha esito negativo e indica uno stato RPC 0x5, l'Analizzatore connettività remota di Exchange visualizza il messaggio di errore seguente:

Errore (0x5) "Accesso negato" generato dal runtime RPC

## Per ulteriori informazioni

**Per correggere questo errore**

1.  Analizzare il livello di autenticazione di LAN Manager (LMCompatibilityLevel) nei client Outlook, nei server Exchange e nei server di catalogo globale. Verificare tali impostazioni per accertarsi che la combinazione configurata sia compatibile.

2.  Verificare che la funzionalità di replica venga eseguita correttamente tra i controller di dominio. Ciò è particolarmente importante se si hanno più domini nella foresta. Verificare i registri del servizio directory sui controller di dominio e utilizzare lo strumento DCDIAG per controllare se sui controller si sono verificati degli errori.

3.  Verificare la disponibilità di autorizzazioni utente appropriate per il server back-end e la cassetta postale di Exchange. Per effettuare correttamente l'accesso, ad esempio, è necessario disporre dell'autorizzazione di accesso al computer dalla rete.

Per ulteriori informazioni su come configurare le impostazioni di sicurezza riportate in questo argomento, vedere l'articolo della Microsoft Knowledge Base [Incompatibilità tra client, servizi e programmi che possono verificarsi quando si modificano le impostazioni di protezione e le assegnazioni di diritti utente](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=823659).

Per ulteriori informazioni su come utilizzare lo strumento DCDIAG per l'analisi, vedere [Panoramica su Dcdiag](http://go.microsoft.com/fwlink/?linkid=68936).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per cui è attualmente disponibile documentazione limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per fornire informazioni sugli errori riscontrati fino a questo punto. Se è necessaria assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

