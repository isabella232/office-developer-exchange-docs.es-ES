---
title: PhoneCallInformation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhoneCallInformation
api_type:
- schema
ms.assetid: a0363c42-6d35-4074-bc17-946eb12736ff
description: El elemento PhoneCallInformation especifica la información de estado para una llamada de teléfono.
ms.openlocfilehash: e64e7b38b3801c60df8a966e95d980746533d3a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836758"
---
# <a name="phonecallinformation"></a>PhoneCallInformation

El elemento **PhoneCallInformation** especifica la información de estado para una llamada de teléfono. 
  
```XML
<PhoneCallInformation>
   <PhoneCallState/>
   <ConnectionFailureCause/>
   <SIPResponseText/>
   <SIPResponseCode/>
</PhoneCallInformation>
```

 **PhoneCallInformationType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[PhoneCallState](phonecallstate.md) <br/> |Especifica el estado de una llamada telefónica. Se requiere este elemento.  <br/> |
|[ConnectionFailureCause](connectionfailurecause.md) <br/> |Especifica la causa de un error de conexión. Se requiere este elemento.  <br/> |
|[SIPResponseText](sipresponsetext.md) <br/> |Especifica el texto de respuesta SIP. Este elemento es opcional.  <br/> |
|[SIPResponseCode](sipresponsecode.md) <br/> |Especifica el código de respuesta SIP. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetPhoneCallInformationResponse](getphonecallinformationresponse.md) <br/> |Define una respuesta a una solicitud de [operación GetPhoneCallInformation](getphonecallinformation-operation.md) .  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

