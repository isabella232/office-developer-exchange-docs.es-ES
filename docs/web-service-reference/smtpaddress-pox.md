---
title: SmtpAddress (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 984ccd97-c337-47b6-ba42-3405a8b55a71
description: El elemento SmtpAddress contiene la dirección SMTP asignada al almacén de mensajes de carpeta pública configurado para el usuario.
ms.openlocfilehash: 48703a11fb056967c6c76073c2e928d5f6efa264
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468645"
---
# <a name="smtpaddress-pox"></a>SmtpAddress (POX)

El elemento **SmtpAddress** contiene la dirección SMTP asignada al almacén de mensajes de carpeta pública configurado para el usuario. 
  
- [Detección automática (POX)](autodiscover-pox.md)
  
- [Respuesta (POX)](response-pox.md)
  
- [Cuenta (POX)](account-pox.md)
  
- [PublicFolderInformation (POX)](publicfolderinformation-pox.md)
  
- [SmtpAddress (POX)](smtpaddress-pox.md)
  
```XML
<SmtpAddress/>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PublicFolderInformation (POX)](publicfolderinformation-pox.md) <br/> |Contiene información que los clientes pueden usar para enviar una solicitud de detección automática para detectar la información de las carpetas públicas del usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa la dirección SMTP asignada al almacén de carpetas públicas configurado para el usuario. Esta dirección SMTP puede usarse en el elemento [EmailAddress (POX)](emailaddress-pox.md) de una solicitud de detección automática para detectar la configuración de las carpetas públicas. 
  
## <a name="remarks"></a>Comentarios

El elemento **SmtpAddress** es un elemento secundario necesario del elemento **PublicFolderInformation** . 
  
## <a name="see-also"></a>Vea también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

