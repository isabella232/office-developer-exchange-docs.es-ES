---
title: IsUndecidedApprovalRequest
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 90841617-3b83-4124-8125-0293c9470f4a
description: El elemento IsUndecidedApprovalRequest especifica si un mensaje de solicitud de aprobación ha sido actúa en.
ms.openlocfilehash: 82b4624df5b2fe7ca212fdf76248e1ccfa3a081f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836127"
---
# <a name="isundecidedapprovalrequest"></a>IsUndecidedApprovalRequest

El elemento **IsUndecidedApprovalRequest** especifica si un mensaje de solicitud de aprobación ha sido actúa en. 
  
```XML
<IsUndecidedApprovalRequest> true | false </IsUndecidedApprovalRequest>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[ApprovalRequestData](approvalrequestdata.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **IsUndecidedApprovalRequest** es **true** si un mensaje de solicitud de aprobación no ha sido actúa en. Un valor de **false** indica que se haya decidido la solicitud de aprobación. 
  
## <a name="remarks"></a>Notas

Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[ApprovalRequestData](approvalrequestdata.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

