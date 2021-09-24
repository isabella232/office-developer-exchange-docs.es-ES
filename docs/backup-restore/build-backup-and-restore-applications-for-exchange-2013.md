---
title: Crear aplicaciones de copia de seguridad y restauración para Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e5e952a5-add1-417c-a3c2-230f4dc99b00
description: Encuentre información sobre los componentes y la arquitectura de las aplicaciones de copia de seguridad y restauración para Exchange 2013 y los requisitos del sistema para crear una aplicación de copia de seguridad y restauración.
ms.openlocfilehash: 590ac029e157196d370cbcbe54e5df75bc1a830b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513881"
---
# <a name="build-backup-and-restore-applications-for-exchange-2013"></a>Crear aplicaciones de copia de seguridad y restauración para Exchange 2013

Encuentre información sobre los componentes y la arquitectura de las aplicaciones de copia de seguridad y restauración para Exchange 2013 y los requisitos del sistema para crear una aplicación de copia de seguridad y restauración.
  
**Se aplica a:** Exchange Server 2013 
  
Puede usar el Servicio de instantáneas de volumen [(VSS)](https://msdn.microsoft.com/library/bb968832%28VS.85%29.aspx) en versiones de Windows Server a partir de Windows Server 2008 para crear aplicaciones que copian de seguridad y restauran Exchange Server datos de 2013. VSS proporciona una infraestructura que permite crear y administrar instantáneas en sistemas de administración de almacenamiento de terceros, aplicaciones empresariales y hardware. Puede crear soluciones basadas en la infraestructura de VSS que usan instantáneas para realizar una copia de seguridad y restaurar una o más Exchange bases de datos de 2013. 
  
## <a name="backup-and-restore-application-prerequisites"></a>Requisitos previos de la aplicación de copia de seguridad y restauración
<a name="bk_systemrequirements"> </a>

Para que la aplicación de copia de seguridad y restauración personalizada y VSS realicen una copia de seguridad y restaure Exchange bases de datos de 2013, el entorno debe incluir lo siguiente:
  
- Una versión de Windows Server a partir de Windows Server 2008 
    
- Exchange 2013
    
Además, si va a crear una aplicación de copia de seguridad y restauración, debe tener en cuenta las siguientes restricciones en el entorno de desarrollo:
  
- VSS es una API COM no administrada a la que se puede obtener acceso .NET Framework código administrado mediante un ensamblado de interoperabilidad COM.
    
- El Shell Exchange administración es una aplicación administrada a la que se accede a través .NET Framework código administrado.
    
- La API CHKSGFILES que se proporciona con Exchange 2013 es un DLL de 64 bits de código nativo. No se admite el Exchange DLL de CHKSGFILES de 32 bits de 2007 con Exchange de 2013.
    
## <a name="backup-and-restore-application-overview"></a>Introducción a la copia de seguridad y restauración de aplicaciones
<a name="bk_components"> </a>

VSS coordina la comunicación entre los siguientes componentes: 
  
- El solicitante de VSS, que es la aplicación de copia de seguridad
    
- Escritor vss
    
- El proveedor vss, que es el sistema, software o componentes de hardware que crean las instantáneas
    
Para usar VSS para realizar una copia Exchange datos de 2013, la aplicación de copia de seguridad debe ser un Exchange VSS para 2013. Exchange 2013 incluye un escritor de VSS, denominado Microsoft Exchange Writer, para el programa de copia de seguridad de Windows Server; sin embargo, Exchange escritor solo hace una copia de seguridad de volúmenes enteros. No realiza una copia de seguridad de Exchange bases de datos de 2013. Si necesita más flexibilidad, puede usar una aplicación de copia de seguridad de terceros que tenga un escritor vss consciente de Exchange que pueda trabajar con bases de datos de Exchange individuales o puede crear un solicitante vss personalizado.
  
Antes de que la aplicación llame a VSS para iniciar una copia de seguridad, debe obtener información sobre la configuración de almacenamiento del sistema de Exchange 2013 al que está haciendo una copia de seguridad. Esa información se almacena en Servicios de dominio de Active Directory (AD DS). La aplicación de copia de seguridad puede obtener Exchange de configuración de almacenamiento mediante Exchange comandos del Shell de administración. Para obtener más información, [vea Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps). 
  
Exchange de copia de seguridad de 2013 llaman a las API COM de VSS para crear copias de seguridad completas, de copia, diferenciales e incrementales de Exchange bases de datos; no interactúan directamente con el escritor de VSS. La funcionalidad grupo de disponibilidad de base de datos (DAG) de Exchange también permite a la aplicación crear una copia de seguridad totalmente coherente, incluso si la copia de seguridad completa inicial y las copias de seguridad incrementales posteriores provienen de diferentes servidores del DAG. Después de que VSS cree la copia de los Exchange, la aplicación de copia de seguridad almacena los datos en el medio previsto.
  
Para restaurar una base de datos de Exchange 2013, la aplicación de restauración recupera la base de datos y los archivos de registro de los medios de copia de seguridad y los almacena en el almacenamiento en disco activo de un servidor Exchange servidor. Las bases de datos individuales no están asociadas a un servidor Exchange particular. 
  
Las aplicaciones de copia de seguridad y restauración deben especificar una serie de parámetros específicos de Exchange 2013 para controlar y administrar correctamente las operaciones ejecutadas por VSS en Exchange bases de datos de 2013. Por ejemplo, dado que Exchange 2013 admite hasta 100 bases de datos activas simultáneamente, la aplicación de copia de seguridad debe especificar y procesar correctamente el archivo de base de datos, los archivos de registro de transacciones y los componentes de la base de datos de archivos de punto de control.
  
Para reconstruir una base de datos que ha tenido cambios desde la última copia de seguridad completa, la aplicación de restauración requiere archivos de registro y base de datos de distintas copias de seguridad. Por ejemplo, puede requerir una copia de seguridad completa semanal y una o más copias de seguridad incrementales diarias. En Exchange 2013 que usan DAG, la aplicación de restauración puede volver a generar una base de datos mediante copias de seguridad de diferentes copias de base de datos en distintos servidores del mismo DAG. Sin embargo, la única forma admitida de restaurar una base de datos de DAG a partir de la copia de seguridad es restaurar todas las copias activas y pasivas de la base de datos mediante los mismos datos.
  
Una vez que todos los datos están en su lugar, la aplicación de restauración Exchange para comprobar la integridad de la base de datos y los archivos de registro. Si la base de datos y los archivos de registro se han restaurado correctamente, el servidor Exchange puede reproducir los archivos de registro de la base de datos para poner la base de datos actualizada y montarla. Si la base de datos se ha recuperado en un servidor que ya tiene una copia activa de la base de datos montada, la base de datos se tratará como una base de datos de recuperación. Si la base de datos se ha recuperado en un servidor diferente, la base de datos puede montarse de forma independiente o esa réplica se puede agregar al DAG.
  
## <a name="backup-and-restore-system-architecture"></a>Arquitectura del sistema de copia de seguridad y restauración
<a name="bk_ExchangeVSS"> </a>

VSS se comunica con el Windows de archivos del servidor y con el controlador de dispositivo de almacenamiento masivo a través de un proveedor de terceros (o personalizado). El proveedor de hardware determina dónde se creará la instantánea. VSS abstrae la instantánea específica del hardware para que la aplicación de copia de seguridad y restauración pueda tener acceso a la instantánea sin información sobre los detalles de implementación de hardware. En la siguiente figura se muestra cómo interactúa la aplicación de copia de seguridad y restauración con Exchange 2013 y Windows Server.
  
**Figura 1. Arquitectura del sistema de copia de seguridad y restauración**

![Diagrama que muestra cómo interactúa una aplicación de copia de seguridad y restauración. Existe una comunicación bidireccional entre Exchange, Windows Server y la aplicación cliente. Windows Server también actúa con un dispositivo de almacenamiento masivo o un medio de copia de seguridad.](media/VSS_architecture_E2k7.gif)
  
La aplicación de copia de seguridad y restauración funciona como solicitante de VSS. El solicitante se comunica con VSS para obtener información sobre Exchange 2013, iniciar la creación de instantáneas y obtener acceso a los datos para la copia de seguridad. 
  
El Exchange es un componente de Exchange 2013 y tiene acceso a Exchange bases de datos de 2013 a través del sistema de archivos Windows server. Dentro del sistema de archivos, cada servidor Exchange puede montar simultáneamente hasta 100 bases de datos con sus archivos de base de datos (.edb) adjuntos, archivos de registro de transacciones y un archivo de punto de control.
  
Para admitir VSS, Exchange 2013 incluye un Exchange de escritura integrado en el Exchange cliente. El escritor de Exchange se coordina con el almacén de Exchange (que funciona en nombre del solicitante) para inmovilizar y desmontar la base de datos antes de realizar la copia de seguridad y, a continuación, descongelar y montar la base de datos una vez completada la copia de seguridad. Durante una restauración, la aplicación de copia de seguridad y restauración indica al escritor de Exchange que coordine con el almacén de Exchange para desmontar la base de datos, reemplazar los archivos de base de datos, montar la base de datos y, a continuación, reproducir los registros de transacciones (según sea necesario).
  
Durante una restauración, el solicitante también se comunica con VSS para preparar el sistema para la restauración y, a continuación, para volver a colocar los datos en el dispositivo de almacenamiento masivo. La aplicación de copia de seguridad y restauración también es responsable de trabajar con Windows Server para leer y escribir datos en los medios de almacenamiento de copia de seguridad, ya sea un archivo de cinta, una red de área de almacenamiento u otro medio de copia de seguridad.
  
La base de datos restaurada se puede montar como una base de datos activa normal o como la base de datos de recuperación Exchange 2013. Solo se puede designar una base de datos montada como base de datos de recuperación en cada Exchange servidor.
  
La información necesaria para completar correctamente las operaciones de copia de seguridad y restauración entre Exchange 2013, VSS y la aplicación de copia de seguridad y restauración se transfiere como parte de los metadatos del Exchange escritor.
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Tipos de operaciones de copia de seguridad para Exchange 2013](types-of-backup-operations-for-exchange-2013.md)
    
- [Restauración de Exchange bases de datos de 2013](restoring-exchange-2013-databases.md)
    
- [Validar la integridad de copia de seguridad mediante la API CHKSGFILES en Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
    
- [Validar la integridad de copia de seguridad mediante la herramienta Eseutil en Exchange 2013](how-to-validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013.md)
    
## <a name="see-also"></a>Ver también

- [Copia de seguridad y restauración para Exchange](backup-and-restore-for-exchange-2013.md) 
- [Referencia de la clase CChkSGFiles](cchksgfiles-class-reference.md) 
- [Servicio de instantáneas de volumen](https://msdn.microsoft.com/library/bb968832%28VS.85%29.aspx) 
- [Windows PowerShell](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
    

