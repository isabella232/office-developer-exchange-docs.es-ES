---
title: LocationSource
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fc4d77d5-6200-4cf3-848a-1088fec0e0d6
description: El elemento LocationSource especifica información sobre el origen de la dirección postal asociada, por ejemplo, un contacto o una libreta de teléfonos.
ms.openlocfilehash: ceba52c43d1c798bb8f5492b779c7c45d7d00b0b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467105"
---
# <a name="locationsource"></a>LocationSource

El elemento **LocationSource** especifica información sobre el origen de la dirección postal asociada, por ejemplo, un contacto o una libreta de teléfonos. 
  
```XML
<LocationSource> None | LocationServices | PhonebookServices | Device | Contact | Resource </LocationSource>
```

 **LocationSourceType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[Valor (PersonaPostalAddressType)](value-personapostaladdresstype.md)  |  [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)
  
## <a name="text-value"></a>Valor de texto

En la tabla siguiente se enumeran los valores de texto para el elemento **LocationSource** : 
  
**Valores de texto del elemento LocationSource**

|**Valor**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |No hay origen de la ubicación.  <br/> |
|LocationServices  <br/> |La información se obtuvo de los servicios de ubicación.  <br/> |
|PhonebookServices  <br/> |La información se obtuvo de los servicios de la libreta de teléfonos.  <br/> |
|Dispositivo  <br/> |La información se obtuvo del dispositivo.  <br/> |
|Contacto  <br/> |La información se obtuvo de un contacto.  <br/> |
|Resource  <br/> |La información se obtuvo de un recurso.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  

