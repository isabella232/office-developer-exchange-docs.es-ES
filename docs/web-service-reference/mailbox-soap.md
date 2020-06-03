---
title: Buzón de correo (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 4ad59e5b-4047-4c34-a318-ca06c31d3de8
description: El elemento Mailbox contiene la dirección de correo electrónico del usuario que se va a detectar.
ms.openlocfilehash: e050cd9d3ca4a2d2450f315f1eedd3862328d096
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467287"
---
# <a name="mailbox-soap"></a>Buzón de correo (SOAP)

El elemento **Mailbox** contiene la dirección de correo electrónico del usuario que se va a detectar. 
  
```XML
<Mailbox/>
```

**string**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Usuario (SOAP)](user-soap.md) <br/> |Representa la identidad de un único usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **Mailbox** es la dirección de correo electrónico del usuario que se va a detectar. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)

