---
title: Position
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 46726ebb-a403-4793-8378-282aa7dc39d0
description: El elemento Position especifica la posición de una entidad extraída de un mensaje.
ms.openlocfilehash: 6b4e7c12bbcf12b8804619caa508f5c2c0bc4eda
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515295"
---
# <a name="position"></a>Position

El **elemento Position** especifica la posición de una entidad extraída de un mensaje. 
  
```XML
<Position> LatestReply | Other | Subject | Signature </Position>
```

 **EmailPositionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[UrlEntity](urlentity.md)  |  [AddressEntity](addressentity.md)  |  [EmailAddressEntity](emailaddressentity.md)  |  [MeetingSuggestion](meetingsuggestion.md)  |  [Contacto (ContactType)](contact-contacttype.md)  |  [Teléfono (PhoneEntityType)](phone-phoneentitytype.md)  |  [TaskSuggestion](tasksuggestion.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento Position** es la ubicación donde se originó una entidad extraída en el mensaje de origen. Los valores de texto del **elemento Position** son: 
  
- **LatestReply:** la entidad extraída se origina a partir de la respuesta más reciente al mensaje. 
    
- **Other:** la entidad extraída se origina a partir de una parte no definida del mensaje. 
    
- **Asunto:** la entidad extraída se origina en el asunto del mensaje. 
    
- **Firma:** la entidad extraída se origina a partir de la firma del mensaje. 
    
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

