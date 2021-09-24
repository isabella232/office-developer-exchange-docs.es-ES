---
title: DeliveryReportEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2ab522bc-40ea-4e43-aa57-6d2562db35e9
description: El elemento DeliveryReportEnabled representa la marca DeliveryReportEnabled(). El elemento DeliveryReportEnabled es solo para uso interno. Los clientes no usan este elemento.
ms.openlocfilehash: 95fe62e25ca871171b398b17f3d03dff9235001b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510172"
---
# <a name="deliveryreportenabled-soap"></a>DeliveryReportEnabled (SOAP)

El **elemento DeliveryReportEnabled** representa la **marca DeliveryReportEnabled().** El **elemento DeliveryReportEnabled** es solo para uso interno. Los clientes no usan este elemento. 
  
```XML
<DeliveryReportEnabled>true | false</DeliveryReportEnabled>
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

Un valor de texto de true para el elemento DeliveryReportEnabled indica que se pueden usar los informes de entrega de los usuarios de la organización. Un valor de false indica que los informes de entrega deben suprimirse.
  
## <a name="remarks"></a>Comentarios

Use este elemento para permitir o suprimir informes de entrega del servidor.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

