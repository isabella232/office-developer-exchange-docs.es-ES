---
title: SmtpAddress (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 984ccd97-c337-47b6-ba42-3405a8b55a71
description: El elemento SmtpAddress contiene la dirección SMTP asignada al almacén de mensajes de carpetas públicas configurado para el usuario.
ms.openlocfilehash: d257b193a3254afceaa72d396a8c2724bb3165c6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546990"
---
# <a name="smtpaddress-pox"></a>SmtpAddress (POX)

El **elemento SmtpAddress** contiene la dirección SMTP asignada al almacén de mensajes de carpetas públicas configurado para el usuario. 
  
- [AutoDiscover (POX)](autodiscover-pox.md)
  
- [Response (POX)](response-pox.md)
  
- [Account (POX)](account-pox.md)
  
- [PublicFolderInformation (POX)](publicfolderinformation-pox.md)
  
- [SmtpAddress (POX)](smtpaddress-pox.md)
  
```XML
<SmtpAddress/>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PublicFolderInformation (POX)](publicfolderinformation-pox.md) <br/> |Contiene información que los clientes pueden usar para enviar una solicitud de detección automática para detectar información de carpetas públicas para el usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa la dirección SMTP asignada al almacén de carpetas públicas configurado para el usuario. Esta dirección SMTP se puede usar en el elemento [EMailAddress (POX)](emailaddress-pox.md) de una solicitud de detección automática para detectar la configuración de carpetas públicas. 
  
## <a name="remarks"></a>Comentarios

El **elemento SmtpAddress** es un elemento secundario necesario del **elemento PublicFolderInformation.** 
  
## <a name="see-also"></a>Consulte también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

