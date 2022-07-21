# ![DSS](images/en_US/readme/DSS_logo.png)

[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)

Anglais | [中文](README-ZH.md)

## Introduction

       DataSphere Studio (DSS en abrégé) est WeDataSphere, un portail de gestion de développement d’applications de données à guichet unique développé par WeBank.

       Grâce à la conception de framework intégré enfichable et au Linkis, un middleware informatique, DSS peut facilement intégrer divers systèmes d’application de données de couche supérieure, ce qui rend le développement de données simple et facile à utiliser.

       DataSphere Studio se positionne comme un portail de développement d’applications de données, et la boucle fermée couvre l’ensemble du processus de développement d’applications de données. Avec une interface utilisateur unifiée, l’expérience de développement graphique par glisser-déposer de type flux de travail répond à l’ensemble du cycle de vie du développement d’applications de données, de l’importation de données au nettoyage de la désensibilisation, à l’analyse de données, à l’exploration de données, à l’inspection de la qualité, à la visualisation, à la planification aux applications de sortie de données, etc.

       Avec les capacités de connexion, de réutilisation et de simplification de Linkis, DSS est né avec des capacités de qualité financière de haute concurrence, de haute disponibilité, d’isolation multi-locataire et de gestion des ressources.

## Aperçu de l’interface utilisateur

       S’il vous plaît soyez patient, il faudra un certain temps pour charger gif.

![DSS-V1.0 GIF](images/en_US/readme/DSS_gif.gif)

## Fonctionnalités de base

