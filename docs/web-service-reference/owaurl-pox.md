---
title: OWAUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 450b86a1-1722-49f5-b541-16c1edc3db7a
description: El elemento OWAUrl describe la dirección URL y el esquema de autenticación que se usa para tener acceso a un determinado equipo que ejecuta Microsoft Exchange Server 2007 que tiene el rol de servidor de acceso de cliente instalado que aloja Outlook Web Access.
ms.openlocfilehash: 93d03506e2a74aa1b4ef6d2a49ccbda01cfc1f9a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836673"
---
# <a name="owaurl-pox"></a>OWAUrl (POX)

El elemento **OWAUrl** describe la dirección URL y el esquema de autenticación que se usa para tener acceso a un determinado equipo que ejecuta Microsoft Exchange Server 2007 que tiene el rol de servidor de acceso de cliente instalado que aloja Outlook Web Access. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[Interno (POX)](internal-pox.md)
  
[OWAUrl (POX)](owaurl-pox.md)
  
```xml
<OWAUrl AuthenticationMethod=""/>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**AuthenticationMethod** <br/> |Describe los métodos de autenticación para obtener acceso a Outlook Web Access.  <br/> |
   
#### <a name="authenticationmethod-attribute"></a>Atributo AuthenticationMethod

|**Valor**|**Descripción**|
|:-----|:-----|
|WindowsIntegrated  <br/> |Autenticación integrada de Windows.  <br/> |
|FBA  <br/> |Autenticación basada en formularios.  <br/> |
|NTLM  <br/> |Autenticación NTLM.  <br/> |
|Implícita  <br/> |Autenticación implícita.  <br/> |
|Básica  <br/> |Autenticación básica.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Interno (POX)](internal-pox.md) <br/> |Contiene la colección de direcciones URL de Outlook Web Access que un cliente puede conectarse a cuando está dentro del firewall.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa la dirección URL del servicio de Outlook Web Access en un servidor de acceso de cliente.
  
## <a name="see-also"></a>Ver también



[Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

