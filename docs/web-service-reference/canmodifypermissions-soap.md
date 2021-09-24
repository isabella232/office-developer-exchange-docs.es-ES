---
title: CanModifyPermissions (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9693de1a-0c76-4898-8f4d-a8693fb005b3
description: El elemento CanModifyPermissions indica si un usuario puede modificar los permisos de acceso a una ubicación de uso compartido de documentos.
ms.openlocfilehash: 5aa11ff62fc5c82d263eb03707d7514b87c94be0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515988"
---
# <a name="canmodifypermissions-soap"></a>CanModifyPermissions (SOAP)

El **elemento CanModifyPermissions** indica si un usuario puede modificar los permisos de acceso a una ubicación de uso compartido de documentos. 
  
```XML
<CanModifyPermissions /> 
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
|[DocumentSharingLocation (SOAP)](documentsharinglocation-soap.md) <br/> |Representa la información de ubicación y metadatos de una ubicación de uso compartido de documentos.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor booleano del **elemento CanModifyPermissions** indica si los usuarios pueden modificar los permisos de acceso a la ubicación de uso compartido. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)


[Referencia del servicio web de Detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[Elementos XML de detección automática soap para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

