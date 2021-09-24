---
title: ServerVersionInfo (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 8662647b-e50a-4774-9ba3-a951ae6df781
description: El elemento ServerVersionInfo contiene la versión del servidor que procesó la solicitud.
ms.openlocfilehash: ac52b3eda429e65cb1ec046167a63fe4029d423a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521461"
---
# <a name="serverversioninfo-soap"></a>ServerVersionInfo (SOAP)

El **elemento ServerVersionInfo** contiene la versión del servidor que procesó la solicitud. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MajorVersion (SOAP)](majorversion-soap.md) <br/> |El número de versión principal del servidor.  <br/> |
|[MinorVersion (SOAP)](minorversion-soap.md) <br/> |Número de versión secundaria del servidor.  <br/> |
|[MajorBuildNumber (SOAP)](majorbuildnumber-soap.md) <br/> |El número de compilación principal del servidor.  <br/> |
|[MinorBuildNumber (SOAP)](minorbuildnumber-soap.md) <br/> |Número de compilación secundaria para el servidor.  <br/> |
|[Version (SOAP)](version-soap.md) <br/> |Una descripción de la versión del producto del servidor.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Este elemento se devuelve en el encabezado SOAP.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   

