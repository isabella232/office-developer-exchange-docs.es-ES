---
title: MicrosoftOnline (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0b88f02a-9c50-44b3-841b-560b24e37af5
description: El elemento MicrosoftOnline contiene un valor que indica si el buzón del usuario está hospedado en Exchange online o Exchange online como parte de Office 365.
ms.openlocfilehash: f3144a673a4c98aad821e21c562141b0ae00f426
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467987"
---
# <a name="microsoftonline-pox"></a>MicrosoftOnline (POX)

El elemento **MicrosoftOnline** contiene un valor que indica si el buzón del usuario está hospedado en Exchange online o Exchange online como parte de Office 365. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[MicrosoftOnline (POX)](microsoftonline-pox.md)
  
```XML
<MicrosoftOnline/>
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
|[Cuenta (POX)](account-pox.md) <br/> |Especifica la configuración de la cuenta del usuario o contiene respuestas de error.  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de texto indica si el buzón de correo del usuario está hospedado en Exchange Online. El valor es **true** si el buzón del usuario está hospedado en Exchange Online; de lo contrario, **false**.
  
## <a name="see-also"></a>Vea también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

