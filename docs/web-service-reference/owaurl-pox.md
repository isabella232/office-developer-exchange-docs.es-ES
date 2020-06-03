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
description: El elemento OWAUrl describe la dirección URL y el esquema de autenticación que se usa para obtener acceso a un equipo concreto que ejecuta Microsoft Exchange Server 2007 que tiene instalada la función de servidor acceso de clientes que hospeda Outlook Web Access.
ms.openlocfilehash: c0728af063cfbf1353eb7d3b81f5fcfe8b398f7d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457266"
---
# <a name="owaurl-pox"></a>OWAUrl (POX)

El elemento **OWAUrl** describe la dirección URL y el esquema de autenticación que se usa para obtener acceso a un equipo concreto que ejecuta Microsoft Exchange Server 2007 que tiene instalada la función de servidor acceso de clientes que hospeda Outlook Web Access. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**AuthenticationMethod** <br/> |Describe los métodos de autenticación para obtener acceso a Outlook Web Access.  <br/> |
   
#### <a name="authenticationmethod-attribute"></a>Atributo AuthenticationMethod

|**Valor**|**Descripción**|
|:-----|:-----|
|WindowsIntegrated  <br/> |Autenticación de Windows integrada.  <br/> |
|FBA  <br/> |Autenticación basada en formularios.  <br/> |
|NTLM  <br/> |Autenticación NTLM.  <br/> |
|Digest  <br/> |Autenticación implícita.  <br/> |
|Básica  <br/> |Autenticación básica.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Interno (POX)](internal-pox.md) <br/> |Contiene la colección de direcciones URL de Outlook Web Access a las que se puede conectar un cliente cuando está dentro del firewall.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa la dirección URL del servicio de Outlook Web Access en un servidor de acceso de cliente.
  
## <a name="see-also"></a>Vea también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

