---
title: Operaciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Operations
api_type:
- schema
ms.assetid: d8cd41b1-28ae-4c95-9ff6-8b25c8e18306
description: El elemento de operaciones contiene una matriz de las operaciones de la regla que se puede realizar en una bandeja de entrada.
ms.openlocfilehash: 1030703d5e496be391d557e99e1420f9fddfdb36
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836655"
---
# <a name="operations"></a>Operaciones

El elemento de **operaciones** contiene una matriz de las operaciones de la regla que se puede realizar en una bandeja de entrada. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[CreateRuleOperation](createruleoperation.md) <br/> |Representa una operación para crear una nueva regla de bandeja de entrada.  <br/> |
|[SetRuleOperation](setruleoperation.md) <br/> |Representa una operación para actualizar una regla de bandeja de entrada.  <br/> |
|[DeleteRuleOperation](deleteruleoperation.md) <br/> |Representa una operación para eliminar una regla de bandeja de entrada.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[UpdateInboxRules](updateinboxrules.md) <br/> |Define una solicitud para actualizar las reglas de bandeja de entrada en un buzón en el almacén del servidor.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación de UpdateInboxRules](updateinboxrules-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

