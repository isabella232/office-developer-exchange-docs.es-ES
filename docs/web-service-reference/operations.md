---
title: Operaciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Operations
api_type:
- schema
ms.assetid: d8cd41b1-28ae-4c95-9ff6-8b25c8e18306
description: El elemento Operations contiene una matriz de operaciones de regla que se pueden realizar en una Bandeja de entrada.
ms.openlocfilehash: 48679c9c7c0482ab53d3af5c661dc6efe513e637
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518074"
---
# <a name="operations"></a>Operaciones

El **elemento Operations** contiene una matriz de operaciones de regla que se pueden realizar en una Bandeja de entrada. 
  
[UpdateInboxRules](updateinboxrules.md)
  
```XML
<Operations>
    <CreateRuleOperation/>
    <SetRuleOperation/>
    <DeleteRuleOperation/>
</Operations>
```

 **ArrayOfRuleOperationsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CreateRuleOperation](createruleoperation.md) <br/> |Representa una operación para crear una nueva regla de bandeja de entrada.  <br/> |
|[SetRuleOperation](setruleoperation.md) <br/> |Representa una operación para actualizar una regla de bandeja de entrada.  <br/> |
|[DeleteRuleOperation](deleteruleoperation.md) <br/> |Representa una operación para eliminar una regla de bandeja de entrada.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UpdateInboxRules](updateinboxrules.md) <br/> |Define una solicitud para actualizar las reglas de la Bandeja de entrada en un buzón en el almacén del servidor.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación de UpdateInboxRules](updateinboxrules-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

