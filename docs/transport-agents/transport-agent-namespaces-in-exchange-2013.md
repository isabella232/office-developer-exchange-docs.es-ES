---
title: Espacios de nombres de agente en Exchange 2013 de transporte
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c40788e-c182-4502-9202-206e6aaa53f8
description: Obtenga información sobre las clases de .NET Framework y miembros que se pueden utilizar para crear a agentes de transporte personalizados para Exchange 2013.
ms.openlocfilehash: a8189ca9915312b64fefda3091f8f81e51271ad6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763378"
---
# <a name="transport-agent-namespaces-in-exchange-2013"></a>Espacios de nombres de agente en Exchange 2013 de transporte

Obtenga información sobre las clases de .NET Framework y miembros que se pueden utilizar para crear a agentes de transporte personalizados para Exchange 2013.
  
**Se aplica a:** Exchange Server 2013 
  
En este artículo se proporciona información acerca de los espacios de nombres que contienen información de referencia que puede usar para crear a agentes de transporte de Exchange Server 2013. También describe las clases que los agentes de transporte se pueden usar para leer y modificar los mensajes de correo electrónico que pasan a través de la canalización de transporte.
  
## <a name="transport-agent-class-library"></a>Biblioteca de clases de agente de transporte

Los siguientes espacios de nombres contienen tipos que puede usar para crear y ampliar a los agentes de transporte.

**La tabla 1. Espacios de nombres de .NET framework**

|**Namespace**|**Descripción**|
|:-----|:-----|
|[Microsoft.Exchange.Data](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.aspx) <br/> |Contiene tipos que especifican las excepciones de datos y la configuración.  <br/> |
|[Microsoft.Exchange.Data.Common](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Common.aspx) <br/> |Contiene tipos que admiten la localización y tratamiento de errores.  <br/> |
|[Microsoft.Exchange.Data.ContentTypes.iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx) <br/> |Contiene tipos que permiten leer y escribir datos de iCalendar.  <br/> |
|[Microsoft.Exchange.Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) <br/> |Contiene tipos que permiten leer y escribir datos TNEF.  <br/> |
|[Microsoft.Exchange.Data.ContentTypes.vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx) <br/> |Contiene tipos que permiten leer y escribir datos de vCard.  <br/> |
|[Microsoft.Exchange.Data.Globalization](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Globalization.aspx) <br/> |Contiene tipos que permiten trabajar con las referencias culturales y conjuntos a fin de producir contenido localizado de caracteres.  <br/> |
|[Microsoft.Exchange.Data.Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx) <br/> |Contiene tipos que permiten leer y escribir datos MIME.  <br/> |
|[Microsoft.Exchange.Data.Mime.Encoders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx) <br/> |Contiene tipos que permiten codificar y descodificar datos MIME.  <br/> |
|[Microsoft.Exchange.Data.TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) <br/> |Contiene tipos que permiten leer y escribir datos con diferentes formatos de texto y conversión los datos a y desde estos formatos.  <br/> |
|[Microsoft.Exchange.Data.Transport](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.aspx) <br/> |Contiene tipos que permiten tener acceso a información acerca de la canalización de transporte del dominio, host y enrutamiento.  <br/> |
|[Microsoft.Exchange.datos.transporte.espacios de nombre](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.aspx) <br/> |Contiene tipos que admiten la extensión de los agentes de entrega de Exchange 2013.  <br/> |
|[Microsoft.Exchange.Data.Transport.Email](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.aspx) <br/> |Contiene tipos que admiten la creación, lectura, escritura y modificación de los mensajes de correo electrónico.  <br/> |
|[Microsoft.Exchange.Data.Transport.Routing](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.aspx) <br/> |Contiene tipos que admiten la extensión del comportamiento de enrutamiento de transporte de Exchange 2013.  <br/> |
|[Microsoft.Exchange.Data.Transport.Smtp](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.aspx) <br/> |Contiene tipos que admiten la extensión de transporte de Exchange 2013 comportamiento de SMTP.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Los agentes de transporte en Exchange](transport-agents-in-exchange-2013.md)   
- [Conceptos de agente en Exchange 2013 de transporte](transport-agent-concepts-in-exchange-2013.md) 
- [Referencia de API de servidor de Exchange](http://msdn.microsoft.com/library/6eddd052-f59f-45b4-b846-7e53d4d7eb16%28Office.15%29.aspx)
- [Elementos del archivo de configuración de los agentes para Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)
    

