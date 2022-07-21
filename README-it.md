# ![DSS](images/en_US/readme/DSS_logo.png)

[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)

| inglese [中文](README-ZH.md)

## Introduzione

       DataSphere Studio (DSS in breve) è WeDataSphere, un portale di gestione dello sviluppo di applicazioni di dati one-stop sviluppato da WeBank.

       Con il design del framework integrato collegabile e Linkis, un middleware di elaborazione, DSS può facilmente integrare vari sistemi applicativi di dati di livello superiore, rendendo lo sviluppo dei dati semplice e facile da usare.

       DataSphere Studio è posizionato come un portale di sviluppo di applicazioni dati e il ciclo chiuso copre l'intero processo di sviluppo di applicazioni di dati. Con un'interfaccia utente unificata, l'esperienza di sviluppo drag-and-drop grafico simile al flusso di lavoro soddisfa l'intero ciclo di vita dello sviluppo di applicazioni di dati dall'importazione dei dati, alla pulizia della desensibilizzazione, all'analisi dei dati, al data mining, all'ispezione della qualità, alla visualizzazione, alla pianificazione delle applicazioni di output dei dati, ecc.

       Con le funzionalità di connessione, riusabilità e semplificazione di Linkis, DSS nasce con funzionalità di livello finanziario di elevata concorrenza, alta disponibilità, isolamento multi-tenant e gestione delle risorse.

## Anteprima dell'interfaccia utente

       Si prega di essere pazienti, ci vorrà del tempo per caricare gif.

![DSS-V1.0 GIF](images/en_US/readme/DSS_gif.gif)

## Caratteristiche principali

