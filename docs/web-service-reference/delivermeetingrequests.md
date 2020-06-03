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
description: El elemento DeliverMeetingRequests define cómo se administran las convocatorias de reunión entre el delegado y la entidad de la identidad. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 3998443613437bca2267678f7bc2c5584b779135
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463681"
---
# <a name="delivermeetingrequests"></a>DeliverMeetingRequests

El elemento **DeliverMeetingRequests** define cómo se administran las convocatorias de reunión entre el delegado y la entidad de la identidad. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```XML
<DeliverMeetingRequests>DelegatesOnly or DelegatesAndMe or DelegatesAndSendInformationToMe or NoForward</DeliverMeetingRequests>
```

 **DeliverMeetingRequestsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AddDelegate](adddelegate.md) <br/> |Define una solicitud para agregar delegados a un buzón. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[UpdateDelegate](updatedelegate.md) <br/> |Define una solicitud para actualizar delegados en un buzón. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |Contiene el estado y el resultado de una solicitud GetDelegate. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumeran los valores posibles para el elemento **DeliverMeetingRequests** . 
  
**Valores del elemento DeliverMeetingRequests**

|**Valor**|**Descripción**|
|:-----|:-----|
|DelegatesOnly  <br/> |Las convocatorias de reunión se reenvían al delegado y se mueven a la carpeta elementos eliminados en el buzón de la entidad de la identidad.  <br/> |
|DelegatesAndMe  <br/> |Las convocatorias de reunión se reenvían al delegado y permanecen en la carpeta Bandeja de entrada en el buzón de la entidad.  <br/> |
|DelegatesAndSendInformationToMe  <br/> |Las convocatorias de reunión se reenvían al delegado y permanecen en la carpeta Bandeja de entrada en el buzón de correo de la entidad de la identidad, pero los botones aceptar, provisional y rechazar no aparecen en el panel de lectura de Microsoft Office Outlook.  <br/> |
|No reenviar  <br/> |Las convocatorias de reunión no se reenvían al delegado.  <br/> |
   
## <a name="remarks"></a>Comentarios

La configuración **DeliverMeetingRequests** afecta a todos los delegados del buzón de una entidad de identidad. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación AddDelegate](adddelegate-operation.md)  
- [Operación UpdateDelegate](updatedelegate-operation.md)  
- [Operación GetDelegate](getdelegate-operation.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)
- [Adición de delegados](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

