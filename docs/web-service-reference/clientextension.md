---
title: ClientExtension
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3445ef2b-1bb1-43ea-bc93-85c72401e5b6
description: El elemento ClientExtension contiene información de usuario y de configuración sobre una aplicación.
ms.openlocfilehash: 5051248a2c8e664d82666bd7b42ee3c3046f43fe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763742"
---
# <a name="clientextension"></a>ClientExtension

El elemento **ClientExtension** contiene información de usuario y de configuración sobre una aplicación. 
  
```XML
<ClientExtension IsAvailable=" true | false " IsMandatory=" true | false " IsEnabledByDefault=" true | false " Type="" Scope="" MarketplaceAssetId="" MarketplaceContentMarket="" AppStatus="" Etoken="">
    <SpecificUsers></SpecificUsers>
    <Manifest></Manifest>
</ClientExtension>
```

 **ClientExtensionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|IsAvailable  <br/> |Especifica si la aplicación está disponible. Un valor de texto de **true** para el atributo **IsAvailable** indica que la aplicación está disponible. Un valor de **false** indica que la aplicación no está disponible. Este atributo es opcional.  <br/> |
|IsMandatory  <br/> |Especifica si la aplicación es obligatoria. Un valor de texto de **true** para el atributo **IsMandatory** indica que la aplicación es obligatoria para el buzón de correo. Un valor de **false** indica que la aplicación no es obligatoria. Este atributo es opcional.  <br/> |
|IsEnabledByDefault  <br/> |Especifica si la aplicación está habilitada de forma predeterminada. Un valor de texto de **true** para el atributo **IsEnabledByDefault** indica que la aplicación está habilitada de forma predeterminada. Un valor de **false** indica que la aplicación no está habilitada de forma predeterminada. Este atributo es opcional.  <br/> |
|ProvidedTo  <br/> |Especifica a quien se proporciona la aplicación. Este atributo es opcional.  <br/> |
|Tipo  <br/> |Especifica el tipo de la aplicación.  <br/> |
|Ámbito  <br/> |Especifica el ámbito de la aplicación.  <br/> |
|MarketplaceAssetId  <br/> |Especifica el identificador de activo del catálogo de soluciones de la aplicación.  <br/> |
|MarketplaceContentMarket  <br/> |Especifica el contenido del catálogo de soluciones que un usuario ve para obtener información detallada y revisa acerca de una aplicación.  <br/> |
|AppStatus  <br/> |Especifica el código de estado de una aplicación de correo en un estado inesperado.  <br/> |
|Etoken  <br/> |Especifica el token de licencia para las aplicaciones de correo de pago o de prueba.  <br/> |
   
#### <a name="type"></a>Tipo

|**Valor**|**Descripción**|
|:-----|:-----|
|Default  <br/> |Indica que la aplicación está disponible de forma predeterminada.  <br/> |
|Privado  <br/> |Indica que la aplicación es privada.  <br/> |
|Catálogo de soluciones  <br/> |Indica que la aplicación es una aplicación de catálogo de soluciones.  <br/> |
   
#### <a name="scope"></a>Ámbito

|**Valor**|**Descripción**|
|:-----|:-----|
|None  <br/> |Indica que la aplicación no tiene ningún ámbito.  <br/> |
|User  <br/> |Indica que la aplicación es por usuario.  <br/> |
|Organización  <br/> |Indica que la aplicación es para una organización.  <br/> |
|Default  <br/> |Indica que la aplicación es una aplicación predeterminada.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[SpecificUsers](specificusers.md) <br/> |Especifica las cuentas de correo electrónico que pueden tener acceso a la aplicación.  <br/> |
|[Manifest](manifest.md) <br/> |Contiene el archivo de manifiesto de aplicación de base-64 codificada.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ClientExtensions](clientextensions.md) <br/> |Especifica una matriz de elementos de **ClientExtension** .  <br/> |
   
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

