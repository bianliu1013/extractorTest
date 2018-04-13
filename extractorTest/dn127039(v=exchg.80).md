---
title: 'Test MCA: Impossibile visualizzare le informazioni sulla disponibilità di un altro utente'
TOCTitle: 'Test MCA: Impossibile visualizzare le informazioni sulla disponibilità di un altro utente'
ms:assetid: 4ec87a51-fc6e-477f-8ccf-7520f64193fd
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Dn127039(v=EXCHG.80)
ms:contentKeyID: 53089510
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
_tocRel: dd439364(v=exchg.80)/toc.json
ms.translationtype: HT
---

# Test MCA: Impossibile visualizzare le informazioni sulla disponibilità di un altro utente

 

_**Ultima modifica dell'argomento:** 2013-02-21_

L'analizzatore connettività di Microsoft include il test **Impossibile visualizzare le informazioni sulla disponibilità di un altro utente**. Questo test verifica che una cassetta postale di Office 365 possa accedere alle informazioni sulla disponibilità di una cassetta postale locale e viceversa.

Il test include le seguenti funzionalità:

  - Un controllo per verificare che l'ora di sistema del server ibrido non sia sfalsata di più di cinque minuti. Se lo sfalsamento supera i cinque minuti, si verificano degli errori quando Microsoft Federation Gateway richiede i token di delega.  
  - Un controllo per verificare che la connettività al server ibrido in ingresso non richieda una preautenticazione del firewall. Il firewall deve consentire l'autenticazione pass-through. Questo controllo è utile quando il client MCA viene eseguito dall'esterno della rete aziendale.  
  - Un controllo per verificare che il server ibrido supporti i requisiti minimi per la versione di Exchange Server.  
  - Una query di base sulla disponibilità rispetto al servizio di disponibilità di destinazione.  
  - Collegamenti alle istruzioni sulla procedura guidata di configurazione ibrida. Questa procedura guidata è una comune fonte di potenziali errori di configurazione nella distribuzione ibrida.  

L'analizzatore connettività remota di Microsoft è un nuovo strumento per cui è attualmente disponibile una documentazione limitata. Nell'ottica di un continuo miglioramento della documentazione disponibile, Microsoft si affida a tutti gli utenti della community per la segnalazione degli eventuali errori rilevati. Utilizzare la sezione Contenuti Community più avanti per segnalare eventuali altri motivi che potrebbero aver provocato gli errori riscontrati fino a questo punto. Se si ha bisogno di assistenza tecnica, creare un post nel [forum TechNet per Exchange](http://go.microsoft.com/fwlink/p/?linkid=73420) appropriato oppure contattare il [supporto tecnico](http://go.microsoft.com/fwlink/p/?linkid=8158).

