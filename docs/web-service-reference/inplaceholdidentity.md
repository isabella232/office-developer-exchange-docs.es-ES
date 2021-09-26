---
title: InPlaceHoldIdentity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 54f45774-00a0-4392-af1b-8c5f2208a53f
description: El elemento InPlaceHoldIdentity especifica la identidad de una retención que conserva los elementos del buzón.
ms.openlocfilehash: 0a5f02b908adf49328461c6e3676dab3698879c3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59547214"
---
# <a name="inplaceholdidentity"></a>InPlaceHoldIdentity

El **elemento InPlaceHoldIdentity** especifica la identidad de una retención que conserva los elementos del buzón. 
  
```XML
<InPlaceHoldIdentity></InPlaceHoldIdentity>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[SetHoldOnMailboxes](setholdonmailboxes.md)  |  [DiscoverySearchConfiguration](discoverysearchconfiguration.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento InPlaceHoldIdentity** es el identificador de retención del buzón. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



[Operación SetHoldOnMailboxes](setholdonmailboxes-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

