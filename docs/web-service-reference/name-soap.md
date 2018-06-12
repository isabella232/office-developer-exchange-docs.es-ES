---
title: Nombre (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: dce6d823-dc33-4a47-babe-6370a15ac7b4
description: El elemento Name representa el nombre de una opción de configuración.
ms.openlocfilehash: 4689c306bb805a40fea0d58c9e04a5a47d3bb14d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836506"
---
# <a name="name-soap"></a>Nombre (SOAP)

El elemento **Name** representa el nombre de una opción de configuración. 
  
```XML
<Name/>
```

**string**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[DomainSetting (SOAP)](domainsetting-soap.md) <br/> |Contiene la configuración de dominio que es devueltos por la solicitud de la [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) .  <br/> |
|[DomainStringSetting (SOAP)](domainstringsetting-soap.md) <br/> |Representa una configuración de dominio, el valor de los cuales es de tipo string.  <br/> |
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Representa una lista de relaciones de organización para una sola organización.  <br/> |
|[UserSetting (SOAP)](usersetting-soap.md) <br/> |Representa una configuración de usuario único.  <br/> |
|[ProtocolConnectionCollectionSetting (SOAP)](protocolconnectioncollectionsetting-soap.md) <br/> |Representa una colección de configuración de conexión del protocolo de servidor.  <br/> |
|[StringSetting (SOAP)](stringsetting-soap.md) <br/> |Representa una configuración de usuario, el valor para el que es de tipo string.  <br/> |
|[WebClientUrlCollectionSetting (SOAP)](webclienturlcollectionsetting-soap.md) <br/> |Representa un usuario de configuración, es decir, una colección de direcciones URL de cliente Web de Exchange.  <br/> |
|[AlternateMailboxCollectionSetting (SOAP)](alternatemailboxcollectionsetting-soap.md) <br/> |Contiene una colección de configuración de buzón de correo alternativas.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **Name** es el nombre de una opción de configuración. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)
- [Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
- [Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)
- [Operación GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

