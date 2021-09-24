---
title: OWAUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 450b86a1-1722-49f5-b541-16c1edc3db7a
description: El elemento OWAUrl describe la dirección URL y el esquema de autenticación que se usa para obtener acceso a un equipo determinado que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente que hospeda Outlook Web Access.
ms.openlocfilehash: fbd61eb75018c57dada40f5ed7472379d365e752
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59534894"
---
# <a name="owaurl-pox"></a>OWAUrl (POX)

El **elemento OWAUrl** describe la dirección URL y el esquema de autenticación que se usa para tener acceso a un equipo determinado que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente que hospeda Outlook Web Access. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[Internal (POX)](internal-pox.md)
  
[OWAUrl (POX)](owaurl-pox.md)
  
```xml
<OWAUrl AuthenticationMethod=""/>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**AuthenticationMethod** <br/> |Describe los métodos de autenticación para obtener acceso Outlook Web Access.  <br/> |
   
#### <a name="authenticationmethod-attribute"></a>Atributo AuthenticationMethod

|**Valor**|**Descripción**|
|:-----|:-----|
|WindowsIntegrated  <br/> |Autenticación Windows integrada.  <br/> |
|FBA  <br/> |Autenticación basada en formularios.  <br/> |
|NTLM  <br/> |Autenticación NTLM.  <br/> |
|Digest  <br/> |Autenticación implícita.  <br/> |
|Básico  <br/> |Autenticación básica.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Internal (POX)](internal-pox.md) <br/> |Contiene la colección de Outlook direcciones URL de Web Access a las que un cliente puede conectarse cuando está dentro del firewall.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa la dirección URL del Outlook de acceso web en un servidor de acceso de cliente.
  
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

