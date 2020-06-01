---
title: SupportedFileExtensions (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f73d18c-7bb1-4ab6-a23b-6d948e590b53
description: El elemento SupportedFileExtensions enumera las extensiones de archivo que se pueden almacenar en una ubicación de uso compartido de documentos.
ms.openlocfilehash: d783b147a25ebbe3bff59c2142012b50bd80004e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44433990"
---
# <a name="supportedfileextensions-soap"></a>SupportedFileExtensions (SOAP)

El elemento **SupportedFileExtensions** enumera las extensiones de archivo que se pueden almacenar en una ubicación de uso compartido de documentos. 
  
```XML
<SupportedFileExtensions /> 
```

 **ArrayOfFileExtension**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FileExtension (SOAP)](fileextension-soap.md) <br/> |Representa una extensión de archivo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DocumentSharingLocation (SOAP)](documentsharinglocation-soap.md) <br/> |Representa la información de ubicación y metadatos de una ubicación de uso compartido de documentos.  <br/> |
   
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

