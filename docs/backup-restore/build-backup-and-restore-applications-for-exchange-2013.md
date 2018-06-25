---
title: Crear copia de seguridad y restauración de aplicaciones para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e5e952a5-add1-417c-a3c2-230f4dc99b00
description: Busque información sobre los componentes y la arquitectura de las aplicaciones de copia de seguridad y restauración para Exchange 2013 y los requisitos del sistema para la creación de una copia de seguridad y restauración de la aplicación.
ms.openlocfilehash: e85a5364c40c472c9e1ea9d1d3b4e89329b1676f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19762986"
---
# <a name="build-backup-and-restore-applications-for-exchange-2013"></a>Crear copia de seguridad y restauración de aplicaciones para Exchange 2013

Busque información sobre los componentes y la arquitectura de las aplicaciones de copia de seguridad y restauración para Exchange 2013 y los requisitos del sistema para la creación de una copia de seguridad y restauración de la aplicación.
  
**Se aplica a:** Exchange Server 2013 
  
Puede usar el [Servicio de instantáneas de volumen (VSS)](http://msdn.microsoft.com/en-us/library/bb968832%28VS.85%29.aspx) en las versiones de Windows Server 2008 a partir de Windows Server para crear aplicaciones de copia de seguridad y restauración datos de Exchange Server 2013. VSS proporciona una infraestructura que le permite crear y administrar las instantáneas a través de sistemas de administración de almacenamiento de terceros, aplicaciones empresariales y hardware. Puede crear soluciones basadas en la infraestructura de VSS que usar instantáneas para copia de seguridad y restaurar una o varias bases de datos de Exchange 2013. 
  
## <a name="backup-and-restore-application-prerequisites"></a>Requisitos previos de aplicación de copia de seguridad y restauración
<a name="bk_systemrequirements"> </a>

En orden para su aplicación de restauración y copia de seguridad personalizada y VSS para copia de seguridad y restauración de bases de datos de Exchange 2013, su entorno debe incluir lo siguiente:
  
- Una versión de Windows Server 2008 a partir de Windows Server 
    
- Exchange 2013
    
Además, si está creando una copia de seguridad y restauración de la aplicación, debe tener en cuenta las restricciones siguientes en el entorno de desarrollo:
  
- VSS es una API de COM no administrada que se puede tener acceso desde el código administrado de .NET Framework a través de un ensamblado de interoperabilidad de COM.
    
- El Shell de administración de Exchange es una aplicación administrada que se tiene acceso a través de código administrado de .NET Framework.
    
- La API de CHKSGFILES que se suministra con Exchange 2013 es una DLL de 64 bits de código nativo. No se admite el uso de la DLL de CHKSGFILES de Exchange 2007 de 32 bits con las bases de datos de Exchange 2013.
    
## <a name="backup-and-restore-application-overview"></a>Información general de aplicaciones de copia de seguridad y restauración
<a name="bk_components"> </a>

VSS coordina la comunicación entre los componentes siguientes: 
  
- El solicitante VSS, que es la aplicación de copia de seguridad
    
- El escritor de VSS
    
- El proveedor VSS, que es de los componentes del sistema, el software o hardware que crean las instantáneas de volumen
    
Para utilizar VSS para realizar una copia de seguridad de los datos de Exchange 2013, la aplicación de copia de seguridad debe ser un solicitante VSS de Exchange 2013 reconozca. Exchange 2013 incluye un escritor de VSS, llamado el escritor de Exchange de Microsoft, el programa de copia de seguridad de Windows Server; Sin embargo, el escritor de Exchange sólo realiza una copia de volúmenes de todo. No una copia de seguridad individuales Exchange 2013 bases de datos. Si necesita más flexibilidad, puede usar una aplicación de copia de seguridad de otro fabricante que tiene un escritor de VSS para Exchange puede trabajar con bases de datos individuales de Exchange, o puede crear a un solicitante VSS personalizado.
  
Antes de la aplicación llama a VSS para iniciar una copia de seguridad, debe obtener información acerca de la configuración de almacenamiento para el sistema de Exchange 2013 que hacer la copia de seguridad. Dicha información se almacena en los servicios de dominio de Active Directory (AD DS). La aplicación de copia de seguridad puede obtener datos de configuración de almacenamiento de Exchange mediante el uso de comandos de Shell de administración de Exchange. Para obtener más información, consulte [Exchange Server PowerShell (Shell de administración de Exchange)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps). 
  
Las aplicaciones de copia de seguridad de Exchange 2013 llamar a las API de COM de VSS para crear completa, copiar, copias de seguridad diferenciales e incrementales de las bases de datos de Exchange; no interactúan directamente con el escritor de VSS. La funcionalidad de grupo de disponibilidad de base de datos (DAG) de Exchange también permite que la aplicación crear una copia de seguridad totalmente coherente, incluso si la copia de seguridad completa inicial y copias de seguridad incrementales más adelante proceden de distintos servidores en el DAG. Después de VSS crea la copia de los datos de Exchange, la aplicación de copia de seguridad almacena los datos en los medios previstos.
  
Para restaurar una base de datos de Exchange 2013, la aplicación de restauración recupera los archivos de registro y base de datos de los medios de copia de seguridad y los almacena en el almacenamiento en disco activo de un servidor de Exchange. Bases de datos individuales no están asociados con un determinado servidor de Exchange. 
  
Las aplicaciones de copia de seguridad y restauración deben especificar un número de parámetros específicos de Exchange 2013 correctamente, controlar y administrar las operaciones de ejecución por VSS frente a las bases de datos de Exchange 2013. Por ejemplo, dado que Exchange 2013 admite hasta 100 bases de datos activos simultáneamente, la aplicación de copia de seguridad debe especificar correctamente y procesar el archivo de base de datos, los archivos de registro de transacciones y componentes de base de datos de archivo de punto de control.
  
Para reconstruir una base de datos que han tenido cambios desde la última copia completa, la aplicación de restauración requiere la base de datos y archivos de registro de las copias de seguridad diferentes. Por ejemplo, puede requerir una copia de seguridad completa semanal y uno o más incrementales copias de seguridad diarias. En Exchange 2013 sistemas que usan dag, la aplicación de restauración puede volver a generar una base de datos mediante el uso de las copias de seguridad de las copias de base de datos diferente en servidores diferentes en el mismo DAG. Sin embargo, la única manera admitida para restaurar una base de datos de DAG a partir de copia de seguridad es restaurar todas las copias activas y pasivas de la base de datos mediante el uso de los mismos datos.
  
Una vez todos los datos, la aplicación de restauración señales de Exchange para comprobar la integridad de la base de datos y archivos de registro. Si la base de datos y archivos de registro se hayan restaurado correctamente, el servidor de Exchange, a continuación, puede reproducir los archivos de registro de la base de datos para que aparezca la base de datos actualizado y montar. Si se ha recuperado la base de datos a un servidor que ya tiene una copia activa de la base de datos montada, la base de datos se trata como una base de datos de recuperación. Si se ha recuperado la base de datos en un servidor diferente, la base de datos o bien se puede montar de forma independiente, o que la réplica puede agregarse a continuación, en el DAG.
  
## <a name="backup-and-restore-system-architecture"></a>Arquitectura del sistema de copia de seguridad y restauración
<a name="bk_ExchangeVSS"> </a>

VSS se comunica con el sistema de archivos de Windows Server y con el controlador de dispositivo de almacenamiento masivo a través de un proveedor de terceros (o personalizado). El proveedor de hardware determina donde se creará la instantánea. VSS resume la instantánea de hardware específicos para que la aplicación de copia de seguridad y restauración puede tener acceso a la instantánea sin información acerca de los detalles de implementación de hardware. La siguiente ilustración muestra cómo interactúa la aplicación de copia de seguridad y restauración con Exchange 2013 y Windows Server.
  
**En la figura 1. Arquitectura del sistema de copia de seguridad y restauración**

![Diagrama que muestra cómo interactúa una aplicación de copia de seguridad y restauración. Existe una comunicación bidireccional entre Exchange, Windows Server y la aplicación cliente. Windows Server también actúa con un dispositivo de almacenamiento masivo o un medio de copia de seguridad.](media/VSS_architecture_E2k7.gif)
  
La aplicación de copia de seguridad y restauración funciona como el solicitante VSS. El solicitante se comunica con VSS para obtener información acerca de Exchange 2013, para iniciar la creación de instantáneas de volumen y para obtener acceso a los datos de copia de seguridad. 
  
El almacén de Exchange es un componente de Exchange 2013 y tiene acceso a las bases de datos de Exchange 2013 mediante el sistema de archivos de Windows Server. En el sistema de archivos, cada servidor de Exchange puede montar simultáneamente hasta 100 bases de datos con un archivo de punto de control, los archivos de registro de transacciones y sus archivos de base de datos (.edb) que lo acompaña.
  
Para admitir VSS, Exchange 2013 incluye un escritor de Exchange que se integra el almacén de Exchange. El escritor de Exchange se coordina con el almacén de Exchange (en funcionamiento en nombre del solicitante) para inmovilizar y desmontar la base de datos antes de la copia de seguridad y, a continuación liberar y montar la base de datos después de la copia de seguridad se completa. Durante una restauración, la aplicación de copia de seguridad y restauración indica el escritor de Exchange para coordinar con el almacén de Exchange para desmontar la base de datos, reemplazar los archivos de base de datos, monte la base de datos y, a continuación, volver a reproducir los registros de transacciones (según sea necesario).
  
Durante una restauración, el solicitante también se comunica con VSS para preparar el sistema para la restauración y, a continuación, para colocar los datos de copia en el dispositivo de almacenamiento masivo. La aplicación de copia de seguridad y restauración también es responsable de trabajar con el servidor de Windows para leer datos desde y escribir datos en los medios de almacenamiento de copia de seguridad, si una cinta archivar, una red de área de almacenamiento u otro medio de copia de seguridad.
  
Como una base de datos activa, regular, o bien como la base de datos de recuperación de Exchange 2013, se puede montar la base de datos restaurada. Sólo una base de datos montada se puede designar como una base de datos de recuperación en cada servidor de Exchange.
  
Información necesaria para finalizar la copia de seguridad correctamente y restaurar las operaciones entre Exchange 2013, VSS, y la aplicación de copia de seguridad y restauración se transfiere como parte de los metadatos del escritor de Exchange.
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Tipos de operaciones de copia de seguridad para Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
    
- [Restauración de bases de datos de Exchange 2013](restoring-exchange-2013-databases.md)
    
- [Validar la integridad de la copia de seguridad mediante el uso de la API CHKSGFILES en Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
    
- [Validar la integridad de la copia de seguridad mediante la herramienta Eseutil en Exchange 2013](how-to-validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013.md)
    
## <a name="see-also"></a>Vea también

- [Copia de seguridad y restauración para Exchange](backup-and-restore-for-exchange-2013.md) 
- [Referencia de clase CChkSGFiles](cchksgfiles-class-reference.md) 
- [Servicio de instantáneas de volumen](http://msdn.microsoft.com/en-us/library/bb968832%28VS.85%29.aspx) 
- [Windows PowerShell](http://msdn.microsoft.com/en-us/library/dd835506%28v=vs.85%29.aspx)
    

