---
title: DomainNames (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 79ffc3f9-25c4-40b5-84ce-09a3c5f892fa
description: El elemento DomainNames representa la colección de nombres de dominio. El elemento DomainNames es solo para uso interno. Los clientes no usan este elemento.
ms.openlocfilehash: 0b425b3cd4c0e7cb2427920d61feb04010a3b123
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458421"
---
# <a name="domainnames-soap"></a>DomainNames (SOAP)

El elemento **DomainNames** representa la colección de nombres de dominio. El elemento **DomainNames** es solo para uso interno. Los clientes no usan este elemento. 
  
```XML
<DomainNames>
    <Domains/>
</DomainNames>
```

 **DomainNames**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Dominios (SOAP)](domains-soap.md) <br/> |Representa una colección de dominios que se devuelven desde la [operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md), la [operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)o la [operación GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md).  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Representa una lista de relaciones de organización para una sola organización.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Este elemento representa los dominios SMTP de las organizaciones externas.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

