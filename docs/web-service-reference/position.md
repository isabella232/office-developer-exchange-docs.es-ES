---
title: Position
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46726ebb-a403-4793-8378-282aa7dc39d0
description: El elemento Position especifica la posición de una entidad extraída de un mensaje.
ms.openlocfilehash: 9acd965c3e0c29f3fa91df338c0671749192b38b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465425"
---
# <a name="position"></a>Position

El elemento **Position** especifica la posición de una entidad extraída de un mensaje. 
  
```XML
<Position> LatestReply | Other | Subject | Signature </Position>
```

 **EmailPositionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[UrlEntity](urlentity.md)  |  [AddressEntity](addressentity.md)  |  [EmailAddressEntity](emailaddressentity.md)  |  [MeetingSuggestion](meetingsuggestion.md)  |  [Contacto (ContactType)](contact-contacttype.md)  |  [Teléfono (PhoneEntityType)](phone-phoneentitytype.md)  |  [TaskSuggestion](tasksuggestion.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **Position** es la ubicación en la que se originó una entidad extraída en el mensaje de origen. Los valores de texto para el elemento **Position** son: 
  
- **LatestReply** : la entidad extraída se origina desde la última respuesta al mensaje. 
    
- **Otro** : la entidad extraída se origina a partir de una parte indefinida del mensaje. 
    
- **Asunto** : la entidad extraída se origina desde el asunto del mensaje. 
    
- **Signature** : la entidad extraída se origina desde la firma del mensaje. 
    
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   

