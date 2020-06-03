---
title: ResponseMessages (ArrayOfDelegateUserResponseMessageType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseMessages
api_type:
- schema
ms.assetid: 14819975-ce54-4f0e-9f90-d4b275895ea0
description: El elemento ResponseMessages contiene los mensajes de respuesta para una solicitud de administración de delegado de servicios Web de Exchange.
ms.openlocfilehash: 6b035f4ee46af1750a275e2c61b2cddea06b37a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465460"
---
# <a name="responsemessages-arrayofdelegateuserresponsemessagetype"></a>ResponseMessages (ArrayOfDelegateUserResponseMessageType)

El elemento **ResponseMessages** contiene los mensajes de respuesta para una solicitud de administración de delegado de servicios Web de Exchange. 
  
```
<ResponseMessages>
   <DelegateUserResponseMessageType/>
</ResponseMessages>
```

 **ArrayOfDelegateUserResponseMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DelegateUserResponseMessageType](delegateuserresponsemessagetype.md) <br/> |Contiene mensajes de respuesta para las operaciones de administración de delegado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AddDelegateResponse](adddelegateresponse.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación AddDelegate](adddelegate-operation.md) .  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación GetDelegate](getdelegate-operation.md) .  <br/> |
|[UpdateDelegateResponse](updatedelegateresponse.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación UpdateDelegate](updatedelegate-operation.md) .  <br/> |
|[RemoveDelegateResponse](removedelegateresponse.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación RemoveDelegate](removedelegate-operation.md) .  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se usa en la [operación AddDelegate](adddelegate-operation.md), en la operación [GetDelegate](getdelegate-operation.md), en la [operación UpdateDelegate](updatedelegate-operation.md)y en la [operación RemoveDelegate](removedelegate-operation.md). Las respuestas de la operación de administración de delegado tienen una estructura distinta que otras respuestas. Los mensajes de respuesta de administración de delegado tienen establecimiento inflexible de tipos.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con el rol de servidor acceso de clientes instalado.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación AddDelegate](adddelegate-operation.md)
  
[Operación GetDelegate](getdelegate-operation.md)
  
[Operación UpdateDelegate](updatedelegate-operation.md)
  
[Operación RemoveDelegate](removedelegate-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

