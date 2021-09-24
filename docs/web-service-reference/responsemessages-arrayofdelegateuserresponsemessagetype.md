---
title: ResponseMessages (ArrayOfDelegateUserResponseMessageType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResponseMessages
api_type:
- schema
ms.assetid: 14819975-ce54-4f0e-9f90-d4b275895ea0
description: El elemento ResponseMessages contiene los mensajes de respuesta de una Exchange de administración de delegados de servicios web.
ms.openlocfilehash: aa90d2572679ecf3e5d99cc55731d388e083ff01
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525571"
---
# <a name="responsemessages-arrayofdelegateuserresponsemessagetype"></a>ResponseMessages (ArrayOfDelegateUserResponseMessageType)

El **elemento ResponseMessages** contiene los mensajes de respuesta de una Exchange de administración de delegados de servicios web. 
  
```
<ResponseMessages>
   <DelegateUserResponseMessageType/>
</ResponseMessages>
```

 **ArrayOfDelegateUserResponseMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DelegateUserResponseMessageType](delegateuserresponsemessagetype.md) <br/> |Contiene mensajes de respuesta para operaciones de administración de delegados.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AddDelegateResponse](adddelegateresponse.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación AddDelegate.](adddelegate-operation.md)  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación GetDelegate.](getdelegate-operation.md)  <br/> |
|[UpdateDelegateResponse](updatedelegateresponse.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación UpdateDelegate.](updatedelegate-operation.md)  <br/> |
|[RemoveDelegateResponse](removedelegateresponse.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación RemoveDelegate.](removedelegate-operation.md)  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se usa en la [operación AddDelegate](adddelegate-operation.md), la operación [GetDelegate](getdelegate-operation.md), [la operación UpdateDelegate](updatedelegate-operation.md)y la [operación RemoveDelegate](removedelegate-operation.md). Las respuestas de la operación de administración delegada se estructuran de forma diferente que otras respuestas. Los mensajes de respuesta de administración delegada están fuertemente especificados.
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que se ejecuta Exchange Server con el rol de servidor acceso de cliente instalado.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación AddDelegate](adddelegate-operation.md)
  
[Operación GetDelegate](getdelegate-operation.md)
  
[Operación UpdateDelegate](updatedelegate-operation.md)
  
[Operación RemoveDelegate](removedelegate-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

