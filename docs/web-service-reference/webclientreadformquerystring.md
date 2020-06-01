---
title: WebClientReadFormQueryString
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WebClientReadFormQueryString
api_type:
- schema
ms.assetid: 13e8871a-32a6-4bb9-9493-864c4c07efff
description: El elemento WebClientReadFormQueryString representa una dirección URL que se concatenará con el punto de conexión de Outlook Web App para leer un elemento en Outlook Web App.
ms.openlocfilehash: d7102ef288c0aafa6cdada09eda321b546edddb7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464983"
---
# <a name="webclientreadformquerystring"></a>WebClientReadFormQueryString

El elemento **WebClientReadFormQueryString** representa una dirección URL que se concatenará con el punto de conexión de Outlook Web App para leer un elemento en Outlook Web App. 
  
```XML
<WebClientReadFormQueryString/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[Contacto](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento en el almacén de Exchange.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el almacén de Exchange.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a una reunión en el almacén de Exchange.  <br/> |
|[Mensaje](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange.  <br/> |
|[PostItem](postitem.md) <br/> |Representa un elemento post en el almacén de Exchange.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Quita un elemento del almacén de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea del almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, se necesita un valor de texto que represente una cadena.
  
## <a name="remarks"></a>Comentarios

El identificador de elemento de una dirección URL de Outlook Web App es el identificador EWS del elemento. Puede codificar en URL el identificador de elemento EWS y anexarlo a la cadena de consulta para obtener la dirección URL de Outlook Web App para un elemento.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
### <a name="version-differences"></a>Diferencias de versión

Las versiones de Exchange que comienzan con la versión principal 15 y terminan con Exchange Server 2013 Build 15.0.775.38 (CU3) y Exchange Online versión 15.00.0775.009 no devuelven un fragmento de cadena de consulta correcto en el elemento **WebClientReadFormQueryString** . 
  
En versiones de Exchange anteriores a la versión principal 15, el identificador de elemento de las direcciones URL de Outlook Web App es un identificador de Outlook Web App. Si el destino es una versión de Exchange anterior a la versión principal 15, tiene que usar la [operación ConvertId](convertid-operation.md) para convertir el identificador. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

