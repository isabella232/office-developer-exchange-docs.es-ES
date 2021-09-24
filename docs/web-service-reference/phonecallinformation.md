---
title: PhoneCallInformation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PhoneCallInformation
api_type:
- schema
ms.assetid: a0363c42-6d35-4074-bc17-946eb12736ff
description: El elemento PhoneCallInformation especifica la información de estado de una llamada telefónica.
ms.openlocfilehash: 815e0ffac761b12969483752f5022f8580f6cc62
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528329"
---
# <a name="phonecallinformation"></a>PhoneCallInformation

El **elemento PhoneCallInformation** especifica la información de estado de una llamada telefónica. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PhoneCallState](phonecallstate.md) <br/> |Especifica el estado de una llamada telefónica. Se requiere este elemento.  <br/> |
|[ConnectionFailureCause](connectionfailurecause.md) <br/> |Especifica la causa de un error de conexión. Se requiere este elemento.  <br/> |
|[SIPResponseText](sipresponsetext.md) <br/> |Especifica el texto de respuesta SIP. Este elemento es opcional.  <br/> |
|[SIPResponseCode](sipresponsecode.md) <br/> |Especifica el código de respuesta SIP. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetPhoneCallInformationResponse](getphonecallinformationresponse.md) <br/> |Define una respuesta a una [solicitud de operación GetPhoneCallInformation.](getphonecallinformation-operation.md)  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

