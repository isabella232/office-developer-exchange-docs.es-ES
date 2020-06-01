---
title: IsPermissionControlled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsPermissionControlled
api_type:
- schema
ms.assetid: a2fd0340-f31f-4389-a1cd-7e93b40bb3c6
description: El elemento IsPermissionControlled indica si los mensajes entrantes deben ser controlados por permisos (protegido por RMS) para que se aplique la condición o excepción.
ms.openlocfilehash: 5fba06c1c56512f4a362f773f119ea346a4c0d2b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460389"
---
# <a name="ispermissioncontrolled"></a>IsPermissionControlled

El elemento **IsPermissionControlled** indica si los mensajes entrantes deben ser controlados por permisos (protegido por RMS) para que se aplique la condición o excepción. 
  
```XML
<IsPermissionControlled>true | false</IsPermissionControlled>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Condiciones](conditions.md) <br/> |Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.  <br/> |
|[Excepciones](exceptions.md) <br/> |Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** indica que el mensaje debe estar protegido por RMS para que se aplique la condición o excepción. Un valor de **false** indica que el mensaje no debe estar protegido con RMS para que se aplique la condición o excepción. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

