---
title: Exchange ActiveSync ha restituito l'errore HTTP 500
TOCTitle: Exchange ActiveSync ha restituito l'errore HTTP 500
ms:assetid: 620c5ce8-3595-4658-9a7a-ec76c10e4a69
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dd439375(v=EXCHG.80)
ms:contentKeyID: 27341553
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Exchange ActiveSync ha restituito l'errore HTTP 500

 

_**Ultima modifica dell'argomento:** 2010-06-25_

L'analizzatore di Microsoft Exchange invia i comandi Exchange ActiveSync per verificare lo stato della connettività di Exchange ActiveSync. Se il comando FolderSync (il primo nella sequenza) restituisce l'errore HTTP 500, l'Analizzatore connettività remota di Microsoft Exchange Server restituisce il seguente messaggio di errore.

"Exchange ActiveSync ha restituito una risposta HTTP 500."

## Per ulteriori informazioni

Questo errore può verificarsi se si utilizza un server Exchange 2003 senza un server front-end e si sceglie un'autenticazione basata su moduli o SSL. In questo caso, vedere l'articolo della Microsoft Knowledge Base che illustra gli errori di Exchange ActiveSync e Outlook Mobile Access che si verificano quando per Exchange Server 2003 è necessaria un'autenticazione SSL o basata su moduli ([http://go.microsoft.com/fwlink/?linkid=3052\&kbid=817379](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=817379)).

In Exchange 2003, per ActiveSync è necessario che l'autenticazione Kerberos funzioni correttamente tra i server front-end e back-end. Di seguito sono indicati alcuni dei motivi per cui l'autenticazione Kerberos può non funzionare in IIS:

  - L'autenticazione Windows integrata potrebbe non essere abilitata sulla directory virtuale "/Exchange" del server back-end.  
  - Gli utenti interessati potrebbero essere membri di troppi gruppi e ciò potrebbe far sì che i loro token superino il numero massimo consentito.  

    > [!NOTA]
    > I metodi di autenticazione sulle directory virtuali di Exchange Server devono essere gestiti tramite il Gestore di sistema di Exchange e non Gestione Internet Information Services (IIS).



Per ulteriori informazioni, vedere l'articolo della Microsoft Knowledge Base che illustra come risolvere gli errori HTTP nel server ActiveSync ([http://go.microsoft.com/fwlink/?linkid=3052\&kbid=330463](http://go.microsoft.com/fwlink/?linkid=3052%26kbid=330463)).

Questo problema può verificarsi anche in Exchange Server 2010, se il gruppo Exchange Servers non dispone dell'autorizzazione appropriata per l'oggetto cassetta postale in Active Directory. Questo problema è in genere dovuto all'interruzione dell'ereditarietà dell'elenco di controllo di accesso (ACL) in Active Directory.

Per verificare se l'ereditarietà è disabilitata per l'utente:

1.  Aprire **Utenti e computer di Active Directory**.  
2.  Scegliere **Visualizza** \> **Funzionalità avanzate** dal menu disponibile nella parte superiore della console.  
3.  Individuare l'account della cassetta postale nella console, fare clic su di esso con il pulsante destro del mouse e scegliere **Proprietà**.  
4.  Fare clic sulla scheda **Sicurezza**.  
5.  Fare clic su **Avanzate**.  
6.  Verificare che la casella di controllo per "Includi le autorizzazioni ereditabili del padre dell'oggetto" sia selezionata.  

Se l'utente è membro di determinati gruppi protetti, ad esempio Domain Administrators, è normale che tale casella di controllo sia deselezionata. Se si verificano problemi con i membri di questi gruppi protetti, verificare le autorizzazioni per l'oggetto AdminSDHolder.


> [!NOTA]
> È consigliabile evitare di utilizzare per la posta elettronica account appartenenti a gruppi protetti. Se sono necessari i diritti concessi da un gruppo protetto, è consigliabile utilizzare due account utente di Active Directory, ovvero un account utente aggiunto a un gruppo protetto e un account utente utilizzato ai fini della posta elettronica e per tutte le altre operazioni.



Per ulteriori informazioni, vedere l'articolo di TechNet Magazine "AdminSDHolder, gruppi protetti e SDPROP" (<http://technet.microsoft.com/it-it/magazine/2009.09.sdadminholder.aspx>).

L'Analizzatore connettività remota di Exchange è un nuovo strumento per il quale, al momento, la documentazione disponibile è piuttosto limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community (in basso) per segnalare eventuali errori riscontrati a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/?linkid=8158).

