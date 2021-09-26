---
title: Name (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: dce6d823-dc33-4a47-babe-6370a15ac7b4
description: El elemento Name representa el nombre de una configuración.
ms.openlocfilehash: 39bb2b6bbf7e29dedb13a9bf828f130c076dfb6b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541997"
---
# <a name="name-soap"></a>Name (SOAP)

El **elemento Name** representa el nombre de una configuración. 
  
```XML
<Name/>
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
|[DomainSetting (SOAP)](domainsetting-soap.md) <br/> |Contiene la configuración de dominio que devuelve la [solicitud de operación GetDomainSettings (SOAP).](getdomainsettings-operation-soap.md)  <br/> |
|[DomainStringSetting (SOAP)](domainstringsetting-soap.md) <br/> |Representa un dominio que establece el valor del cual es de tipo string.  <br/> |
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Representa una lista de relaciones de organización para una sola organización.  <br/> |
|[UserSetting (SOAP)](usersetting-soap.md) <br/> |Representa una configuración de usuario único.  <br/> |
|[ProtocolConnectionCollectionSetting (SOAP)](protocolconnectioncollectionsetting-soap.md) <br/> |Representa una colección de opciones de conexión de protocolo de servidor.  <br/> |
|[StringSetting (SOAP)](stringsetting-soap.md) <br/> |Representa un usuario que establece el valor para el que es de tipo string.  <br/> |
|[WebClientUrlCollectionSetting (SOAP)](webclienturlcollectionsetting-soap.md) <br/> |Representa una configuración de usuario que es una colección de direcciones URL Exchange cliente web.  <br/> |
|[AlternateMailboxCollectionSetting (SOAP)](alternatemailboxcollectionsetting-soap.md) <br/> |Contiene una colección de opciones alternativas de buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento Name** es el nombre de una configuración. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)
- [Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
- [Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)
- [Operación GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

