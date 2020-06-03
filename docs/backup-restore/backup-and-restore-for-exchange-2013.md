---
title: Copia de seguridad y restauración para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 329902d9-0ecb-4cfb-86dd-5ce863deff3f
description: Obtenga información acerca de la creación de aplicaciones de copia de seguridad y restauración para Exchange 2013.
ms.openlocfilehash: 1c5d99be60501fd1c4414ea22294bd05645bb0a7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455243"
---
# <a name="backup-and-restore-for-exchange"></a>Copia de seguridad y restauración para Exchange
  
Exchange Server 2013 proporciona grupos de disponibilidad de base de datos (Dag), que ayudan a mantener los datos almacenados protegidos y disponibles, y reducen la necesidad de aplicaciones de copia de seguridad y restauración personalizadas. Los Dag habilitan la redundancia de datos fuera del sitio para ayudar a garantizar que no perderá datos. Sin embargo, muchos planes de recuperación ante desastres continúan incluyendo métodos y sistemas de copia de seguridad y restauración más tradicionales, incluidas las aplicaciones personalizadas, para obtener redundancia con el DAG. Para ayudar a garantizar la disponibilidad de los datos y la redundancia en la organización, puede crear aplicaciones personalizadas que usen las tecnologías de Exchange Server y del sistema operativo Windows Server para realizar copias de seguridad y restaurar los datos de Exchange.

<a name="bk_plugin"> </a>

## <a name="backup-technologies-in-exchange-2013"></a>Tecnologías de copia de seguridad en Exchange 2013

Exchange 2013 incluye un complemento para copias de seguridad de Windows Server que los administradores pueden usar para realizar copias de seguridad basadas en VSS de los datos de Exchange. Los administradores también pueden usar copias de seguridad de Windows Server para realizar copias de seguridad y restauraciones de bases de datos de Exchange. Si va a crear una aplicación de copia de seguridad y restauración para Exchange 2013, debe crear una aplicación compatible con Exchange que admita VSS Writer for Exchange 2013 y use la API CHKSGFILES para validar la coherencia de esa copia de seguridad. Para obtener más información, vea [validar la integridad de la copia de seguridad mediante la API de CHKSGFILES en Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md).

<a name="bk_vsswriter"> </a>

## <a name="vss-writer-in-exchange-2013"></a>VSS Writer en Exchange 2013

Exchange 2013 presenta un cambio importante en la arquitectura del escritor de VSS en Exchange Server 2010 y en Exchange Server 2007. Exchange 2010 y Exchange 2007 incluyen dos escritores de VSS: uno dentro del servicio almacén de información de Exchange (Store. exe) y otro dentro del servicio de replicación de Exchange (MSExchangeRepl. exe). En Exchange 2013, la funcionalidad del escritor de VSS se encuentra en el servicio de replicación de Exchange. La aplicación de copia de seguridad y restauración usa el nuevo escritor de VSS, llamado escritor de Microsoft Exchange, para hacer una copia de seguridad de las copias de bases de datos activas y pasivas, y restaurar copias de seguridad de las bases de datos. Aunque el nuevo VSS Writer se ejecuta en el servicio de replicación de Exchange, el servicio almacén de información de Exchange debe estar en ejecución para que el escritor esté disponible. Como resultado, ambos servicios son necesarios para realizar copias de seguridad o restaurar bases de datos de Exchange.
  
Aunque la arquitectura del escritor de VSS se actualizó en Exchange 2013, la funcionalidad subyacente no ha cambiado. Si ha creado una aplicación de copia de seguridad y restauración para Exchange 2010, no es necesario realizar ningún cambio en la aplicación para Exchange 2013. Asegúrese de volver a compilar la aplicación con los archivos más recientes para garantizar la compatibilidad. Para las aplicaciones de copia de seguridad y restauración creadas para Exchange 2007 o versiones anteriores, tendrá que volver a escribir el código para usar la API de CHKSGFILES más reciente.
  
## <a name="what-you-need-to-know-about-vss-backup-and-restore"></a>Lo que debe saber sobre la copia de seguridad y restauración de VSS

|Si está preguntando por...|Lea esto|
|:-----|:-----|
|Arquitecturas de aplicación  <br/> |Las aplicaciones de copia de seguridad y restauración que usan VSS para hacer copias de seguridad de bases de datos de Exchange suelen consistir en un servicio en segundo plano que realiza la copia de seguridad, un servicio de programación y una consola de aplicación GUI de Windows que controla y configura el sistema de copia de seguridad y restauración.  <br/> |
|Uso remoto  <br/> |Las aplicaciones que usan VSS para hacer copias de seguridad de los servidores de Exchange deben ejecutarse en el equipo con Windows Server 2008 en el que se ejecuta el proceso de almacén de Exchange. Debido a la flexibilidad de los sistemas de almacenamiento de gran tamaño, es posible que el hardware que hospeda los volúmenes de almacenamiento no forme parte físicamente del equipo que ejecuta Windows Server 2008.  <br/> |
|Lenguajes y herramientas  <br/> |Puede usar cualquier lenguaje compatible con COM para usar VSS. Se usa con más frecuencia en aplicaciones escritas en C++. Debido a que tiene que desconectar el almacén de Exchange para crear instantáneas, las aplicaciones de copia de seguridad suelen ser sensibles al tiempo, lo que en la mayoría de los casos hace que no resulte práctico usar lenguajes como Visual Basic o VBScript.  <br/> |
|Implementación administrada  <br/> |Puede usar las API de VSS en un entorno de código administrado a través de un ensamblado de interoperabilidad COM.  <br/> |
|Permite scripts  <br/> |Sí, pero no se recomienda.  <br/> |
|Las pruebas y las herramientas de depuración disponibles  <br/> |No se necesitan herramientas especiales para depurar aplicaciones que usan Windows VSS.  <br/> |
   
## <a name="in-this-section"></a>En esta sección

- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [Creación de aplicaciones de copia de seguridad y restauración para Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Referencia de clase función cchksgfiles](cchksgfiles-class-reference.md)
    
## <a name="see-also"></a>Vea también

- [Servicio de instantáneas de volumen (Windows)](https://msdn.microsoft.com/library/windows/desktop/bb968832%28v=vs.85%29.aspx)   
- [Explorar la API administrada de EWS, EWS y servicios web en Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
- [Exchange Management Shell](../management/exchange-management-shell.md)   
- [Agentes de transporte en Exchange](../transport-agents/transport-agents-in-exchange-2013.md) 
    

