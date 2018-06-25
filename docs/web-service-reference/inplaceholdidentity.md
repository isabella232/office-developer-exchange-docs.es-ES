---
title: InPlaceHoldIdentity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54f45774-00a0-4392-af1b-8c5f2208a53f
description: El elemento InPlaceHoldIdentity especifica la identidad de una suspensión que conserva los elementos del buzón de correo.
ms.openlocfilehash: 954e6ad6c3e0b7786d6bbb8230dba913a32359bc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835938"
---
# <a name="inplaceholdidentity"></a>InPlaceHoldIdentity

El elemento **InPlaceHoldIdentity** especifica la identidad de una suspensión que conserva los elementos del buzón de correo. 
  
```XML
<InPlaceHoldIdentity></InPlaceHoldIdentity>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[SetHoldOnMailboxes](setholdonmailboxes.md) | [DiscoverySearchConfiguration](discoverysearchconfiguration.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **InPlaceHoldIdentity** es el identificador de espera de buzón de correo. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación SetHoldOnMailboxes](setholdonmailboxes-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

