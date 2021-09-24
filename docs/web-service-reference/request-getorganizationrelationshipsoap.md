---
title: Request (GetOrganizationRelationship) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 85dc155c-fad0-4756-b9a8-dedf5040a7c6
description: El elemento Request representa una solicitud GetOrganizationRelationshipSettingsRequest (SOAP). El elemento Request es solo para uso interno. Los clientes no usan este elemento.
ms.openlocfilehash: 06af9ca1067407f7fac9db3ff7c5b4e0fbe8a108
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512372"
---
# <a name="request-getorganizationrelationship-soap"></a>Request (GetOrganizationRelationship) (SOAP)

El **elemento Request** representa una solicitud [GetOrganizationRelationshipSettingsRequest (SOAP).](getorganizationrelationshipsettingsrequest-soap.md) El **elemento Request** es solo para uso interno. Los clientes no usan este elemento. 
  
```XML
<Request>
   <Domains/>
</Request>
```

 **GetOrganizationRelationshipSettingsRequest**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Domains (SOAP)](domains-soap.md) <br/> |Representa los dominios para los que se va a ejecutar detección automática y que se van a usar en una consulta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetOrganizationRelationshipSettingsRequestMessage (SOAP)](getorganizationrelationshipsettingsrequestmessage-soap.md) <br/> |Representa una [solicitud de operación GetOrganizationRelationshipSettings (SOAP).](getorganizationrelationshipsettings-operation-soap.md)  <br/> |
   
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



[GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md)


[Trabajar con detección automática](https://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