### 1. Interface utilisateur de gestion du développement d’applications à guichet unique et à processus complet

       Le MAS est hautement intégré. Les composants actuellement intégrés comprennent(**Compatibilité des versions DSS pour les composants ci-dessus, veuillez visiter : [Liste de compatibilité des composants intégrés](README.md#4-integrated-data-application-components)**):

       1. Outil IDE de développement de données - [Scriptis](https://github.com/WeBankFinTech/Scriptis)

       2. Outil de visualisation de données - [Visualis](https://github.com/WeBankFinTech/Visualis) (Basé sur le projet open source [Davinci](https://github.com/edp963/davinci) contribué par CreditEase)

       3. Outil de gestion de la qualité des données - [Qualite](https://github.com/WeBankFinTech/Qualitis)

       4. Outil de planification du flux de travail - [Planification](https://github.com/WeBankFinTech/Schedulis)

       5. Outil d’échange de données - [Échange](https://github.com/WeBankFinTech/Exchangis)

       6. Service d’API de données - [DataApiService](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Using_Document/DataApiService_Usage_Documentation.md)

       7. Outil de gestion du développement d’applications en streaming - [Streamis](https://github.com/WeBankFinTech/Streamis)

       8. Plate-forme d’apprentissage automatique à guichet unique - [Prophétie](https://github.com/WeBankFinTech/Prophecis)

       9. Outil de planification des tâches de flux de travail - DolphinScheduler (**Dans la fusion de code**)

       10. Documentation d’aide et guide du débutant - Guide de l’utilisateur (**Dans la fusion de code**)

       11. Centre de modèles de données - DataModelCenter (**En développement**)

       **Compatibilité des versions DSS pour les composants ci-dessus, veuillez visiter : [Liste de compatibilité des composants intégrés](README.md#4-integrated-data-application-components)**.

       Avec une architecture de framework enfichable, DSS est conçu pour permettre aux utilisateurs d’intégrer rapidement de nouveaux outils d’application de données ou de remplacer divers outils intégrés par DSS. Par exemple, remplacez Scriptis par Zeppelin, et remplacez Schedulis par DolphinScheduler...

![DSS one-stop video](images/en_US/readme/onestop.gif)

### 2. AppConn, basé sur Linkis, définit un concept de design unique

       AppConn est le concept de base qui permet à DSS d’intégrer facilement et rapidement divers systèmes Web de couche supérieure.

       AppConn, un connecteur d’application, définit un ensemble de protocoles d’intégration frontaux et back-end unifiés à trois niveaux, permettant aux systèmes d’application de données externes de faire facilement et rapidement partie du développement d’applications de données DSS.

       Les spécifications à trois niveaux d’AppConn sont : la spécification SSO de premier niveau, la spécification de structure organisationnelle de deuxième niveau et la spécification de processus de développement de troisième niveau.

       DSS organise plusieurs AppConns en série pour former un flux de travail qui prend en charge l’exécution en temps réel et l’exécution planifiée. Les utilisateurs peuvent compléter l’ensemble du développement de processus des applications de données avec de simples opérations de glisser-déposer.

       Depuis qu’AppConn est intégré à Linkis, le système d’application de données externe partage les capacités de gestion des ressources, de limitation simultanée et de haute performance. AppConn permet également un contexte partageable au niveau du système et permet ainsi à l’application de données externes de s’éloigner complètement des silos d’applications.

### 3. Espace de travail, en tant qu’unité de gestion

       Avec Workspace comme unité de gestion, il organise et gère les applications métier de divers systèmes d’applications de données, définit un ensemble de normes communes pour le développement collaboratif d’espaces de travail entre les systèmes d’applications de données et fournit des fonctionnalités de gestion des rôles utilisateur.

### 4. Composants d’application de données intégrés

       DSS a intégré une variété de systèmes d’application de données de couche supérieure en implémentant plusieurs AppConns, qui peuvent essentiellement répondre aux besoins de développement de données des utilisateurs.

       **Si vous le souhaitez, de nouveaux systèmes d’application de données peuvent également être facilement intégrés pour remplacer ou enrichir le processus de développement d’applications de données de DSS.** [Cliquez sur moi pour apprendre à intégrer rapidement de nouveaux systèmes d’application](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Development_Documentation/Third-party_System_Access_Development_Guide.md)

| Composant | Description | DSS0. Version compatible X (DSS0.9.1 recommandée) | Version compatible DSS1.0 (DSS1.1.0 recommandé) |
| --------------- | -------------------------------------------------------------------- | --------- | ---------- |
| [**Linkis**](https://github.com/apache/incubator-linkis) | Le middleware informatique Apache Linkis, en fournissant des interfaces standard telles que REST/ WebSocket/JDBC/SDK, les applications de couche supérieure peuvent facilement se connecter et accéder aux moteurs sous-jacents tels que MySQL/ Spark/Hive/Presto/Flink. | Linkis0.11.0 est recommandé (\**Libéré* \*) | >= Linkis1.1.1 (**libéré**) |
| [**DataApiService**](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Using_Document/DataApiService_Usage_Documentation.md)  | (DSS dispose d’outils d’application tiers intégrés) service d’API de données. Le script SQL peut être rapidement publié en tant qu’interface Restful, offrant une capacité d’accès Rest au monde extérieur. | | non pris en charge DSS1.1.0 recommandé (**libéré**)|
| [**Scriptis**](https://github.com/WeBankFinTech/DataSphereStudio) | (DSS dispose d’outils d’application tiers intégrés) prend en charge l’écriture en ligne de scripts SQL, Pyspark, HiveQL et autres, et soumet-le à l’outil Web d’analyse de données \[Linkis] (https ://github.com/WeBankFinTech/Linkis). | DSS0.9.1 recommandé (**Libéré**) | DSS1.1.0 recommandé (**Libéré**) |
| [**Planification**](https://github.com/WeBankFinTech/Schedulis) | Système de planification des tâches de flux de travail basé sur le développement secondaire Azkaban, avec des fonctionnalités de qualité financière telles que des performances élevées, une haute disponibilité et une isolation des ressources mutualisées. | Schedulis0.6.1 recommandé (**libéré**) | >= Schedulis0.7.0 (**Libéré**) |
| **EventCheck (en anglais)** | (un outil d’application tiers intégré à DSS) fournit des capacités de communication de signaux dans l’ensemble de l’entreprise, de l’ingénierie et du flux de travail. | DSS0.9.1 recommandé (**Libéré**) | DSS1.1.0 recommandé (**Libéré**) |
| **EnvoyerE-mail** | (DSS dispose d’outils d’application tiers intégrés) offre la possibilité d’envoyer des données, tous les ensembles de résultats d’autres nœuds de flux de travail peuvent être envoyés par e-mail | DSS0.9.1 est recommandé (**libéré**) | DSS1.1.0 recommandé (**Libéré**) |
| [**Qualite**](https://github.com/WeBankFinTech/Qualitis) | Outil de vérification de la qualité des données, fournissant des capacités de vérification des données telles que l’intégrité et l’exactitude des données | Qualitis0.8.0 est recommandé (\*\*Publié \*\*) | >= Qualitis0.9.2 (**Libéré**) |
| [**Streamis**](https://github.com/WeBankFinTech/Streamis) | Outil de gestion du développement d’applications en streaming. Il prend en charge la publication de Flink Jar et Flink SQL, et fournit les capacités de développement, de débogage et de gestion de la production des applications de streaming, telles que: démarrage-arrêt, surveillance de l’état, point de contrôle, etc. | | non pris en charge >= Streamis0.2.0 (**Libéré**) |
| [**Prophétie**](https://github.com/WeBankFinTech/Prophecis) | Une plate-forme d’apprentissage automatique à guichet unique qui intègre plusieurs frameworks d’apprentissage automatique open source. MlFlow de Prophecis peut être connecté au flux de travail DSS via AppConn. | | non pris en charge >= Prophétie 0.3.2 (**Libéré**) |
| [**Échange**](https://github.com/WeBankFinTech/Exchangis) | Une plate-forme d’échange de données qui prend en charge la transmission de données entre des sources de données hétérogènes structurées et non structurées, le prochain Exchangis1. 0, fonctionnera avec le flux de travail DSS | | non pris en charge = Exchangis1.0.0 (**Libéré**) |
| [**Visualis**](https://github.com/WeBankFinTech/Visualis) | Un outil bi de visualisation de données basé sur le développement secondaire de Davinci, un projet open source de CreditEase, offre aux utilisateurs des capacités de visualisation de données au niveau financier en termes de sécurité des données. | Visualis0.5.0 recommandé |= Visualis1.0.0 (**Libéré**) |
| [**DolphinScheduler**](https://github.com/apache/dolphinscheduler) | Apache DolphinScheduler, une plate-forme de planification de tâches de flux de travail visuel distribuée et facilement évolutive, prend en charge la publication en un clic de flux de travail DSS sur DolphinScheduler. | | non pris en charge DolphinScheduler1.3.X (**Libéré**) |
| **Guide de l’utilisateur** | (DSS sera intégré à des outils d’application tiers) contient des documents d’aide, un guide du débutant, un habillage en mode sombre, etc. | | non pris en charge >= DSS1.1.0 (**Libéré**) |
| **DataModelCenter** | (l’outil d’application tiers que DSS construira) fournit principalement des capacités de planification d’entrepôt de données, de développement de modèles de données et de gestion des actifs de données. La planification de l’entrepôt de données comprend les domaines d’objet, les hiérarchies d’entrepôt de données, les modificateurs, etc. ; le développement de modèles de données comprend des indicateurs, des dimensions, des métriques, la création de tables basées sur des assistants, etc.; les ressources de données sont connectées à Apache Atlas pour fournir des fonctionnalités de traçage de données. | | non pris en charge Prévu dans DSS1.2.0 (**en cours de développement**) |
| **Gestionnaire d’utilisateurs** | (DSS dispose d’outils d’application tiers intégrés) initialisez automatiquement tous les environnements utilisateur nécessaires à un nouvel utilisateur DSS, y compris: la création d’utilisateurs Linux, divers chemins d’accès utilisateur, l’autorisation de répertoire, etc. | DSS0.9.1 recommandé (**Libéré**) | | de planification
| [**Air**](https://github.com/apache/airflow) | Prend en charge la publication de workflows DSS sur Apache Airflow pour la planification planifiée. | PR pas encore fusionné | | non pris en charge

## Environnement d’essai de démonstration

       La fonction de DataSphere Studio prenant en charge l’exécution de scripts présente des risques de sécurité élevés et l’isolation de l’environnement de démonstration WeDataSphere n’a pas été achevée. Étant donné que de nombreux utilisateurs se renseignent sur l’environnement de démonstration, nous avons décidé d’émettre d’abord des codes d’invitation à la communauté et d’accepter les demandes d’essai d’entreprises et d’organisations.

       Si vous souhaitez essayer l’environnement de démonstration, rejoignez le groupe d’utilisateurs de la communauté DataSphere Studio (**Veuillez vous référer à la fin du document**), et contact **Robot du groupe WeDataSphere** pour obtenir un code d’invitation.

       Page d’inscription de l’utilisateur de l’environnement DataSphereStudio Demo : [cliquez sur moi pour entrer](https://dss-open.wedatasphere.com/#/register)

       Page de connexion à l’environnement DataSphereStudio Demo : [cliquez sur moi pour entrer](https://dss-open.wedatasphere.com/#/login)

## Télécharger

       Veuillez vous rendre à la section [Page Des versions du DSS](https://github.com/WeBankFinTech/DataSphereStudio/releases) pour télécharger une version compilée ou un package de code source de DSS.

## Compiler et déployer

       Veuillez suivre [Guide de compilation](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Development_Documentation/Compilation_Documentation.md) pour compiler DSS à partir du code source.

       Veuillez vous référer à [Documents de déploiement](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Installation_and_Deployment/DSS%26Linkis_one-click_deployment_document_stand-alone_version.md) pour effectuer le déploiement.

## Exemples et orientations

       Vous trouverez des exemples et des conseils sur l’utilisation du DSS dans [Manuel](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Using_Document/DSS_User_Manual.md).

## Documents

       Pour obtenir la liste complète des documents relatifs à DSS1.0, reportez-vous à la section [DSS-Doc](https://github.com/WeBankFinTech/DataSphereStudio-Doc)

       Voici le guide d’installation des plug-ins AppConn liés à DSS :

*   [Guide d’installation du plug-in Visualis AppConn pour DSS](https://github.com/WeBankFinTech/Visualis/blob/master/visualis_docs/en_US/Visualis_appconn_install_en.md)

*   [Guide d’installation du plug-in Schedulis AppConn pour DSS](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Installation_and_Deployment/Schedulis_Linkis_JobType_Installation_Documentation.md)

*   [Qualitis AppConn Plugin Guide d’installation pour DSS](https://github.com/WeBankFinTech/Qualitis/blob/master/docs/zh_CN/ch1/%E6%8E%A5%E5%85%A5%E5%B7%A5%E4%BD%9C%E6%B5%81%E6%8C%87%E5%8D%97.md)

*   [Guide d’installation du plug-in Exchangis AppConn pour DSS](https://github.com/WeDataSphere/Exchangis/blob/master/docs/en_US/ch1/exchangis_appconn_deploy_en.md)

*   [Guide d’installation du plug-in Streamis AppConn pour DSS](https://github.com/WeBankFinTech/Streamis/blob/main/docs/en_US/0.2.0/development/StreamisAppConnInstallationDocument.md)

*   [Prophecis AppConn Plugin Guide d’installation pour DSS](https://github.com/WeBankFinTech/Prophecis/blob/master/docs/zh_CN/Deployment_Documents/Prophecis%20Appconn%E5%AE%89%E8%A3%85%E6%96%87%E6%A1%A3.md)

*   [DolphinScheduler AppConn Plugin Guide d’installation pour DSS](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Installation_and_Deployment/DolphinScheduler_Plugin_Installation_Documentation.md)

## Architecture

![DSS Architecture](images/en_US/readme/architecture.png)

## Scénarios d’utilisation

      DataSphere Studio convient aux scénarios suivants :

      1. Scénarios dans lesquels la capacité de la plate-forme Big Data est en cours de préparation ou d’initialisation, mais aucun outil d’application de données n’est disponible.

      2. Scénarios dans lesquels les utilisateurs disposent déjà de capacités de plate-forme big data foundation, mais avec seulement quelques outils d’application de données.

      3. Scénarios dans lesquels les utilisateurs ont la capacité d’une plate-forme de base Big Data et d’outils d’application de données complets, mais souffrent d’un fort isolement et de coûts d’apprentissage élevés parce que ces outils n’ont pas été intégrés ensemble.

      4. Scénarios dans lesquels les utilisateurs disposent des capacités d’une plate-forme de base Big Data et d’outils d’application de données complets. mais manque de spécifications unifiées et standardisées, alors qu’une partie de ces outils ont été intégrés.

## Contribuant

       Les contributions sont toujours les bienvenues, nous avons besoin de plus de contributeurs pour construire le MAS ensemble. soit du code, soit un document, soit d’autres supports qui pourraient aider la communauté.

       Pour les contributions au code et à la documentation, veuillez suivre le guide de contribution.

## Communication

       Pour toute question ou suggestion, veuillez soumettre un problème.

       Vous pouvez scanner le code QR ci-dessous pour rejoindre notre groupe WeChat et QQ afin d’obtenir une réponse plus immédiate.

![communication](images/en_US/readme/communication.png)

## Qui utilise DSS

       Nous avons ouvert un problème permettant aux utilisateurs de faire part de leurs commentaires et d’enregistrer qui utilise DSS.

       Depuis la première version de DSS en 2019, il a accumulé plus de 700 sociétés d’essai et plus de 1000 utilisateurs d’essai de bac à sable, qui impliquent divers secteurs, de la finance, de la banque, de la télécommunication, à la manufacture, aux sociétés Internet, etc.

## Licence

       DSS est sous licence Apache 2.0. Voir le [Licence](LICENSE) pour plus de détails.
