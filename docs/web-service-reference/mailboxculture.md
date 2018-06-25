---
title: MailboxCulture
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxCulture
api_type:
- schema
ms.assetid: 105cc061-3c35-455f-b102-8023e2055632
description: El elemento MailboxCulture indica la referencia cultural que se utilizará al abrir un buzón de correo. Este elemento se produce en el encabezado SOAP.
ms.openlocfilehash: 9003560a89b83032b4dd1b7ff54f3101819cc3c8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836266"
---
# <a name="mailboxculture"></a>MailboxCulture

El elemento **MailboxCulture** indica la referencia cultural que se utilizará al abrir un buzón de correo. Este elemento se produce en el encabezado SOAP. 
  
```xml
<MailboxCulture/>
```

**MailboxCultureType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

El valor de texto indica el idioma que se usa en las operaciones del servicio Web de Exchange. Los valores posibles para este elemento se describen en RFC 3066.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

