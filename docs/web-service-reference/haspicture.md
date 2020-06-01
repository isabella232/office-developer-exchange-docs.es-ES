---
title: HasPicture
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HasPicture
api_type:
- schema
ms.assetid: 922a43fe-01bd-49f2-9261-e00e4699b8da
description: El elemento HasPicture indica si el elemento de contacto tiene un archivo adjunto que representa la imagen del contacto.
ms.openlocfilehash: 0f0758e38807587d47b9469f40b10bd9c6ea5012
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462440"
---
# <a name="haspicture"></a>HasPicture

El elemento **HasPicture** indica si el elemento de contacto tiene un archivo adjunto que representa la imagen del contacto. 
  
[Contacto](contact.md)
  
[HasPicture](haspicture.md)
  
```xml
<HasPicture>true or false</HasPicture>
```

 **boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Contacto](contact.md) <br/> |Representa un elemento de contacto en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **HasPicture** puede ser **true** o **false**. El valor predeterminado es **False**.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

