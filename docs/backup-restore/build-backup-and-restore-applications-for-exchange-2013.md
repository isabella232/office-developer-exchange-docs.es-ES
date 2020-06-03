---
title: Creación de aplicaciones de copia de seguridad y restauración para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e5e952a5-add1-417c-a3c2-230f4dc99b00
description: Busque información sobre los componentes y la arquitectura de las aplicaciones de copia de seguridad y restauración para Exchange 2013 y los requisitos del sistema para crear una aplicación de copia de seguridad y restauración.
ms.openlocfilehash: f8a332d0816792f8888c97a8394886b026f5204b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455276"
---
# <a name="build-backup-and-restore-applications-for-exchange-2013"></a>Creación de aplicaciones de copia de seguridad y restauración para Exchange 2013

Busque información sobre los componentes y la arquitectura de las aplicaciones de copia de seguridad y restauración para Exchange 2013 y los requisitos del sistema para crear una aplicación de copia de seguridad y restauración.
  
**Se aplica a:** Exchange Server 2013 
  
Puede usar el [servicio de instantáneas de volumen (VSS)](https://msdn.microsoft.com/library/bb968832%28VS.85%29.aspx) en versiones de Windows Server que empiecen por windows Server 2008 para crear aplicaciones que realicen copias de seguridad y restauren datos de Exchange Server 2013. VSS proporciona una infraestructura que permite crear y administrar instantáneas en sistemas de administración de almacenamiento de terceros, aplicaciones empresariales y hardware. Puede crear soluciones basadas en la infraestructura de VSS que usan instantáneas para hacer una copia de seguridad y restaurar una o varias bases de datos de Exchange 2013. 
  
## <a name="backup-and-restore-application-prerequisites"></a>Requisitos previos de la aplicación de copia de seguridad y restauración
<a name="bk_systemrequirements"> </a>

Para que la aplicación de copia de seguridad y restauración personalizada y VSS puedan realizar copias de seguridad y restauraciones de bases de datos de Exchange 2013, el entorno debe incluir lo siguiente:
  
- Una versión de Windows Server a partir de Windows Server 2008 
    
- Exchange 2013
    
Además, si va a crear una aplicación de copia de seguridad y restauración, debe tener en cuenta las siguientes restricciones en el entorno de desarrollo:
  
- VSS es una API de COM no administrada a la que se puede tener acceso desde código administrado de .NET Framework a través de un ensamblado de interoperabilidad COM.
    
- El shell de administración de Exchange es una aplicación administrada a la que se tiene acceso a través de código administrado de .NET Framework.
    
- La API de CHKSGFILES que se proporciona con Exchange 2013 es una DLL de 64 bits de código nativo. No se admite el uso de la DLL CHKSGFILES de Exchange 2007 32-bit con las bases de datos de Exchange 2013.
    
## <a name="backup-and-restore-application-overview"></a>Información general sobre la aplicación de copia de seguridad y restauración
<a name="bk_components"> </a>

VSS coordina la comunicación entre los siguientes componentes: 
  
- El solicitante de VSS, que es la aplicación de copia de seguridad
    
- El escritor de VSS
    
- El proveedor de VSS, que es el sistema, el software o los componentes de hardware que crean las instantáneas
    
Para usar VSS para hacer una copia de seguridad de los datos de Exchange 2013, la aplicación de copia de seguridad debe ser un solicitante VSS de Exchange 2013-Aware. Exchange 2013 incluye un Escritor VSS, denominado escritor de Microsoft Exchange, para el programa de copia de seguridad de Windows Server; sin embargo, el escritor de Exchange solo realiza una copia de seguridad de volúmenes completos. No realiza una copia de seguridad de bases de datos de Exchange 2013 individuales. Si necesita más flexibilidad, puede usar una aplicación de copia de seguridad de terceros que tenga un escritor de VSS que reconozca Exchange y que pueda funcionar con bases de datos individuales de Exchange, o bien puede crear un solicitante personalizado de VSS.
  
Antes de que la aplicación llame a VSS para iniciar una copia de seguridad, debe obtener información sobre la configuración de almacenamiento del sistema Exchange 2013 en el que se está realizando la copia de seguridad. Esta información se almacena en servicios de dominio de Active Directory (AD DS). La aplicación de copia de seguridad puede obtener datos de configuración de almacenamiento de Exchange mediante comandos de Shell de administración de Exchange. Para obtener más información, vea [PowerShell de Exchange Server (Shell de administración de Exchange)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps). 
  
Las aplicaciones de copia de seguridad de Exchange 2013 llaman a las API COM de VSS para crear copias de seguridad completas, de copia, diferenciales e incrementales de las bases de datos de Exchange; no interactúan directamente con VSS Writer. La funcionalidad del grupo de disponibilidad de base de datos (DAG) de Exchange también permite que su aplicación cree una copia de seguridad completamente coherente, incluso si la copia de seguridad completa inicial y las copias de seguridad incrementales posteriores provienen de diferentes servidores en el DAG. Una vez que VSS crea la copia de los datos de Exchange, la aplicación de copia de seguridad almacena los datos en los medios deseados.
  
Para restaurar una base de datos de Exchange 2013, la aplicación de restauración recupera la base de datos y los archivos de registro del medio de copia de seguridad y los almacena en el almacenamiento en disco activo de un servidor de Exchange. Las bases de datos individuales no están asociadas a un servidor de Exchange en particular. 
  
Las aplicaciones de copia de seguridad y restauración deben especificar un número de parámetros específicos de Exchange 2013 para controlar y administrar correctamente las operaciones ejecutadas por VSS en las bases de datos de Exchange 2013. Por ejemplo, dado que Exchange 2013 admite hasta 100 simultáneamente bases de datos activas, la aplicación de copia de seguridad debe especificar y procesar correctamente el archivo de base de datos, los archivos de registro de transacciones y los componentes de base de datos de archivos de controles.
  
Para reconstruir una base de datos que tenía cambios desde la última copia de seguridad completa, la aplicación de restauración requiere archivos de registro y de base de datos de distintas copias de seguridad. Por ejemplo, es posible que necesite una copia de seguridad completa semanal y una o más copias de seguridad incrementales diarias. En los sistemas Exchange 2013 que usan Dag, la aplicación de restauración puede reconstruir una base de datos con copias de seguridad de diferentes copias de bases de datos en servidores diferentes del mismo DAG. Sin embargo, la única forma admitida de restaurar una base de datos de DAG desde una copia de seguridad es restaurar todas las copias activas y pasivas de la base de datos con los mismos datos.
  
Una vez que todos los datos están en su ubicación, la aplicación de restauración indica a Exchange que Compruebe la integridad de la base de datos y los archivos de registro. Si la base de datos y los archivos de registro se han restaurado correctamente, el servidor de Exchange puede reproducir los archivos de registro de la base de datos para actualizar la base de datos y montarla. Si la base de datos se ha recuperado en un servidor que ya tiene una copia activa de la base de datos montada, la base de datos se trata como una base de datos de recuperación. Si la base de datos se ha recuperado en un servidor diferente, la base de datos puede montarse de manera independiente o puede agregarse a la réplica en el DAG.
  
## <a name="backup-and-restore-system-architecture"></a>Arquitectura del sistema de copia de seguridad y restauración
<a name="bk_ExchangeVSS"> </a>

VSS se comunica con el sistema de archivos de Windows Server y con el controlador de dispositivo de almacenamiento masivo a través de un proveedor de terceros (o personalizado). El proveedor de hardware determina dónde se creará la instantánea. VSS abstrae la instantánea específica del hardware para que la aplicación de copia de seguridad y restauración pueda tener acceso a la instantánea sin información sobre los detalles de implementación de hardware. La siguiente figura muestra cómo interactúa la aplicación de copia de seguridad y restauración con Exchange 2013 y Windows Server.
  
**Figura 1. Arquitectura del sistema de copia de seguridad y restauración**

![Diagrama que muestra cómo interactúa una aplicación de copia de seguridad y restauración. Existe una comunicación bidireccional entre Exchange, Windows Server y la aplicación cliente. Windows Server también actúa con un dispositivo de almacenamiento masivo o un medio de copia de seguridad.](media/VSS_architecture_E2k7.gif)
  
La aplicación de copia de seguridad y restauración funciona como el solicitante de VSS. El solicitante se comunica con VSS para obtener información acerca de Exchange 2013, para iniciar la creación de instantáneas y para obtener acceso a los datos de copia de seguridad. 
  
El almacén de Exchange es un componente de Exchange 2013 y obtiene acceso a las bases de datos de Exchange 2013 mediante el sistema de archivos de Windows Server. En el sistema de archivos, cada servidor de Exchange puede montar simultáneamente hasta 100 bases de datos con los archivos de base de datos (. edb) adjuntos, los archivos de registro de transacciones y un archivo de punto de control.
  
Para admitir VSS, Exchange 2013 incluye un escritor de Exchange integrado en el almacén de Exchange. El escritor de Exchange coordina el almacén de Exchange (que opera en nombre del solicitante) para inmovilizar y desmontar la base de datos antes de realizar la copia de seguridad y, a continuación, para liberar y montar la base de datos una vez completada la copia de seguridad. Durante una restauración, la aplicación de copia de seguridad y restauración indica al escritor de Exchange que coordine con el almacén de Exchange que desmonte la base de datos, reemplace los archivos de base de datos, Monte la base de datos y, a continuación, vuelva a reproducir los registros de transacciones (según sea necesario).
  
Durante una restauración, el solicitante también se comunica con VSS para preparar el sistema para la restauración y, a continuación, volver a colocar los datos en el dispositivo de almacenamiento masivo. La aplicación de copia de seguridad y restauración también es responsable de trabajar con Windows Server para leer y escribir datos en los medios de almacenamiento de copia de seguridad, ya sea un archivo en cinta, una red de área de almacenamiento u otro medio de copia de seguridad.
  
La base de datos restaurada puede montarse como una base de datos normal, activa o como la base de datos de recuperación 2013 de Exchange. Solo se puede designar una base de datos montada como base de datos de recuperación en cada servidor de Exchange.
  
La información necesaria para completar correctamente las operaciones de copia de seguridad y restauración entre Exchange 2013, VSS y la aplicación de copia de seguridad y restauración se transfiere como parte de los metadatos del escritor de Exchange.
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Tipos de operaciones de copia de seguridad para Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
    
- [Restauración de bases de datos de Exchange 2013](restoring-exchange-2013-databases.md)
    
- [Validar la integridad de la copia de seguridad mediante la API de CHKSGFILES en Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
    
- [Validar la integridad de la copia de seguridad mediante la herramienta Eseutil en Exchange 2013](how-to-validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013.md)
    
## <a name="see-also"></a>Vea también

- [Copia de seguridad y restauración para Exchange](backup-and-restore-for-exchange-2013.md) 
- [Referencia de clase función cchksgfiles](cchksgfiles-class-reference.md) 
- [Servicio de instantáneas de volumen](https://msdn.microsoft.com/library/bb968832%28VS.85%29.aspx) 
- [Windows PowerShell](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
    

