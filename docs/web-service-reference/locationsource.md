---
title: LocationSource
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: fc4d77d5-6200-4cf3-848a-1088fec0e0d6
description: El elemento LocationSource especifica información sobre el origen de la dirección postal asociada, por ejemplo, un contacto o una libreta de teléfono.
ms.openlocfilehash: f3569494d3e662fbc46060944c8bd399b62d656b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543264"
---
# <a name="locationsource"></a>LocationSource

El **elemento LocationSource** especifica información sobre el origen de la dirección postal asociada, por ejemplo, un contacto o una libreta de teléfono. 
  
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

Los valores de texto del **elemento LocationSource** se enumeran en la tabla siguiente: 
  
**Valores de texto del elemento LocationSource**

|**Valor**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |No hay ningún origen de ubicación.  <br/> |
|LocationServices  <br/> |La información se obtuvo de los servicios de ubicación.  <br/> |
|PhonebookServices  <br/> |La información se obtuvo de los servicios de la libreta de teléfonos.  <br/> |
|Dispositivo  <br/> |La información se obtuvo del dispositivo.  <br/> |
|Contacto  <br/> |La información se obtuvo de un contacto.  <br/> |
|Recurso  <br/> |La información se obtuvo de un recurso.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  

