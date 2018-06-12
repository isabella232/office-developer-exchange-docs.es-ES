---
title: Copia de seguridad y restauración para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 329902d9-0ecb-4cfb-86dd-5ce863deff3f
description: Obtenga información sobre la creación de copia de seguridad y restauración de aplicaciones para Exchange 2013.
ms.openlocfilehash: 9eceb3d512a73ad9cb07a01864fb8b029d5b5772
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19762975"
---
# <a name="backup-and-restore-for-exchange"></a>Copia de seguridad y restauración para Exchange
  
Exchange Server 2013 proporciona grupos de disponibilidad de base de datos (dag), que ayudan a mantener los datos almacenados segura y disponible y reducir la necesidad de copia de seguridad personalizada y restauración de aplicaciones. Dag habilitar la redundancia de datos fuera del sitio ayudar a garantizar que no se pierdan datos. Sin embargo, muchos planes de recuperación ante desastres continuarán incluir más tradicional copia de seguridad y restauración de métodos y sistemas, incluidas las aplicaciones personalizadas, con fines de redundancia con el DAG. Para ayudar a garantizar la disponibilidad de los datos y redundancia en su organización, puede crear aplicaciones personalizadas que usan tecnologías de sistema operativo de Exchange Server y Windows Server para hacer una copia de y restaurar los datos de Exchange.

<a name="bk_plugin"> </a>

## <a name="backup-technologies-in-exchange-2013"></a>Tecnologías de copia de seguridad de Exchange 2013

Exchange 2013 incluye un complemento para la copia de seguridad de servidor de Windows que los administradores pueden usar para realizar copias de seguridad basadas en VSS de datos de Exchange. Los administradores también pueden usar copias de seguridad de Windows Server para hacer una copia de y restauración de bases de datos de Exchange. Si está creando una copia de seguridad y restauración de aplicaciones para Exchange 2013, debe crear una aplicación compatible con Exchange que admite el escritor de VSS para Exchange 2013 y usar la API de CHKSGFILES para validar la coherencia de esa copia de seguridad. Para obtener más información, consulte [Validate integridad de la copia de seguridad mediante el uso de la API CHKSGFILES en Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md).

<a name="bk_vsswriter"> </a>

## <a name="vss-writer-in-exchange-2013"></a>Escritor de VSS de Exchange 2013

Exchange 2013 presenta un cambio significativo para la arquitectura del escritor VSS de Exchange Server 2010 y Exchange Server 2007. Exchange 2010 y Exchange 2007 incluyen dos escritores de VSS: uno dentro del servicio de almacén de información de Exchange (store.exe) y otra dentro del servicio de replicación de Exchange (msexchangerepl.exe). En Exchange 2013, la funcionalidad de escritor VSS se encuentra en el servicio de replicación de Exchange. La aplicación de copia de seguridad y restauración usa el nuevo escritor de VSS, llamado el escritor de Exchange de Microsoft, para realizar una copia de seguridad de copias activas y pasivas de base de datos, y restaurar una copia de copias de base de datos. Aunque el escritor VSS nuevo se ejecuta en el servicio de replicación de Exchange, debe ejecutar el servicio de almacenamiento de información de Exchange en orden para el sistema de escritura para que esté disponible. Como resultado, ambos servicios son necesarios para realizar una copia de o restaurar las bases de datos de Exchange.
  
Aunque se actualizó la arquitectura del escritor VSS de Exchange 2013, la funcionalidad subyacente no ha cambiado. Si ha creado una aplicación de copia de seguridad y restauración para Exchange 2010, no es necesario realizar cambios en la aplicación para Exchange 2013. Asegúrese de volver a compilar la aplicación con los archivos más recientes para garantizar la compatibilidad. Copia de seguridad y restauración en las aplicaciones creadas para Exchange 2007 o versiones anteriores, debe volver a escribir el código para utilizar la API de CHKSGFILES más reciente.
  
## <a name="what-you-need-to-know-about-vss-backup-and-restore"></a>Lo que necesita saber acerca de la restauración y copia de seguridad VSS

|Si se pregunta acerca de...|Lea esto|
|:-----|:-----|
|Arquitecturas de aplicación  <br/> |Copia de seguridad y restauración de aplicaciones que usan VSS para realizar una copia de seguridad de las bases de datos normalmente constan de un servicio en segundo plano que realiza la copia de seguridad, un servicio de programación y una consola de aplicación de interfaz gráfica de usuario de Windows que controla y configura la copia de seguridad y restauración del sistema de Exchange.  <br/> |
|Uso remoto  <br/> |Deben ejecutar aplicaciones que usan VSS para realizar una copia de seguridad de los servidores de Exchange en el equipo de Windows Server 2008 en el que se ejecuta el proceso de almacén de Exchange. Debido a la flexibilidad en sistemas de almacenamiento de gran tamaño, el hardware que hospeda los volúmenes de almacenamiento podría no ser físicamente parte del equipo que ejecuta Windows Server 2008.  <br/> |
|Lenguajes y herramientas  <br/> |Puede usar cualquier lenguaje compatible con COM para utilizar VSS. Se usa con más frecuencia en las aplicaciones escritas en C++. Dado que tiene que seguir el almacén de Exchange sin conexión para crear instantáneas de volumen, las aplicaciones de copia de seguridad son normalmente urgente, que en la mayoría de los casos, facilita el uso de lenguajes como Visual Basic o VBScript poco práctico.  <br/> |
|Implementación administrada  <br/> |Puede usar las API de VSS en un entorno de código administrado a través de un ensamblado de interoperabilidad de COM.  <br/> |
|Permite scripts  <br/> |Sí, pero no se recomienda.  <br/> |
|Las pruebas y las herramientas de depuración disponibles  <br/> |No hay herramientas especiales necesarios para depurar las aplicaciones que usan el VSS de Windows.  <br/> |
   
## <a name="in-this-section"></a>En esta sección

- [Conceptos de copia de seguridad y restauración para Exchange 2013](backup-and-restore-concepts-for-exchange-2013.md)
    
- [Crear copia de seguridad y restauración de aplicaciones para Exchange 2013](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Referencia de clase CChkSGFiles](cchksgfiles-class-reference.md)
    
## <a name="see-also"></a>Ver también

- [Servicio de instantáneas de volumen (Windows)](http://msdn.microsoft.com/en-us/library/windows/desktop/bb968832%28v=vs.85%29.aspx)   
- [Explore la API administrada de EWS, EWS y servicios web de Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
- [Shell de administración de Exchange](../management/exchange-management-shell.md)   
- [Los agentes de transporte en Exchange](../transport-agents/transport-agents-in-exchange-2013.md) 
    