### 1. Interfaccia utente di gestione dello sviluppo di applicazioni completa e completa

       DSS è altamente integrato. I componenti attualmente integrati includono(**Compatibilità della versione DSS per i componenti di cui sopra, visitare: [Elenco di compatibilità dei componenti integrati](README.md#4-integrated-data-application-components)**):

       1. Strumento IDE per lo sviluppo dei dati - [Scriptis](https://github.com/WeBankFinTech/Scriptis)

       2. Strumento di visualizzazione dei dati - [Visualis](https://github.com/WeBankFinTech/Visualis) (Basato sul progetto open source [Davinci ·](https://github.com/edp963/davinci) contributo di CreditEase)

       3. Strumento di gestione della qualità dei dati - [Qualitis](https://github.com/WeBankFinTech/Qualitis)

       4. Strumento di pianificazione del flusso di lavoro - [Schedulis](https://github.com/WeBankFinTech/Schedulis)

       5. Strumento di scambio dati - [Scambio](https://github.com/WeBankFinTech/Exchangis)

       6. Servizio Api dati - [DataApiService](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Using_Document/DataApiService_Usage_Documentation.md)

       7. Strumento di gestione dello sviluppo di applicazioni in streaming - [Streamis ·](https://github.com/WeBankFinTech/Streamis)

       8. Piattaforma di apprendimento automatico one-stop - [Prophecis](https://github.com/WeBankFinTech/Prophecis)

       9. Strumento di pianificazione delle attività del flusso di lavoro - DolphinScheduler (**Nell'unione di codice**)

       10. Documentazione di aiuto e guida per principianti - Guida per l'utente (**Nell'unione di codice**)

       11. Data Model Center - DataModelCenter (**In fase di sviluppo**)

       **Compatibilità della versione DSS per i componenti di cui sopra, visitare: [Elenco di compatibilità dei componenti integrati](README.md#4-integrated-data-application-components)**.

       Con un'architettura framework collegabile, DSS è progettato per consentire agli utenti di integrare rapidamente nuovi strumenti applicativi per i dati o sostituire vari strumenti integrati da DSS. Ad esempio, sostituisci Scriptis con Zeppelin e sostituisci Schedulis con DolphinScheduler...

![DSS one-stop video](images/en_US/readme/onestop.gif)

### 2. AppConn, basato su Linkis, definisce un concetto di design unico

       AppConn è il concetto di base che consente a DSS di integrare facilmente e rapidamente vari sistemi Web di livello superiore.

       AppConn, un connettore di applicazioni, definisce un set di protocolli di integrazione unificati front-end e back-end a tre livelli, consentendo ai sistemi applicativi di dati esterni di diventare facilmente e rapidamente parte dello sviluppo di applicazioni di dati DSS.

       Le specifiche a tre livelli di AppConn sono: la specifica SSO di primo livello, la specifica della struttura organizzativa di secondo livello e la specifica del processo di sviluppo di terzo livello.

       DSS organizza più AppConn in serie per formare un flusso di lavoro che supporti l'esecuzione in tempo reale e l'esecuzione pianificata. Gli utenti possono completare l'intero processo di sviluppo delle applicazioni dati con semplici operazioni di trascinamento della selezione.

       Poiché AppConn è integrato con Linkis, il sistema di applicazioni dati esterne condivide le funzionalità di gestione delle risorse, limitazione simultanea e prestazioni elevate. AppConn consente anche un contesto condivisibile a livello di sistema e quindi rende l'applicazione di dati esterni completamente lontana dai silos delle applicazioni.

### 3. Spazio di lavoro, come unità di gestione

       Con Workspace come unità di gestione, organizza e gestisce le applicazioni aziendali di vari sistemi di applicazioni dati, definisce un set di standard comuni per lo sviluppo collaborativo di aree di lavoro tra sistemi di applicazioni dati e fornisce funzionalità di gestione dei ruoli utente.

### 4. Componenti integrati dell'applicazione dati

       DSS ha integrato una varietà di sistemi applicativi di dati di livello superiore implementando più AppConn, che possono fondamentalmente soddisfare le esigenze di sviluppo dei dati degli utenti.

       **Se lo si desidera, è inoltre possibile integrare facilmente nuovi sistemi di applicazioni dati per sostituire o arricchire il processo di sviluppo di applicazioni dati di DSS.** [Clicca su di me per scoprire come integrare rapidamente nuovi sistemi applicativi](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Development_Documentation/Third-party_System_Access_Development_Guide.md)

| | dei componenti Descrizione | DSS0. Versione compatibile X (consigliato DSS0.9.1) | Versione compatibile con DSS1.0 (consigliato DSS1.1.0) |
| --------------- | -------------------------------------------------------------------- | --------- | ---------- |
| [**Linkis ·**](https://github.com/apache/incubator-linkis) | Elaborazione middleware Apache Linkis, fornendo interfacce standard come REST / WebSocket / JDBC / SDK, le applicazioni di livello superiore possono facilmente connettersi e accedere ai motori sottostanti come MySQL / Spark / Hive / Presto / Flink. | Si consiglia Linkis0.11.0 (\**Rilasciato* \*) | >= Linkis1.1.1 (**Rilasciato**) |
| [**DataApiService**](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Using_Document/DataApiService_Usage_Documentation.md)  | (DSS ha strumenti applicativi di terze parti incorporati) servizio API dati. Lo script SQL può essere rapidamente pubblicato come interfaccia Restful, fornendo funzionalità di accesso Rest al mondo esterno. | | non supportati DSS1.1.0 consigliato (**Rilasciato**)|
| [**Scriptis**](https://github.com/WeBankFinTech/DataSphereStudio) | (DSS ha strumenti applicativi di terze parti integrati) supporta la scrittura online di SQL, Pyspark, HiveQL e altri script e invia allo strumento Web di analisi dei dati \[Linkis] (https ://github.com/WeBankFinTech/Linkis). | DSS0.9.1 consigliato (**Rilasciato**) | DSS1.1.0 consigliato (**Rilasciato**) |
| [**Schedulis**](https://github.com/WeBankFinTech/Schedulis) | Sistema di pianificazione delle attività del flusso di lavoro basato sullo sviluppo secondario Azkaban, con funzionalità di livello finanziario come prestazioni elevate, alta disponibilità e isolamento delle risorse multi-tenant. | Schedulis0.6.1 consigliato (**Rilasciato**) | >= Schedulis0.7.0 (**Rilasciato**) |
| **Controllo eventi** | (uno strumento applicativo di terze parti integrato in DSS) fornisce funzionalità di comunicazione del segnale in tutte le aziende, l'ingegneria e il flusso di lavoro. | DSS0.9.1 consigliato (**Rilasciato**) | DSS1.1.0 consigliato (**Rilasciato**) |
| **InviaEmail** | (DSS ha strumenti applicativi di terze parti integrati) offre la possibilità di inviare dati, tutti i set di risultati di altri nodi del flusso di lavoro possono essere inviati via e-mail | DSS0.9.1 è consigliato (**Rilasciato**) | DSS1.1.0 consigliato (**Rilasciato**) |
| [**Qualitis**](https://github.com/WeBankFinTech/Qualitis) | Strumento di verifica della qualità dei dati, che fornisce funzionalità di verifica dei dati come l'integrità e la correttezza dei dati | Qualitis0.8.0 è consigliato (\*\*Rilasciato \*\*) | >= Qualitis0.9.2 (**Rilasciato**) |
| [**Streamis ·**](https://github.com/WeBankFinTech/Streamis) | Strumento di gestione dello sviluppo di applicazioni in streaming. Supporta il rilascio di Flink Jar e Flink SQL e fornisce le funzionalità di sviluppo, debug e gestione della produzione di applicazioni di streaming, come ad esempio: start-stop, monitoraggio dello stato, checkpoint, ecc. | | non supportati >= Streamis0.2.0 (**Rilasciato**) |
| [**Prophecis**](https://github.com/WeBankFinTech/Prophecis) | Una piattaforma di machine learning one-stop che integra più framework di machine learning open source. MLFlow di Prophecis può essere collegato al flusso di lavoro DSS tramite AppConn. | | non supportati >= Profezia 0.3.2 (**Rilasciato**) |
| [**Scambio**](https://github.com/WeBankFinTech/Exchangis) | Una piattaforma di scambio dati che supporta la trasmissione di dati tra fonti di dati eterogenee strutturate e non strutturate, l'imminente Exchangis1. 0, funzionerà con il flusso di lavoro DSS | | non supportati = Exchangis1.0.0 (**Rilasciato**) |
| [**Visualis**](https://github.com/WeBankFinTech/Visualis) | Uno strumento di BI di visualizzazione dei dati basato sullo sviluppo secondario di Davinci, un progetto open source di CreditEase, fornisce agli utenti funzionalità di visualizzazione dei dati a livello finanziario in termini di sicurezza dei dati. | Visualis0.5.0 consigliato |= Visualis1.0.0 (**Rilasciato**) |
| [**DolphinScheduler**](https://github.com/apache/dolphinscheduler) | Apache DolphinScheduler, una piattaforma di pianificazione delle attività del flusso di lavoro visivo distribuita e facilmente scalabile, supporta la pubblicazione con un clic dei flussi di lavoro DSS su DolphinScheduler. | | non supportati DolphinScheduler1.3.X (**Rilasciato**) |
| **Guida per l'utente** | (DSS sarà integrato in strumenti applicativi di terze parti) contiene documenti di aiuto, guida per principianti, skinning in modalità scura, ecc. | | non supportati >= DSS1.1.0 (**Rilasciato**) |
| **DataModelCenter** | (lo strumento applicativo di terze parti che DSS costruirà) fornisce principalmente funzionalità di pianificazione del data warehouse, sviluppo di modelli di dati e gestione delle risorse di dati. La pianificazione del data warehouse include domini soggetti, gerarchie di data warehouse, modificatori, ecc.; lo sviluppo di modelli di dati include indicatori, dimensioni, metriche, creazione di tabelle basate su procedure guidate, ecc.; le risorse di dati sono collegate ad Apache Atlas per fornire funzionalità di derivazione dei dati. | | non supportati Pianificato in DSS1.2.0 (**in fase di sviluppo**) |
| **UserManager** | (DSS ha strumenti applicativi di terze parti integrati) inizializza automaticamente tutti gli ambienti utente necessari per un nuovo utente DSS, tra cui: creazione di utenti Linux, vari percorsi utente, autorizzazione directory, ecc. | DSS0.9.1 consigliato (**Rilasciato**) | pianificazione |
| [**Flusso d' aria**](https://github.com/apache/airflow) | Supporta la pubblicazione di flussi di lavoro DSS su Apache Airflow per la pianificazione pianificata. | PR non ancora fusa | | non supportati

## Ambiente Demo Trial

       La funzione di DataSphere Studio che supporta l'esecuzione di script presenta elevati rischi per la sicurezza e l'isolamento dell'ambiente WeDataSphere Demo non è stato completato. Considerando che molti utenti stanno chiedendo informazioni sull'ambiente Demo, abbiamo deciso di rilasciare prima i codici di invito alla comunità e accettare le domande di prova da aziende e organizzazioni.

       Se si desidera provare l'ambiente Demo, partecipare al gruppo di utenti della community di DataSphere Studio (**Si prega di fare riferimento alla fine del documento**), e contatto **Robot del gruppo WeDataSphere** per ottenere un codice di invito.

       Pagina di registrazione utente dell'ambiente Demo di DataSphereStudio: [clicca su di me per entrare](https://dss-open.wedatasphere.com/#/register)

       Pagina di accesso all'ambiente Demo di DataSphereStudio: [clicca su di me per entrare](https://dss-open.wedatasphere.com/#/login)

## Scaricare

       Si prega di andare al [Pagina delle versioni di DSS](https://github.com/WeBankFinTech/DataSphereStudio/releases) per scaricare una versione compilata o un pacchetto di codice sorgente di DSS.

## Compilare e distribuire

       Si prega di seguire [Compila la guida](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Development_Documentation/Compilation_Documentation.md) per compilare DSS dal codice sorgente.

       Si prega di fare riferimento a [Documenti di distribuzione](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Installation_and_Deployment/DSS%26Linkis_one-click_deployment_document_stand-alone_version.md) per eseguire la distribuzione.

## Esempi e linee guida

       È possibile trovare esempi e indicazioni su come utilizzare DSS in [Manuale](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Using_Document/DSS_User_Manual.md).

## Documenti

       Per un elenco completo dei documenti per DSS1.0, vedere [DSS-Doc](https://github.com/WeBankFinTech/DataSphereStudio-Doc)

       Di seguito è riportata la guida all'installazione per i plug-in AppConn relativi a DSS:

*   [Guida all'installazione di Visualis AppConn Plugin per DSS](https://github.com/WeBankFinTech/Visualis/blob/master/visualis_docs/en_US/Visualis_appconn_install_en.md)

*   [Guida all'installazione di Schedulis AppConn Plugin per DSS](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Installation_and_Deployment/Schedulis_Linkis_JobType_Installation_Documentation.md)

*   [Guida all'installazione di Qualitis AppConn Plugin per DSS](https://github.com/WeBankFinTech/Qualitis/blob/master/docs/zh_CN/ch1/%E6%8E%A5%E5%85%A5%E5%B7%A5%E4%BD%9C%E6%B5%81%E6%8C%87%E5%8D%97.md)

*   [Guida all'installazione del plug-in Exchangeis AppConn per DSS](https://github.com/WeDataSphere/Exchangis/blob/master/docs/en_US/ch1/exchangis_appconn_deploy_en.md)

*   [Guida all'installazione del plug-in Streamis AppConn per DSS](https://github.com/WeBankFinTech/Streamis/blob/main/docs/en_US/0.2.0/development/StreamisAppConnInstallationDocument.md)

*   [Prophecis AppConn Plugin Guida all'installazione per DSS](https://github.com/WeBankFinTech/Prophecis/blob/master/docs/zh_CN/Deployment_Documents/Prophecis%20Appconn%E5%AE%89%E8%A3%85%E6%96%87%E6%A1%A3.md)

*   [Guida all'installazione di DolphinScheduler AppConn Plugin per DSS](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Installation_and_Deployment/DolphinScheduler_Plugin_Installation_Documentation.md)

## Architettura

![DSS Architecture](images/en_US/readme/architecture.png)

## Scenari di utilizzo

      DataSphere Studio è adatto per i seguenti scenari:

      1. Scenari in cui la funzionalità della piattaforma Big Data viene preparata o inizializzata ma non sono disponibili strumenti di applicazione dei dati.

      2. Scenari in cui gli utenti dispongono già di funzionalità della piattaforma Big Data Foundation, ma con solo pochi strumenti di applicazione dei dati.

      3. Scenari in cui gli utenti hanno la capacità di una piattaforma di base di big data e di strumenti applicativi di dati completi, ma soffrono di un forte isolamento e di elevati costi di apprendimento perché tali strumenti non sono stati integrati insieme.

      4. Scenari in cui gli utenti hanno le capacità della piattaforma di base dei big data e strumenti applicativi completi per i dati. ma manca di specifiche unificate e standardizzate, mentre una parte di questi strumenti è stata integrata.

## Contribuire

       I contributi sono sempre i benvenuti, abbiamo bisogno di più contributori per costruire DSS insieme. o codice, o doc, o altri supporti che potrebbero aiutare la comunità.

       Per i contributi al codice e alla documentazione, segui la guida ai contributi.

## Comunicazione

       Per qualsiasi domanda o suggerimento, si prega gentilmente di inviare un problema.

       Puoi scansionare il codice QR qui sotto per unirti al nostro gruppo WeChat e QQ per ottenere una risposta più immediata.

![communication](images/en_US/readme/communication.png)

## Chi utilizza DSS

       Abbiamo aperto un problema per consentire agli utenti di inviare feedback e registrare chi utilizza DSS.

       Dalla prima versione di DSS nel 2019, ha accumulato più di 700 società di prova e oltre 1000 utenti di prova sandbox, che coinvolgono diversi settori, dalla finanza, alle banche, alle telecomunicazioni, alla manifattura, alle società internet e così via.

## Licenza

       DSS è sotto la licenza Apache 2.0. Vedi il [Licenza](LICENSE) per i dettagli.
