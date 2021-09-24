---
title: PostalAddress (PersonaPostalAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 075f7d65-9d05-47cb-af26-0dd6d5593439
description: El elemento PostalAddress especifica la dirección postal de una persona.
ms.openlocfilehash: 4e95a94c5a7ce917a0a4b9abf7b7ef120301ae6c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523905"
---
# <a name="postaladdress-personapostaladdresstype"></a>PostalAddress (PersonaPostalAddressType)

El **elemento PostalAddress** especifica la dirección postal de una persona. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[Calle](street.md)  |  [Ciudad](city.md)  |  [Estado](state-ex15websvcsotherref.md)  |  [País](country.md)  |  [PostalCode](postalcode.md)  |  [PostOfficeBox](postofficebox.md)  |  [Tipo (cadena)](type-string.md)  |  [Latitud](latitude.md)  |  [Longitud](longitude.md)  |  [Precisión](accuracy.md)  |  [Altitud](altitude.md)  |  [AltitudeAccuracy](altitudeaccuracy.md)  |  [FormattedAddress](formattedaddress.md)  |  [LocationUri](locationuri.md)  |  [LocationSource](locationsource.md)
  
### <a name="parent-elements"></a>Elementos principales

[EnhancedLocation](enhancedlocation.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

