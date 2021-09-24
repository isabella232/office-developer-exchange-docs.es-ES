---
title: FreeBusyAccessEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 8d2d3276-b180-424e-a707-7256d14a1776
description: El elemento FreeBusyAccessEnabled representa la marca FreeBusyAccessEnabled(). El elemento FreeBusyAccessEnabled es solo para uso interno. Los clientes no usan este elemento.
ms.openlocfilehash: faf51798ba211b4219a3f2abee3b3e5e9ce4ab29
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530223"
---
# <a name="freebusyaccessenabled-soap"></a>FreeBusyAccessEnabled (SOAP)

El **elemento FreeBusyAccessEnabled** representa la **marca FreeBusyAccessEnabled().** El **elemento FreeBusyAccessEnabled** es solo para uso interno. Los clientes no usan este elemento. 
  
```XML
<FreeBusyAccessEnabled>true | false</FreeBusyAccessEnabled>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |Representa una lista de relaciones de organización para una sola organización.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento FreeBusyAccessEnabled** indica que la relación de uso compartido debe usarse para recuperar información de disponibilidad de los usuarios de la organización. Un valor de **false** indica que se debe suprimir la relación de uso compartido. 
  
## <a name="remarks"></a>Comentarios

Use este elemento para permitir o suprimir la información de disponibilidad del servidor. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

