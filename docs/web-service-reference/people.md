---
title: Personas
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 65312428-548c-4fe9-971a-d0dab3be5ddf
description: El elemento People especifica una matriz de datos de persona devueltos como resultado de una solicitud FindPeople.
ms.openlocfilehash: 35af1da4e72829004ec054b27a5304012ebb996c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543152"
---
# <a name="people"></a>Personas

El **elemento People** especifica una matriz de datos de persona devueltos como resultado de una solicitud **FindPeople.** 
  
```XML
<People>
   <Persona/>
</People>
```

**ArrayOfPeopleType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

[Rol](persona.md)
  
### <a name="parent-elements"></a>Elementos principales

[FindPeopleResponse](findpeopleresponse.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

