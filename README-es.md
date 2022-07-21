# ![DSS](images/en_US/readme/DSS_logo.png)

[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)

| en inglés [中文](README-ZH.md)

## Introducción

       DataSphere Studio (DSS para abreviar) es WeDataSphere, un portal de gestión de desarrollo de aplicaciones de datos integral desarrollado por WeBank.

       Con el diseño de marco integrado conectable y Linkis, un middleware informático, DSS puede integrar fácilmente varios sistemas de aplicación de datos de capa superior, lo que hace que el desarrollo de datos sea simple y fácil de usar.

       DataSphere Studio se posiciona como un portal de desarrollo de aplicaciones de datos, y el bucle cerrado cubre todo el proceso de desarrollo de aplicaciones de datos. Con una interfaz de usuario unificada, la experiencia de desarrollo gráfico de arrastrar y soltar similar a un flujo de trabajo cumple con todo el ciclo de vida del desarrollo de aplicaciones de datos, desde la importación de datos, la limpieza de desensibilización, el análisis de datos, la minería de datos, la inspección de calidad, la visualización, la programación hasta las aplicaciones de salida de datos, etc.

       Con las capacidades de conexión, reutilización y simplificación de Linkis, DSS nace con capacidades de grado financiero de alta concurrencia, alta disponibilidad, aislamiento de múltiples inquilinos y administración de recursos.

## Vista previa de la interfaz de usuario

       Tenga paciencia, tomará algún tiempo cargar gif.

![DSS-V1.0 GIF](images/en_US/readme/DSS_gif.gif)

## Características principales

