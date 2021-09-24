---
title: Espacios de nombres de agente de transporte Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5c40788e-c182-4502-9202-206e6aaa53f8
description: Obtenga información sobre las .NET Framework y los miembros que puede usar para crear agentes de transporte personalizados para Exchange 2013.
ms.openlocfilehash: 076ddb8e2ccbdfa195a68aca6b296337a2876b55
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59537133"
---
# <a name="transport-agent-namespaces-in-exchange-2013"></a>Espacios de nombres de agente de transporte Exchange 2013

Obtenga información sobre las .NET Framework y los miembros que puede usar para crear agentes de transporte personalizados para Exchange 2013.
  
**Se aplica a:** Exchange Server 2013 
  
En este artículo se proporciona información sobre los espacios de nombres que contienen información de referencia que puede usar para crear agentes de transporte para Exchange Server 2013. También describe las clases que los agentes de transporte pueden usar para leer y modificar mensajes de correo electrónico que pasan a través de la canalización de transporte.
  
## <a name="transport-agent-class-library"></a>Biblioteca de clases de agente de transporte

Los siguientes espacios de nombres contienen tipos que puede usar para crear y ampliar agentes de transporte.

**Tabla 1. .NET Framework espacios de nombres**

|**Namespace**|**Descripción**|
|:-----|:-----|
|[Microsoft. Exchange. Datos](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.aspx) <br/> |Contiene tipos que especifican excepciones de configuración y datos.  <br/> |
|[Microsoft. Exchange.Data.Common](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Common.aspx) <br/> |Contiene tipos que admiten la localización y el control de errores.  <br/> |
|[Microsoft. Exchange. Data.ContentTypes.iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx) <br/> |Contiene tipos que permiten leer y escribir datos de iCalendar.  <br/> |
|[Microsoft. Exchange. Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) <br/> |Contiene tipos que permiten leer y escribir datos TNEF.  <br/> |
|[Microsoft. Exchange. Data.ContentTypes.vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx) <br/> |Contiene tipos que permiten leer y escribir datos de vCard.  <br/> |
|[Microsoft. Exchange. Data.Globalization](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Globalization.aspx) <br/> |Contiene tipos que permiten trabajar con culturas y conjuntos de caracteres para producir contenido localizado.  <br/> |
|[Microsoft. Exchange. Data.Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx) <br/> |Contiene tipos que permiten leer y escribir datos MIME.  <br/> |
|[Microsoft. Exchange. Data.Mime.Encoders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx) <br/> |Contiene tipos que permiten codificar y descodificar datos MIME.  <br/> |
|[Microsoft. Exchange. Data.TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) <br/> |Contiene tipos que permiten leer y escribir datos con diferentes formatos de texto y convertir datos a y desde esos formatos.  <br/> |
|[Microsoft. Exchange. Data.Transport](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.aspx) <br/> |Contiene tipos que permiten tener acceso a la información de enrutamiento, host y dominio sobre la canalización de transporte.  <br/> |
|[Microsoft. Exchange. Data.Transport.Delivery](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.aspx) <br/> |Contiene tipos que admiten la extensión de Exchange de entrega de 2013.  <br/> |
|[Microsoft. Exchange. Data.Transport.Email](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Email.aspx) <br/> |Contiene tipos que admiten la creación, lectura, escritura y modificación de mensajes de correo electrónico.  <br/> |
|[Microsoft. Exchange. Data.Transport.Routing](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.aspx) <br/> |Contiene tipos que admiten la extensión del Exchange de enrutamiento de transporte de 2013.  <br/> |
|[Microsoft. Exchange. Data.Transport.Smtp](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.aspx) <br/> |Contiene tipos que admiten la extensión del comportamiento SMTP Exchange transporte de 2013.  <br/> |
   
## <a name="see-also"></a>Ver también

- [Agentes de transporte en Exchange](transport-agents-in-exchange-2013.md)   
- [Conceptos de agente de transporte Exchange 2013](transport-agent-concepts-in-exchange-2013.md) 
- 
  [Referencia de la API de servidor para Exchange](https://msdn.microsoft.com/library/6eddd052-f59f-45b4-b846-7e53d4d7eb16%28Office.15%29.aspx)
- [Elementos de archivo de configuración de agentes para Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)
    

