---
title: CanModifyPermissions (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9693de1a-0c76-4898-8f4d-a8693fb005b3
description: El elemento CanModifyPermissions indica si un usuario puede modificar los permisos de acceso a una ubicación de uso compartido de documentos.
ms.openlocfilehash: bf21b80a738498176bac41feea001ff859a54c2b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461586"
---
# <a name="canmodifypermissions-soap"></a>CanModifyPermissions (SOAP)

El elemento **CanModifyPermissions** indica si un usuario puede modificar los permisos de acceso a una ubicación de uso compartido de documentos. 
  
```XML
<CanModifyPermissions /> 
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DocumentSharingLocation (SOAP)](documentsharinglocation-soap.md) <br/> |Representa la información de ubicación y metadatos de una ubicación de uso compartido de documentos.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor booleano del elemento **CanModifyPermissions** indica si los usuarios pueden modificar los permisos de acceso a la ubicación de uso compartido. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)


[Referencia del servicio web de Detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[Elementos XML de detección automática de SOAP para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

