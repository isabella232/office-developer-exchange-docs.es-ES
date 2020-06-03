---
title: Espacios de nombres de agente de transporte en Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c40788e-c182-4502-9202-206e6aaa53f8
description: Obtenga información sobre las clases y los miembros de .NET Framework que puede usar para crear agentes de transporte personalizados para Exchange 2013.
ms.openlocfilehash: fc2d9108c910a730bb48c5be028797f0f15ad4ad
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461796"
---
# <a name="transport-agent-namespaces-in-exchange-2013"></a>Espacios de nombres de agente de transporte en Exchange 2013

Obtenga información sobre las clases y los miembros de .NET Framework que puede usar para crear agentes de transporte personalizados para Exchange 2013.
  
**Se aplica a:** Exchange Server 2013 
  
En este artículo se proporciona información acerca de los espacios de nombres que contienen información de referencia que se puede usar para crear agentes de transporte para Exchange Server 2013. También se describen las clases que los agentes de transporte pueden usar para leer y modificar los mensajes de correo electrónico que pasan a través de la canalización de transporte.
  
## <a name="transport-agent-class-library"></a>Biblioteca de clases de agente de transporte

Los espacios de nombres siguientes contienen tipos que puede usar para crear y ampliar agentes de transporte.

**Tabla 1. Espacios de nombres de .NET Framework**

|**Namespace**|**Descripción**|
|:-----|:-----|
|[Microsoft. Exchange. Data](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.aspx) <br/> |Contiene tipos que especifican los datos y las excepciones de configuración.  <br/> |
|[Microsoft. Exchange. Data. Common](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Common.aspx) <br/> |Contiene tipos que admiten la localización y el control de errores.  <br/> |
|[Microsoft. Exchange. Data. ContentTypes. iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx) <br/> |Contiene tipos que permiten leer y escribir datos de iCalendar.  <br/> |
|[Microsoft. Exchange. Data. ContentTypes. TNEF](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) <br/> |Contiene tipos que permiten leer y escribir datos TNEF.  <br/> |
|[Microsoft. Exchange. Data. ContentTypes. vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx) <br/> |Contiene tipos que permiten leer y escribir datos vCard.  <br/> |
|[Microsoft. Exchange. Data. Globalization](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Globalization.aspx) <br/> |Contiene tipos que permiten trabajar con referencias culturales y juegos de caracteres para generar contenido localizado.  <br/> |
|[Microsoft. Exchange. Data. MIME](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx) <br/> |Contiene tipos que permiten leer y escribir datos MIME.  <br/> |
|[Microsoft. Exchange. Data. MIME. codificadores](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx) <br/> |Contiene tipos que permiten codificar y descodificar datos MIME.  <br/> |
|[Microsoft. Exchange. Data. TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) <br/> |Contiene tipos que permiten leer y escribir datos con formatos de texto diferentes y convertir datos a y desde estos formatos.  <br/> |
|[Microsoft. Exchange. Data. Transport](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.aspx) <br/> |Contiene tipos que permiten obtener acceso a información de enrutamiento, host y dominio sobre la canalización de transporte.  <br/> |
|[Microsoft. Exchange. Data. Transport. Delivery](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.aspx) <br/> |Contiene tipos compatibles con la extensión de los agentes de entrega de Exchange 2013.  <br/> |
|[Microsoft. Exchange. Data. Transport. email](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.aspx) <br/> |Contiene tipos que admiten la creación, lectura, escritura y modificación de mensajes de correo electrónico.  <br/> |
|[Microsoft. Exchange. Data. Transport. Routing](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.aspx) <br/> |Contiene tipos que admiten la extensión del comportamiento de enrutamiento de transporte 2013 de Exchange.  <br/> |
|[Microsoft. Exchange. Data. Transport. SMTP](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.aspx) <br/> |Contiene tipos que admiten la extensión del comportamiento SMTP de transporte 2013 de Exchange.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Agentes de transporte en Exchange](transport-agents-in-exchange-2013.md)   
- [Conceptos del agente de transporte en Exchange 2013](transport-agent-concepts-in-exchange-2013.md) 
- 
  [Referencia de la API de servidor para Exchange](https://msdn.microsoft.com/library/6eddd052-f59f-45b4-b846-7e53d4d7eb16%28Office.15%29.aspx)
- [Elementos del archivo de configuración de agentes para Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)
    

