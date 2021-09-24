---
title: DeliverMeetingRequests
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeliverMeetingRequests
api_type:
- schema
ms.assetid: 04b999af-0b27-4e6d-a8b1-400955a1afaa
description: El elemento DeliverMeetingRequests define cómo se controlan las solicitudes de reunión entre el delegado y la entidad de seguridad. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 8e61af87337cb1fc8936b4de7753fca2d6c1161e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519831"
---
# <a name="delivermeetingrequests"></a>DeliverMeetingRequests

El **elemento DeliverMeetingRequests** define cómo se controlan las solicitudes de reunión entre el delegado y la entidad de seguridad. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```XML
<DeliverMeetingRequests>DelegatesOnly or DelegatesAndMe or DelegatesAndSendInformationToMe or NoForward</DeliverMeetingRequests>
```

 **DeliverMeetingRequestsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AddDelegate](adddelegate.md) <br/> |Define una solicitud para agregar delegados a un buzón. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[UpdateDelegate](updatedelegate.md) <br/> |Define una solicitud para actualizar delegados en un buzón. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |Contiene el estado y el resultado de una solicitud GetDelegate. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la tabla siguiente se enumeran los valores **posibles para el elemento DeliverMeetingRequests.** 
  
**Valores del elemento DeliverMeetingRequests**

|**Valor**|**Descripción**|
|:-----|:-----|
|DelegatesOnly  <br/> |Las solicitudes de reunión se reenvían al delegado y se movían a la carpeta Elementos eliminados del buzón de la entidad de seguridad.  <br/> |
|DelegatesAndMe  <br/> |Las solicitudes de reunión se reenvía al delegado y permanecen en la carpeta Bandeja de entrada en el buzón de la entidad de seguridad.  <br/> |
|DelegatesAndSendInformationToMe  <br/> |Las solicitudes de reunión se reenvía al delegado y permanecen en la carpeta Bandeja de entrada del buzón de la entidad de seguridad, pero los botones Aceptar, Provisional y Rechazar no aparecen en el panel de Microsoft Office Outlook lectura.  <br/> |
|NoForward  <br/> |Las solicitudes de reunión no se reenvía al delegado.  <br/> |
   
## <a name="remarks"></a>Comentarios

La **configuración DeliverMeetingRequests** afecta a todos los delegados del buzón de una entidad de seguridad. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación AddDelegate](adddelegate-operation.md)  
- [Operación UpdateDelegate](updatedelegate-operation.md)  
- [Operación GetDelegate](getdelegate-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)
- [Agregar delegados](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

