---
title: MicrosoftOnline (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0b88f02a-9c50-44b3-841b-560b24e37af5
description: El elemento MicrosoftOnline contiene un valor que indica si el buzón del usuario está hospedado en Exchange Online o Exchange Online como parte de Office 365.
ms.openlocfilehash: fbf230df18ca488babb1523cc7f689923eaeb55b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510949"
---
# <a name="microsoftonline-pox"></a>MicrosoftOnline (POX)

El **elemento MicrosoftOnline** contiene un valor que indica si el buzón del usuario está hospedado en Exchange Online o Exchange Online como parte de Office 365. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[MicrosoftOnline (POX)](microsoftonline-pox.md)
  
```XML
<MicrosoftOnline/>
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
|[Account (POX)](account-pox.md) <br/> |Especifica la configuración de la cuenta para el usuario o contiene respuestas de error.  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de texto indica si el buzón del usuario está hospedado en Exchange Online. El valor es **true** si el buzón del usuario está hospedado en Exchange Online; de lo contrario, **false**.
  
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

