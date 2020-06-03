---
title: CallState (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- CallState
api_type:
- schema
ms.assetid: 88670707-12f7-41c5-ac81-dda0c354a2cb
description: El elemento CallState contiene un valor que indica el estado de una llamada.
ms.openlocfilehash: 44614c460286ff49ebc2373263c1827c6be5cc08
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44454613"
---
# <a name="callstate-um-web-service"></a>CallState (servicio Web de mensajería unificada)

El elemento **CallState** contiene un valor que indica el estado de una llamada. 
  
[GetCallInfoResponse (servicio Web de mensajería unificada)](getcallinforesponse-um-web-service.md)
  
[CallState (servicio Web de mensajería unificada)](callstate-um-web-service.md)
  
```xml
<CallState/>
```

 **UMCallState**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetCallInfoResponse (servicio Web de mensajería unificada)](getcallinforesponse-um-web-service.md) <br/> |Define una respuesta a una [operación de GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-operation-um-web-service.md).  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. Los valores posibles son los siguientes:
  
- Usado
    
- Conectando
    
- Alertas
    
- Conectado
    
- Desconectado
    
- Entra
    
- Transferencia
    
- Reenvío
    
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetCallInfo (servicio Web de mensajería unificada)](getcallinfo-operation-um-web-service.md)
  
[GetCallInfoResponse (servicio Web de mensajería unificada)](getcallinforesponse-um-web-service.md)

