---
title: UpdateDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateDelegate
api_type:
- schema
ms.assetid: c6ae99c4-18b0-4136-90ab-12cf15e15f91
description: El elemento UpdateDelegate define una solicitud para actualizar los delegados en un buzón de correo. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 32322e48acfa5f1058786162565a185a3e565d6e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840806"
---
# <a name="updatedelegate"></a>UpdateDelegate

El elemento **UpdateDelegate** define una solicitud para actualizar los delegados en un buzón de correo. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<UpdateDelegate>
      <DelegateUsers/>
   <DeliverMeetingRequests/>
      <Mailbox/>
</UpdateDelegate>
```

 **UpdateDelegateType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[DelegateUsers](delegateusers.md) <br/> |Contiene una matriz de elementos de [UsuarioDelegado](delegateuser.md) que identifican los delegados y las actualizaciones se pueden aplicar a los delegados. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[DeliverMeetingRequests](delivermeetingrequests.md) <br/> |Define cómo se controlan las convocatorias de reunión entre el delegado y la entidad de seguridad. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[Buzón de correo](mailbox.md) <br/> |Identifica un objeto de servicio de directorio de Active Directory habilitados para correo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación UpdateDelegate](updatedelegate-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

