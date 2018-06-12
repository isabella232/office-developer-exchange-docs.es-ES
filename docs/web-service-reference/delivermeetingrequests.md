---
title: DeliverMeetingRequests
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeliverMeetingRequests
api_type:
- schema
ms.assetid: 04b999af-0b27-4e6d-a8b1-400955a1afaa
description: El elemento DeliverMeetingRequests define cómo se controlan las convocatorias de reunión entre el delegado y la entidad de seguridad. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 803bd2da72bdb21b507a59cc11635a40d4431acf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764121"
---
# <a name="delivermeetingrequests"></a>DeliverMeetingRequests

El elemento **DeliverMeetingRequests** define cómo se controlan las convocatorias de reunión entre el delegado y la entidad de seguridad. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```XML
<DeliverMeetingRequests>DelegatesOnly or DelegatesAndMe or DelegatesAndSendInformationToMe or NoForward</DeliverMeetingRequests>
```

 **DeliverMeetingRequestsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[AddDelegate](adddelegate.md) <br/> |Define una solicitud para agregar delegados a un buzón de correo. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[UpdateDelegate](updatedelegate.md) <br/> |Define una solicitud para actualizar los delegados en un buzón de correo. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |Contiene el estado y el resultado de una solicitud de GetDelegate. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumera los valores posibles para el elemento **DeliverMeetingRequests** . 
  
**Valores de elemento DeliverMeetingRequests**

|**Valor**|**Descripción**|
|:-----|:-----|
|DelegatesOnly  <br/> |Las convocatorias de reunión se transfieren al delegado y movidas a la carpeta Elementos eliminados en el buzón de la entidad de seguridad.  <br/> |
|DelegatesAndMe  <br/> |Las convocatorias de reunión se transfieren al delegado y permanecerán en la carpeta Bandeja de entrada en el buzón de la entidad de seguridad.  <br/> |
|DelegatesAndSendInformationToMe  <br/> |Las convocatorias de reunión se transfieren al delegado y permanecerán en la carpeta Bandeja de entrada en el buzón de la entidad de seguridad, pero los botones Aceptar, provisional y rechazar no aparecen en el panel de lectura de Microsoft Office Outlook.  <br/> |
|NoForward  <br/> |Las convocatorias de reunión no se transfieren al delegado.  <br/> |
   
## <a name="remarks"></a>Notas

La configuración de **DeliverMeetingRequests** afecta a todos los delegados en el buzón de correo de una entidad de seguridad. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación AddDelegate](adddelegate-operation.md)  
- [Operación UpdateDelegate](updatedelegate-operation.md)  
- [Operación GetDelegate](getdelegate-operation.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)
- [Adición de delegados](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

