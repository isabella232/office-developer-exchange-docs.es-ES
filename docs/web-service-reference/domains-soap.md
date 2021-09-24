---
title: Domains (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 5f81d1b7-c6a4-456f-9935-13d04a3d92d7
description: El elemento Domains representa la colección de dominios que se devuelve en una operación GetDomainSettings (SOAP), los dominios que la organización ha federado en una operación GetFederationInformation (SOAP) o los dominios con una relación de organización devueltos por la operación GetOrganizationRelationshipSettings (SOAP).
ms.openlocfilehash: 667b2611ce8b393252f9bdda6dd7ec201b605047
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538327"
---
# <a name="domains-soap"></a>Domains (SOAP)

El **elemento Domains** representa la colección de dominios que se devuelve en una operación [GetDomainSettings (SOAP),](getdomainsettings-operation-soap.md)los dominios que la organización ha federado en una operación [GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)o los dominios con una relación de organización devueltos por la operación [GetOrganizationRelationshipSettings (SOAP).](getorganizationrelationshipsettings-operation-soap.md)
  
```XML
<Domains>
   <Domain/>
</Domains>
```

 **Dominios**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Domain (SOAP)](domain-soap.md) <br/> |Representa un solo dominio.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md) <br/> |Representa una [solicitud de operación GetDomainSettings (SOAP).](getdomainsettings-operation-soap.md)  <br/> |
|[Response (GetFederationInformation) (SOAP)](response-getfederationinformationsoap.md) <br/> |Contiene la [información de respuesta de la operación GetFederationInformation (SOAP).](getfederationinformation-operation-soap.md)  <br/> |
|[GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) <br/> |Representa una [solicitud de operación GetOrganizationRelationshipSettings (SOAP).](getorganizationrelationshipsettings-operation-soap.md)  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también

- [GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md)  
- [GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md)

