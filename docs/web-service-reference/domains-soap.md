---
title: Dominios (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5f81d1b7-c6a4-456f-9935-13d04a3d92d7
description: El elemento de dominios representa la colección de dominio que se devuelve en una operación de GetDomainSettings (SOAP), los dominios que la organización ha federados en una operación de GetFederationInformation (SOAP) o los dominios con una relación de organización como devuelto por la operación de GetOrganizationRelationshipSettings (SOAP).
ms.openlocfilehash: 7a21a3a09516de2d1c38021ca3ccd2161d9cdd1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764272"
---
# <a name="domains-soap"></a>Dominios (SOAP)

El elemento de **dominios** representa la colección de dominio que se devuelve en una [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md), los dominios que la organización ha federados en una [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)o los dominios con una relación de la organización como devuelto por la [operación de GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md).
  
```XML
<Domains>
   <Domain/>
</Domains>
```

 **Dominios**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Dominio (SOAP)](domain-soap.md) <br/> |Representa un solo dominio.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md) <br/> |Representa una solicitud de [operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) .  <br/> |
|[Respuesta (GetFederationInformation) (SOAP)](response-getfederationinformationsoap.md) <br/> |Contiene la información de respuesta de la [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .  <br/> |
|[GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) <br/> |Representa una solicitud de [operación GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md) .  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también

- [GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md)  
- [GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md)

