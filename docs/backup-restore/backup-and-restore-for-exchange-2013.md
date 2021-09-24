---
title: Copia de seguridad y restauración para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 329902d9-0ecb-4cfb-86dd-5ce863deff3f
description: Busque información sobre cómo crear aplicaciones de copia de seguridad y restauración para Exchange 2013.
ms.openlocfilehash: 2be8295985651319860ab2d2a143d69f663bf932
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514903"
---
# <a name="backup-and-restore-for-exchange"></a>Copia de seguridad y restauración para Exchange
  
Exchange Server 2013 proporciona grupos de disponibilidad de base de datos (DAG), que ayudan a mantener los datos almacenados seguros y disponibles, y reducen la necesidad de realizar copias de seguridad y restaurar aplicaciones personalizadas. Los DAG habilitan la redundancia de datos fuera del sitio para ayudar a garantizar que no perderá datos. Sin embargo, muchos planes de recuperación ante desastres siguen incluyendo sistemas y métodos de copia de seguridad y restauración más tradicionales, incluidas las aplicaciones personalizadas, para redundancia con el DAG. Para garantizar la disponibilidad y redundancia de datos en su organización, puede crear aplicaciones personalizadas que usen tecnologías del sistema operativo Exchange Server y Windows Server para realizar copias de seguridad y restaurar los datos Exchange datos.

<a name="bk_plugin"> </a>

## <a name="backup-technologies-in-exchange-2013"></a>Tecnologías de copia de seguridad Exchange 2013

Exchange 2013 incluye un complemento para la copia de seguridad de servidor de Windows que los administradores pueden usar para realizar copias de seguridad basadas en VSS de Exchange datos. Los administradores también pueden usar Windows server Backup para realizar copias de seguridad y restaurar Exchange bases de datos. Si va a crear una aplicación de copia de seguridad y restauración para Exchange 2013, debe crear una aplicación compatible con Exchange que admita el escritor de VSS para Exchange 2013 y usar la API CHKSGFILES para validar la coherencia de esa copia de seguridad. Para obtener más información, vea [Validate backup integrity by using the CHKSGFILES API in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md).

<a name="bk_vsswriter"> </a>

## <a name="vss-writer-in-exchange-2013"></a>Escritor vss en Exchange 2013

Exchange 2013 presenta un cambio significativo en la arquitectura del escritor vss en Exchange Server 2010 y Exchange Server 2007. Exchange 2010 y Exchange 2007 incluyen dos escritores de VSS: uno dentro del servicio de almacén de información de Exchange (store.exe) y otro dentro del servicio de replicación de Exchange (msexchangerepl.exe). En Exchange 2013, la funcionalidad de escritor vss se encuentra en el servicio de replicación Exchange vss. La aplicación de copia de seguridad y restauración usa el nuevo escritor de VSS, llamado Escritor de Microsoft Exchange, para realizar copias de seguridad de bases de datos activas y pasivas, y para restaurar copias de base de datos copiadas. Aunque el nuevo escritor vss se ejecuta en el servicio de replicación de Exchange, el servicio de almacén de información de Exchange debe ejecutarse para que el escritor esté disponible. Como resultado, ambos servicios son necesarios para realizar copias de seguridad o restaurar bases de datos de Exchange.
  
Aunque la arquitectura del escritor vss se actualizó en Exchange 2013, la funcionalidad subyacente no ha cambiado. Si creó una aplicación de copia de seguridad y restauración para Exchange 2010, no es necesario realizar cambios en la aplicación para Exchange 2013. Asegúrese de volver a compilar la aplicación con los archivos más recientes para garantizar la compatibilidad. Para las aplicaciones de copia de seguridad y restauración creadas para Exchange 2007 o versiones anteriores, deberá reescribir el código para usar la API de CHKSGFILES más reciente.
  
## <a name="what-you-need-to-know-about-vss-backup-and-restore"></a>Lo que necesita saber acerca de la copia de seguridad y restauración de VSS

|Si te estás preguntando acerca de...|Lea esto|
|:-----|:-----|
|Arquitecturas de aplicación  <br/> |Las aplicaciones de copia de seguridad y restauración que usan VSS para hacer una copia de seguridad de bases de datos de Exchange suelen estar formadas por un servicio en segundo plano que realiza la copia de seguridad, un servicio de programación y una consola de aplicaciones gui de Windows que controla y configura el sistema de copia de seguridad y restauración.  <br/> |
|Uso remoto  <br/> |Las aplicaciones que usan VSS para realizar una copia de seguridad de los servidores Exchange deben ejecutarse en el equipo de Windows Server 2008 en el que se ejecuta el proceso Exchange almacén. Debido a la flexibilidad de los sistemas de almacenamiento grandes, es posible que el hardware que hospeda los volúmenes de almacenamiento no sea físicamente parte del equipo que ejecuta Windows Server 2008.  <br/> |
|Lenguajes y herramientas  <br/> |Puede usar cualquier idioma compatible con COM para usar VSS. Se usa con más frecuencia en aplicaciones escritas en C++. Dado que debe desconectar el almacén de Exchange para crear instantáneas, las aplicaciones de copia de seguridad suelen ser de tiempo, lo que en la mayoría de los casos hace que el uso de idiomas como Visual Basic o VBScript sea poco práctico.  <br/> |
|Implementación administrada  <br/> |Puede usar las API de VSS en un entorno de código administrado a través de un ensamblado de interoperabilidad COM.  <br/> |
|Permite scripts  <br/> |Sí, pero no se recomienda.  <br/> |
|Las pruebas y las herramientas de depuración disponibles  <br/> |No se necesitan herramientas especiales para depurar aplicaciones que usan el Windows VSS.  <br/> |
   
## <a name="in-this-section"></a>En esta sección

- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [Crear aplicaciones de copia de seguridad y restauración para Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Referencia de la clase CChkSGFiles](cchksgfiles-class-reference.md)
    
## <a name="see-also"></a>Ver también

- [Servicio de instantáneas de volumen (Windows)](https://msdn.microsoft.com/library/windows/desktop/bb968832%28v=vs.85%29.aspx)   
- [Explorar la API administrada de EWS, EWS y servicios web en Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
- [Exchange Management Shell](../management/exchange-management-shell.md)   
- [Agentes de transporte en Exchange](../transport-agents/transport-agents-in-exchange-2013.md) 
    

