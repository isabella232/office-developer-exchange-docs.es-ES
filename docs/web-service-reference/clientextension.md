---
title: ClientExtension
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3445ef2b-1bb1-43ea-bc93-85c72401e5b6
description: El elemento ClientExtension contiene información de usuario y configuración sobre una aplicación.
ms.openlocfilehash: d3d9ce1d242a63f28da3464f0faff86abde502c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460200"
---
# <a name="clientextension"></a>ClientExtension

El elemento **ClientExtension** contiene información de usuario y configuración sobre una aplicación. 
  
```XML
<ClientExtension IsAvailable=" true | false " IsMandatory=" true | false " IsEnabledByDefault=" true | false " Type="" Scope="" MarketplaceAssetId="" MarketplaceContentMarket="" AppStatus="" Etoken="">
    <SpecificUsers></SpecificUsers>
    <Manifest></Manifest>
</ClientExtension>
```

 **ClientExtensionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|IsAvailable  <br/> |Especifica si la aplicación está disponible. Un valor de texto de **true** para el atributo **isavailable** indica que la aplicación está disponible. Un valor de **false** indica que la aplicación no está disponible. Este atributo es opcional.  <br/> |
|IsMandatory  <br/> |Especifica si la aplicación es obligatoria. Un valor de texto de **true** para el atributo **IsMandatory** indica que la aplicación es obligatoria para el buzón. Un valor de **false** indica que la aplicación no es obligatoria. Este atributo es opcional.  <br/> |
|IsEnabledByDefault  <br/> |Especifica si la aplicación está habilitada de forma predeterminada. Un valor de texto de **true** para el atributo **IsEnabledByDefault** indica que la aplicación está habilitada de forma predeterminada. Un valor de **false** indica que la aplicación no está habilitada de forma predeterminada. Este atributo es opcional.  <br/> |
|ProvidedTo  <br/> |Especifica la persona a la que se proporciona la aplicación. Este atributo es opcional.  <br/> |
|Tipo  <br/> |Especifica el tipo de aplicación.  <br/> |
|Ámbito  <br/> |Especifica el ámbito de la aplicación.  <br/> |
|MarketplaceAssetId  <br/> |Especifica el identificador de activos del mercado de la aplicación.  <br/> |
|MarketplaceContentMarket  <br/> |Especifica el contenido del catálogo de soluciones que un usuario ve para obtener detalles y revisiones de una aplicación.  <br/> |
|AppStatus  <br/> |Especifica el código de estado de una aplicación de correo en un estado inesperado.  <br/> |
|Etoken  <br/> |Especifica el token de licencia para las aplicaciones de correo de pago o de prueba.  <br/> |
   
#### <a name="type"></a>Tipo

|**Valor**|**Descripción**|
|:-----|:-----|
|Predeterminado  <br/> |Indica que la aplicación está disponible de forma predeterminada.  <br/> |
|Private  <br/> |Indica que la aplicación es privada.  <br/> |
|Venta  <br/> |Indica que la aplicación es una aplicación del catálogo de soluciones.  <br/> |
   
#### <a name="scope"></a>Ámbito

|**Valor**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |Indica que la aplicación no tiene ningún ámbito.  <br/> |
|User  <br/> |Indica que la aplicación es por usuario.  <br/> |
|Organización  <br/> |Indica que la aplicación es para una organización.  <br/> |
|Predeterminado  <br/> |Indica que la aplicación es una aplicación predeterminada.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SpecificUsers](specificusers.md) <br/> |Especifica las cuentas de correo electrónico que pueden acceder a la aplicación.  <br/> |
|[Manifiesto](manifest.md) <br/> |Contiene el archivo de manifiesto de la aplicación codificado de base 64.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ClientExtensions](clientextensions.md) <br/> |Especifica una matriz de elementos **ClientExtension** .  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

