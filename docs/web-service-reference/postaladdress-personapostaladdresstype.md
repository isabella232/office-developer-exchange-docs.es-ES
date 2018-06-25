---
title: PostalAddress (PersonaPostalAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 075f7d65-9d05-47cb-af26-0dd6d5593439
description: El elemento PostalAddress especifica la dirección postal para un rol.
ms.openlocfilehash: fb418154867aebb4d284e75be579003c0ddc88f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836855"
---
# <a name="postaladdress-personapostaladdresstype"></a>PostalAddress (PersonaPostalAddressType)

El elemento **PostalAddress** especifica la dirección postal para un rol. 
  
```XML
<PostalAddress>
   <Street/>
   <City/>
   <State/>
   <Country/>
   <PostalCode/>
   <PostOfficeBox/>
   <Type/>
   <Latitude/>
   <Longitude/>
   <Accuracy/>
   <Altitude/>
   <AltitudeAccuracy/>
   <FormattedAddress/>
   <LocationUri/>
   <LocationSource/>
</PostalAddress>
```

 **PersonaPostalAddressType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[Calle](street.md) | [Ciudad](city.md) | [estado](state-ex15websvcsotherref.md) | [país](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [(string) de tipo](type-string.md) | [latitud](latitude.md)  |  [ Longitud](longitude.md) | [precisión](accuracy.md) | [altitud](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)
  
### <a name="parent-elements"></a>Elementos principales

[EnhancedLocation](enhancedlocation.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

