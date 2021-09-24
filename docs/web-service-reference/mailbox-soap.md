---
title: Mailbox (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 4ad59e5b-4047-4c34-a318-ca06c31d3de8
description: El elemento Mailbox contiene la dirección de correo electrónico del usuario que se va a detectar.
ms.openlocfilehash: 6349a28b7ed97cfaa2bb8ef8f68d93e16d81c377
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514287"
---
# <a name="mailbox-soap"></a>Mailbox (SOAP)

El **elemento Mailbox** contiene la dirección de correo electrónico del usuario que se va a detectar. 
  
```XML
<Mailbox/>
```

**string**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[User (SOAP)](user-soap.md) <br/> |Representa la identidad de un solo usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento Mailbox** es la dirección de correo electrónico del usuario que se va a detectar. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)

