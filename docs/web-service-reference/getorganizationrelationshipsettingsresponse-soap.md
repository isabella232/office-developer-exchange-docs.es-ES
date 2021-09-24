---
title: GetOrganizationRelationshipSettingsResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2f43b817-92c2-4e04-8095-479d790f768c
description: El elemento GetOrganizationRelationshipSettingsResponse contiene la respuesta de la operación GetOrganizationRelationshipSettings (SOAP). El elemento GetOrganizationRelationshipSettingsResponse es solo para uso interno. Los clientes no usan este elemento.
ms.openlocfilehash: e62496b70c89477fa87a50de256aa8a6b37f3111
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524248"
---
# <a name="getorganizationrelationshipsettingsresponse-soap"></a>GetOrganizationRelationshipSettingsResponse (SOAP)

El **elemento GetOrganizationRelationshipSettingsResponse** contiene la respuesta de la operación [GetOrganizationRelationshipSettings (SOAP).](getorganizationrelationshipsettings-operation-soap.md) El **elemento GetOrganizationRelationshipSettingsResponse** es solo para uso interno. Los clientes no usan este elemento. 
  
```XML
<GetOrganizationRelationshipSettingResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <OrganizationRelationshipSettingsCollection/>
</GetOrganizationRelationshipSettingResponse>
```

 **GetOrganizationRelationshipSettingsResponse**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Representa un código de error devuelto por el servicio de detección automática.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Representa un mensaje asociado a un código de error devuelto por el servicio de detección automática.  <br/> |
|[OrganizationRelationshipSettingsCollection (SOAP)](organizationrelationshipsettingscollection-soap.md) <br/> |Representa una colección de relaciones de organización que coinciden con la consulta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
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



[Operación GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

