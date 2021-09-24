---
title: RequestedVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 962036c9-9b13-4669-bed2-2502c0f5aabe
description: El elemento RequestedVersion especifica la versión de servicio mínima en la que el cliente desea que se procese la solicitud.
ms.openlocfilehash: 390dee362bf2e6c2bdeac4e0e5564ecbd59b7319
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513335"
---
# <a name="requestedversion-soap"></a>RequestedVersion (SOAP)

El **elemento RequestedVersion** especifica la versión de servicio mínima en la que el cliente desea que se procese la solicitud. 
  
```XML
<RequestedVersion/>
```

 **ExchangeVersion**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Request (SOAP)](request-soap.md) <br/> |Contiene las opciones de configuración solicitadas y los usuarios de destino.  <br/> |
|[Request (GetDomainSettings) (SOAP)](request-getdomainsettingssoap.md) <br/> |Representa una solicitud para obtener la configuración del dominio.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento RequestedVersion** puede ser Exchange2010, Exchange2010_SP1, Exchange2010_SP2 o Exchange2013.
  
## <a name="remarks"></a>Comentarios

Si este elemento no está presente, se usa la versión del servicio más reciente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
  
[Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)

