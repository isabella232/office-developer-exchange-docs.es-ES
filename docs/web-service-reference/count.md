---
title: Recuento
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Count
api_type:
- schema
ms.assetid: 68314b4a-1e17-4e21-9c2e-224d70ef7a32
description: El elemento Count contiene el número de conflictos en una respuesta de operación UpdateItem.
ms.openlocfilehash: 0504b0517e3337e0b985a8755a907ca460f90ccf
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511891"
---
# <a name="count"></a>Recuento

El [elemento Count](count.md) contiene el número de conflictos en una respuesta de operación [UpdateItem.](updateitem-operation.md) 
  
[UpdateItemResponse](updateitemresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[UpdateItemResponseMessage](updateitemresponsemessage.md)
  
[ConflictResults](conflictresults.md)
  
[Count](count.md)
  
```xml
<Count/>
```

 **int**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ConflictResults](conflictresults.md) <br/> |Contiene el número de conflictos en una [respuesta de operación UpdateItem.](updateitem-operation.md)  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto es un entero que representa el número de conflictos en una [respuesta de operación UpdateItem.](updateitem-operation.md) 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación UpdateItem](updateitem-operation.md)
  
 **ConflictResultsType**

