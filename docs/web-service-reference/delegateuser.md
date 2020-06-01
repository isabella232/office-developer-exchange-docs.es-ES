---
title: DelegateUser
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegateUser
api_type:
- schema
ms.assetid: aac4e74e-f69b-4c41-a0c9-489610330fbf
description: El elemento DelegateUser identifica un único delegado para agregar o actualizar en un buzón o un delegado devuelto en una respuesta de administración de delegado. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 40d9dacbd544436a3edf3213cf078cd33f961a74
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458806"
---
# <a name="delegateuser"></a>DelegateUser

El elemento **DelegateUser** identifica un único delegado para agregar o actualizar en un buzón o un delegado devuelto en una respuesta de administración de delegado. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<DelegateUser>
   <UserId/>
   <DelegatePermissions/>
   <ReceiveCopiesOfMeetingMessages/>
   <ViewPrivateItems/>
</DelegateUser>
```

**DelegateUserType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UserId](userid.md) <br/> |Identifica el delegado. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[DelegatePermissions](delegatepermissions.md) <br/> |Contiene la configuración del nivel de permisos de delegado. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[ReceiveCopiesOfMeetingMessages](receivecopiesofmeetingmessages.md) <br/> |Indica si un delegado recibe copias de mensajes relacionados con la reunión que se dirigen a la entidad de la identidad. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
|[ViewPrivateItems](viewprivateitems.md) <br/> |Indica si un delegado tiene permiso para ver elementos de calendario privados en el buzón de la entidad de la identidad. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DelegateUsers](delegateusers.md) <br/> |Contiene las identidades de los delegados que se agregan o actualizan en un buzón.  <br/> |
|[DelegateUserResponseMessageType](delegateuserresponsemessagetype.md) <br/> |Contiene mensajes de respuesta para las operaciones de administración de delegado. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación AddDelegate](adddelegate-operation.md) 
- [Operación UpdateDelegate](updatedelegate-operation.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)
- [Adición de delegados](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