### 1. Interfaz de usuario de administración de desarrollo de aplicaciones integral y de proceso completo

       DSS está altamente integrado. Los componentes actualmente integrados incluyen(**Compatibilidad de la versión DSS para los componentes anteriores, visite: [Lista de compatibilidad de componentes integrados](README.md#4-integrated-data-application-components)**):

       1. Herramienta IDE de desarrollo de datos - [Scriptis](https://github.com/WeBankFinTech/Scriptis)

       2. Herramienta de visualización de datos - [Visualis](https://github.com/WeBankFinTech/Visualis) (Basado en el proyecto de código abierto [Davinci](https://github.com/edp963/davinci) contribución de CreditEase)

       3. Herramienta de gestión de calidad de datos - [Calidad](https://github.com/WeBankFinTech/Qualitis)

       4. Herramienta de programación de flujo de trabajo - [Schedulis](https://github.com/WeBankFinTech/Schedulis)

       5. Herramienta de intercambio de datos - [Exchangis](https://github.com/WeBankFinTech/Exchangis)

       6. Servicio de API de datos - [DataApiService](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Using_Document/DataApiService_Usage_Documentation.md)

       7. Herramienta de gestión de desarrollo de aplicaciones de streaming - [Streamis](https://github.com/WeBankFinTech/Streamis)

       8. Plataforma de aprendizaje automático integral - [Profecías](https://github.com/WeBankFinTech/Prophecis)

       9. Herramienta de programación de tareas de flujo de trabajo - DolphinScheduler (**En la fusión de código**)

       10. Documentación de ayuda y guía para principiantes - UserGuide (**En la fusión de código**)

       11. Centro de modelos de datos - DataModelCenter (**En desarrollo**)

       **Compatibilidad de la versión DSS para los componentes anteriores, visite: [Lista de compatibilidad de componentes integrados](README.md#4-integrated-data-application-components)**.

       Con una arquitectura de marco conectable, DSS está diseñado para permitir a los usuarios integrar rápidamente nuevas herramientas de aplicación de datos o reemplazar varias herramientas que DSS ha integrado. Por ejemplo, reemplace Scriptis con Zeppelin y reemplace Schedulis con DolphinScheduler ...

![DSS one-stop video](images/en_US/readme/onestop.gif)

### 2. AppConn, basado en Linkis, define un concepto de diseño único

       AppConn es el concepto central que permite a DSS integrar fácil y rápidamente varios sistemas web de capa superior.

       AppConn, un conector de aplicaciones, define un conjunto de protocolos unificados de integración de tres niveles front-end y back-end, lo que permite que los sistemas de aplicaciones de datos externos se conviertan fácil y rápidamente en parte del desarrollo de aplicaciones de datos DSS.

       Las especificaciones de tres niveles de AppConn son: la especificación de SSO de primer nivel, la especificación de estructura organizativa de segundo nivel y la especificación de proceso de desarrollo de tercer nivel.

       DSS organiza varios AppConns en serie para formar un flujo de trabajo que admita la ejecución en tiempo real y la ejecución programada. Los usuarios pueden completar todo el proceso de desarrollo de aplicaciones de datos con simples operaciones de arrastrar y soltar.

       Dado que AppConn está integrado con Linkis, el sistema de aplicación de datos externos comparte las capacidades de administración de recursos, limitación concurrente y alto rendimiento. AppConn también permite un contexto compartible en todo el nivel del sistema y, por lo tanto, hace que la aplicación de datos externos se aleje por completo de los silos de aplicaciones.

### 3. Espacio de trabajo, como unidad de gestión

       Con Workspace como unidad de administración, organiza y administra aplicaciones comerciales de varios sistemas de aplicaciones de datos, define un conjunto de estándares comunes para el desarrollo colaborativo de espacios de trabajo en todos los sistemas de aplicaciones de datos y proporciona capacidades de administración de roles de usuario.

### 4. Componentes integrados de la aplicación de datos

       DSS ha integrado una variedad de sistemas de aplicación de datos de capa superior mediante la implementación de múltiples AppConns, que básicamente pueden satisfacer las necesidades de desarrollo de datos de los usuarios.

       **Si se desea, también se pueden integrar fácilmente nuevos sistemas de aplicación de datos para reemplazar o enriquecer el proceso de desarrollo de aplicaciones de datos de DSS.** [Haga clic en mí para aprender a integrar rápidamente nuevos sistemas de aplicaciones](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Development_Documentation/Third-party_System_Access_Development_Guide.md)

| | de componentes Descripción | DSS0. Versión compatible con X (se recomienda DSS0.9.1) | Versión compatible con DSS1.0 (se recomienda DSS1.1.0) |
| --------------- | -------------------------------------------------------------------- | --------- | ---------- |
| [**Linkis**](https://github.com/apache/incubator-linkis) | El middleware informático Apache Linkis, al proporcionar interfaces estándar como REST / WebSocket / JDBC / SDK, las aplicaciones de capa superior pueden conectarse y acceder fácilmente a motores subyacentes como MySQL / Spark / Hive / Presto / Flink. | Se recomienda Linkis0.11.0 (\**Liberado* \*) | >= Linkis1.1.1 (**liberado**) |
| [**DataApiService**](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Using_Document/DataApiService_Usage_Documentation.md)  | (DSS tiene herramientas de aplicación de terceros integradas) servicio de API de datos. El script SQL se puede publicar rápidamente como una interfaz Restful, proporcionando capacidad de acceso Rest al mundo exterior. | No se admiten | Se recomienda DSS1.1.0 (**liberado**)|
| [**Scriptis**](https://github.com/WeBankFinTech/DataSphereStudio) | (DSS tiene herramientas de aplicación de terceros incorporadas) admite la escritura en línea de SQL, Pyspark, HiveQL y otros scripts, y se envía a la herramienta web de análisis de datos \[Linkis] (https://github.com/WeBankFinTech/Linkis). | DSS0.9.1 recomendado (**Liberado**) | DSS1.1.0 recomendado (**Liberado**) |
| [**Schedulis**](https://github.com/WeBankFinTech/Schedulis) | Sistema de programación de tareas de flujo de trabajo basado en el desarrollo secundario de Azkaban, con características de grado financiero como alto rendimiento, alta disponibilidad y aislamiento de recursos multiinquilino. | Schedulis recomendado0.6.1 (**liberado**) | >= Schedulis0.7.0 (**Liberado**) |
| **EventCheck** | (una herramienta de aplicación de terceros integrada en DSS) proporciona capacidades de comunicación de señales en todos los negocios, ingeniería y flujo de trabajo. | DSS0.9.1 recomendado (**Liberado**) | DSS1.1.0 recomendado (**Liberado**) |
| **EnviarEmail** | (DSS tiene herramientas de aplicación de terceros incorporadas) proporciona la capacidad de enviar datos, todos los conjuntos de resultados de otros nodos de flujo de trabajo se pueden enviar por correo electrónico | Se recomienda DSS0.9.1 (**liberado**) | DSS1.1.0 recomendado (**Liberado**) |
| [**Calidad**](https://github.com/WeBankFinTech/Qualitis) | Herramienta de verificación de calidad de datos, que proporciona capacidades de verificación de datos como la integridad y corrección de datos | Se recomienda Qualitis0.8.0 (\*\*Publicado \*\*) | >= Qualitis0.9.2 (**Liberado**) |
| [**Streamis**](https://github.com/WeBankFinTech/Streamis) | Herramienta de gestión de desarrollo de aplicaciones en streaming. Es compatible con el lanzamiento de Flink Jar y Flink SQL, y proporciona las capacidades de desarrollo, depuración y gestión de producción de aplicaciones de streaming, tales como: start-stop, monitoreo de estado, punto de control, etc. | No se admiten | >= Streamis0.2.0 (**Liberado**) |
| [**Profecías**](https://github.com/WeBankFinTech/Prophecis) | Una plataforma de aprendizaje automático integral que integra múltiples marcos de aprendizaje automático de código abierto. MLFlow de Prophecis se puede conectar al flujo de trabajo de DSS a través de AppConn. | No se admiten | >= Profecía 0.3.2 (**Liberado**) |
| [**Exchangis**](https://github.com/WeBankFinTech/Exchangis) | Una plataforma de intercambio de datos que admite la transmisión de datos entre fuentes de datos heterogéneas estructuradas y no estructuradas, el próximo Exchangis1. 0, funcionará con el flujo de trabajo de DSS | no es compatible | = Exchangis1.0.0 (**Liberado**) |
| [**Visualis**](https://github.com/WeBankFinTech/Visualis) | Una herramienta de BI de visualización de datos basada en el desarrollo secundario de Davinci, un proyecto de código abierto de CreditEase, proporciona a los usuarios capacidades de visualización de datos a nivel financiero en términos de seguridad de datos. | Visualis0.5.0 recomendado |= Visualis1.0.0 (**Liberado**) |
| [**DolphinScheduler**](https://github.com/apache/dolphinscheduler) | Apache DolphinScheduler, una plataforma de programación de tareas de flujo de trabajo visual distribuida y fácilmente escalable, admite la publicación con un solo clic de flujos de trabajo DSS en DolphinScheduler. | No se admiten | DolphinScheduler1.3.x (**Liberado**) |
| **Guía del usuario** | (DSS serán herramientas de aplicación de terceros incorporadas) contiene documentos de ayuda, guía para principiantes, skinning en modo oscuro, etc. | No se admiten | >= DSS1.1.0 (**Liberado**) |
| **DataModelCenter** | (la herramienta de aplicación de terceros que DSS construirá) proporciona principalmente planificación de almacenamiento de datos, desarrollo de modelos de datos y capacidades de gestión de activos de datos. La planificación del almacén de datos incluye dominios temáticos, jerarquías de almacenamiento de datos, modificadores, etc.; el desarrollo de modelos de datos incluye indicadores, dimensiones, métricas, creación de tablas basadas en asistentes, etc.; los activos de datos están conectados a Apache Atlas para proporcionar capacidades de linaje de datos. | No se admiten | Previsto en DSS1.2.0 (**en desarrollo**) |
| **UserManager** | (DSS tiene herramientas de aplicación de terceros integradas) inicializa automáticamente todos los entornos de usuario necesarios para un nuevo usuario de DSS, incluyendo: creación de usuarios de Linux, varias rutas de usuario, autorización de directorios, etc. | DSS0.9.1 recomendado (**Liberado**) | Planificación |
| [**Corriente de aire**](https://github.com/apache/airflow) | Admite la publicación de flujos de trabajo DSS en Apache Airflow para la programación programada. | PR aún no se ha fusionado | No se admiten |

## Entorno de prueba de demostración

       La función de DataSphere Studio que admite la ejecución de scripts tiene altos riesgos de seguridad y no se ha completado el aislamiento del entorno de demostración de WeDataSphere. Teniendo en cuenta que muchos usuarios están preguntando sobre el entorno de demostración, decidimos primero emitir códigos de invitación a la comunidad y aceptar aplicaciones de prueba de empresas y organizaciones.

       Si desea probar el entorno de demostración, únase al grupo de usuarios de la comunidad de DataSphere Studio (**Consulte el final del documento**), y contacto **Robot del grupo WeDataSphere** para obtener un código de invitación.

       Página de registro de usuario del entorno dataspherestudio demo: [Haga clic en mí para entrar](https://dss-open.wedatasphere.com/#/register)

       Página de inicio de sesión del entorno datasphereStudio Demo: [Haga clic en mí para entrar](https://dss-open.wedatasphere.com/#/login)

## Descargar

       Por favor, vaya al [Página de versiones de DSS](https://github.com/WeBankFinTech/DataSphereStudio/releases) para descargar una versión compilada o un paquete de código fuente de DSS.

## Compilar e implementar

       Por favor, siga [Guía de compilación](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Development_Documentation/Compilation_Documentation.md) para compilar DSS a partir del código fuente.

       Por favor refiérase a [Documentos de implementación](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Installation_and_Deployment/DSS%26Linkis_one-click_deployment_document_stand-alone_version.md) para realizar la implementación.

## Ejemplos y orientación

       Puede encontrar ejemplos y orientación sobre cómo usar DSS en [Manual de usuario](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Using_Document/DSS_User_Manual.md).

## Documentos

       Para obtener una lista completa de los documentos para DSS1.0, consulte [DSS-Doc](https://github.com/WeBankFinTech/DataSphereStudio-Doc)

       La siguiente es la guía de instalación para los complementos de AppConn relacionados con DSS:

*   [Guía de instalación del complemento Visualis AppConn para DSS](https://github.com/WeBankFinTech/Visualis/blob/master/visualis_docs/en_US/Visualis_appconn_install_en.md)

*   [Guía de instalación del complemento Schedulis AppConn para DSS](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Installation_and_Deployment/Schedulis_Linkis_JobType_Installation_Documentation.md)

*   [Guía de instalación del complemento Qualitis AppConn para DSS](https://github.com/WeBankFinTech/Qualitis/blob/master/docs/zh_CN/ch1/%E6%8E%A5%E5%85%A5%E5%B7%A5%E4%BD%9C%E6%B5%81%E6%8C%87%E5%8D%97.md)

*   [Guía de instalación del complemento AppConn de Exchangis para DSS](https://github.com/WeDataSphere/Exchangis/blob/master/docs/en_US/ch1/exchangis_appconn_deploy_en.md)

*   [Guía de instalación del complemento Streamis AppConn para DSS](https://github.com/WeBankFinTech/Streamis/blob/main/docs/en_US/0.2.0/development/StreamisAppConnInstallationDocument.md)

*   [Guía de instalación del complemento Prophecis AppConn para DSS](https://github.com/WeBankFinTech/Prophecis/blob/master/docs/zh_CN/Deployment_Documents/Prophecis%20Appconn%E5%AE%89%E8%A3%85%E6%96%87%E6%A1%A3.md)

*   [Guía de instalación del complemento DolphinScheduler AppConn para DSS](https://github.com/WeBankFinTech/DataSphereStudio-Doc/blob/main/en_US/Installation_and_Deployment/DolphinScheduler_Plugin_Installation_Documentation.md)

## Arquitectura

![DSS Architecture](images/en_US/readme/architecture.png)

## Escenarios de uso

      DataSphere Studio es adecuado para los siguientes escenarios:

      1. Escenarios en los que la capacidad de la plataforma de big data se está preparando o inicializando pero no hay herramientas de aplicación de datos disponibles.

      2. Escenarios en los que los usuarios ya tienen capacidades de plataforma de base de big data pero con solo unas pocas herramientas de aplicación de datos.

      3. Escenarios en los que los usuarios tienen la capacidad de una plataforma de base de big data y herramientas integrales de aplicación de datos, pero sufren un fuerte aislamiento y altos costos de aprendizaje porque esas herramientas no se han integrado juntas.

      4. Escenarios en los que los usuarios tienen las capacidades de la plataforma de base de big data y las herramientas integrales de aplicación de datos. pero carece de especificaciones unificadas y estandarizadas, mientras que una parte de estas herramientas se han integrado.

## Contribuyendo

       Las contribuciones siempre son bienvenidas, necesitamos más contribuyentes para construir DSS juntos. ya sea código, o doc, u otros soportes que podrían ayudar a la comunidad.

       Para contribuciones de código y documentación, siga la guía de contribución.

## Comunicación

       Para cualquier pregunta o sugerencia, por favor envíe un problema.

       Puede escanear el código QR a continuación para unirse a nuestro grupo de WeChat y QQ para obtener una respuesta más inmediata.

![communication](images/en_US/readme/communication.png)

## Quién usa DSS

       Abrimos un problema para que los usuarios puedan comentar y registrar quién está usando DSS.

       Desde el primer lanzamiento de DSS en 2019, ha acumulado más de 700 compañías de prueba y más de 1000 usuarios de prueba de sandbox, que involucran diversas industrias, desde finanzas, banca, telecomunicaciones, hasta fábricas, compañías de Internet, etc.

## Licencia

       DSS está bajo la licencia Apache 2.0. Ver el [Licencia](LICENSE) para más detalles.
