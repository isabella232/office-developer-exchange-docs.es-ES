---
title: SmtpAddress (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 984ccd97-c337-47b6-ba42-3405a8b55a71
description: El elemento SmtpAddress contiene la dirección SMTP asignada a la tienda de mensaje de carpeta pública configurada para el usuario.
ms.openlocfilehash: 43ebb328e31cdec11412e80b743d4d4393b7960a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837507"
---
# <a name="smtpaddress-pox"></a>SmtpAddress (POX)

El elemento **SmtpAddress** contiene la dirección SMTP asignada a la tienda de mensaje de carpeta pública configurada para el usuario. 
  
- [Detección automática (POX)](autodiscover-pox.md)
  
- [Respuesta (POX)](response-pox.md)
  
- [Cuenta (POX)](account-pox.md)
  
- [PublicFolderInformation (POX)](publicfolderinformation-pox.md)
  
- [SmtpAddress (POX)](smtpaddress-pox.md)
  
```XML
<SmtpAddress/>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[PublicFolderInformation (POX)](publicfolderinformation-pox.md) <br/> |Contiene información que los clientes pueden usar para enviar una solicitud de detección automática para detectar información de carpetas públicas para el usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa la dirección SMTP asignada a la tienda de carpeta pública configurada para el usuario. Esta dirección SMTP puede utilizarse en el elemento [EMailAddress (POX)](emailaddress-pox.md) de una solicitud de detección automática para detectar la configuración de carpetas públicas. 
  
## <a name="remarks"></a>Notas

El elemento **SmtpAddress** es un elemento secundario necesario del elemento **PublicFolderInformation** . 
  
## <a name="see-also"></a>Ver también

- [Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

