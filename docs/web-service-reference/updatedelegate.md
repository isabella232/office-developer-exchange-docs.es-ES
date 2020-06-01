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
description: El elemento UpdateDelegate define una solicitud para actualizar delegados en un buzón. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 17d69eb8c539217d39e1dd0c2616261d02ad304d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468876"
---
# <a name="updatedelegate"></a>UpdateDelegate

El elemento **UpdateDelegate** define una solicitud para actualizar delegados en un buzón. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<UpdateDelegate>
      <DelegateUsers/>
   <DeliverMeetingRequests/>
      <Mailbox/>
</UpdateDelegate>
```

 **UpdateDelegateType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DelegateUsers](delegateusers.md) <br/> |Contiene una matriz de elementos [DelegateUser](delegateuser.md) que identifican los delegados y las actualizaciones que se van a aplicar a los delegados. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[DeliverMeetingRequests](delivermeetingrequests.md) <br/> |Define cómo se administran las convocatorias de reunión entre el delegado y la entidad de la identidad. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[Buzón](mailbox.md) <br/> |Identifica un objeto de servicio de directorio de Active Directory habilitado para correo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación UpdateDelegate](updatedelegate-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

