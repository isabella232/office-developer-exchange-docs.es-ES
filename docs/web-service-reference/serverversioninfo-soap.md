---
title: ServerVersionInfo (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 8662647b-e50a-4774-9ba3-a951ae6df781
description: El elemento ServerVersionInfo contiene la versión del servidor que ha procesado la solicitud.
ms.openlocfilehash: b54b4833361ec78c7f8213473af4638965c7ddae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467651"
---
# <a name="serverversioninfo-soap"></a>ServerVersionInfo (SOAP)

El elemento **ServerVersionInfo** contiene la versión del servidor que ha procesado la solicitud. 
  
```XML
<ServerVersionInfo>
   <MajorVersion/>
   <MinorVersion/>
   <MajorBuildNumber/>
   <MinorBuildNumber/>
   <Version/>
</ServerVersionInfo>
```

 **ServerVersionInfo**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MajorVersion (SOAP)](majorversion-soap.md) <br/> |Número de versión principal del servidor.  <br/> |
|[MinorVersion (SOAP)](minorversion-soap.md) <br/> |Número de versión secundaria del servidor.  <br/> |
|[MajorBuildNumber (SOAP)](majorbuildnumber-soap.md) <br/> |El número de compilación principal del servidor.  <br/> |
|[MinorBuildNumber (SOAP)](minorbuildnumber-soap.md) <br/> |Número de compilación secundaria del servidor.  <br/> |
|[Versión (SOAP)](version-soap.md) <br/> |Una descripción de la versión del producto del servidor.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Este elemento se devuelve en el encabezado SOAP.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   

