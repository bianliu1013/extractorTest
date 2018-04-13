---
title: You must uninstall all interim updates before you install Exchange Server 2010 Service Pack 2
TOCTitle: You must uninstall all interim updates before you install Exchange Server 2010 Service Pack 2
ms:assetid: b206d733-c2f7-4afb-8ffb-227005848013
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Hh696885(v=EXCHG.80)
ms:contentKeyID: 42607553
ms.date: 10/25/2013
mtps_version: v=EXCHG.80
ms.translationtype: HT
---

# You must uninstall all interim updates before you install Exchange Server 2010 Service Pack 2

\[L'obiettivo di questo argomento è risolvere un problema specifico correlato a Exchange Server Analyzer Tool. È applicabile solo ai sistemi su cui è stato eseguito Exchange Server Analyzer Tool e nei quali è stato riscontrato tale problema. Exchange Server Analyzer Tool, che può essere scaricato gratuitamente, raccoglie dati di configurazione in modalità remota da ogni server della topologia e li analizza in modo automatico. Nel rapporto che risulta dall'analisi vengono fornite informazioni dettagliate su importanti problemi di configurazione, problemi potenziali e impostazioni del prodotto non predefinite. I consigli forniti consentono di migliorare le prestazioni, la scalabilità, l'affidabilità e il tempo di attività. Per ulteriori informazioni sullo strumento o per scaricare le versioni aggiornate, vedere "Analizzatori di Microsoft Exchange" all'indirizzo <http://go.microsoft.com/fwlink/?linkid=34707>.\]  

***Ultima modifica dell'argomento:** 2011-11-02*

The Microsoft Exchange Best Practices Analyzer Tool checks whether a Microsoft Exchange Server 2010 interim update (IU) is installed on the computer that is running Exchange 2010. If an IU is installed, Microsoft Exchange Server 2010 Service Pack 2 (SP2) cannot be installed.

To install Exchange 2010 SP2, you must uninstall the IU. After the IU is uninstalled, install Exchange 2010 SP2.

To uninstall the IU, follow these steps:

1.  In **Control Panel**, double-click **Programs and Features**.  
2.  In the **Currently installed programs** list, click **Interim Update for Exchange Server 2010 (KB***xxxxxx***)**, where *xxxxxx* is the Knowledge Base article number that is associated with the IU.  
3.  Click **Remove**.  
4.  At a command prompt, run **sn.exe -Vu \*** to enable strong name verification.  
5.  Run **sn.exe –Vl** to verify that strong name verification is enabled.

