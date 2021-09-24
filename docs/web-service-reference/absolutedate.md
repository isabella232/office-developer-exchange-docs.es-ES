---
title: AbsoluteDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AbsoluteDate
api_type:
- schema
ms.assetid: 8bc59a26-6fe1-42e9-968c-69a94a3fb0ae
description: El elemento AbsoluteDate representa la fecha en que cambia la hora del horario estándar o del horario de verano.
ms.openlocfilehash: 5482afcfda1de76d11fea548709836f14c6c2aca
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540373"
---
# <a name="absolutedate"></a>AbsoluteDate

El **elemento AbsoluteDate** representa la fecha en que cambia la hora del horario estándar o del horario de verano. 
  
```xml
<AbsoluteDate/>
```

**date**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Estándar](standard.md) <br/> |Representa la fecha y hora en que la hora cambia del horario de verano a la hora estándar.  <br/> |
|[Daylight](daylight.md) <br/> |Representa la fecha y la hora en que la hora cambia de la hora estándar al horario de verano.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa la fecha en que se produce el cambio entre el horario estándar o el horario de verano.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)




