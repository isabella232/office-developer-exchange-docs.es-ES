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
ms.openlocfilehash: 7f5cf5fcca0a72287593349fcf5090a74225d012
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836248"
---
# <a name="locationsource"></a>LocationSource

El elemento **LocationSource** especifica información sobre el origen de la dirección postal asociada, por ejemplo, un contacto o una libreta de teléfonos. 
  
```XML
<LocationSource> None | LocationServices | PhonebookServices | Device | Contact | Resource </LocationSource>
```

 **LocationSourceType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[Valor (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)
  
## <a name="text-value"></a>Valor de texto

Los valores de texto para el elemento de **LocationSource** se enumeran en la siguiente tabla: 
  
**Valores de texto de elemento LocationSource**

|**Valor**|**Descripción**|
|:-----|:-----|
|None  <br/> |No hay ningún origen de la ubicación.  <br/> |
|LocationServices  <br/> |La información obtenida de los servicios de ubicación.  <br/> |
|PhonebookServices  <br/> |La información obtenida de los servicios de libreta de teléfonos.  <br/> |
|Dispositivo  <br/> |Se obtuvo la información desde el dispositivo.  <br/> |
|Contacto  <br/> |La información obtenida de un contacto.  <br/> |
|Recurso  <br/> |La información obtenida de un recurso.  <br/> |
   
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  

