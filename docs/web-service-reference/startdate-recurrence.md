---
title: StartDate (Recurrence)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- StartDate
api_type:
- schema
ms.assetid: bd65ac06-b3ac-4c9b-9568-3e4dc94378e7
description: El elemento StartDate representa la fecha de inicio de una tarea periódica o un elemento de calendario.
ms.openlocfilehash: 50f83e5c97d346cc3f7dfced1ee71aa3f9f38ed5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545870"
---
# <a name="startdate-recurrence"></a>StartDate (Recurrence)

El **elemento StartDate** representa la fecha de inicio de una tarea periódica o un elemento de calendario. 
  
```xml
<StartDate/>
```

**Date**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[EndDateRecurrence](enddaterecurrence.md) <br/> |Describe la fecha de inicio y la fecha de finalización de un patrón de periodicidad de elementos.  <br/> |
|[NoEndRecurrence](noendrecurrence.md) <br/> |Describe la fecha de inicio de un patrón de periodicidad de elementos que no tiene una fecha de finalización definida.  <br/> |
|[NumberedRecurrence](numberedrecurrence.md) <br/> |Describe la fecha de inicio y el número de repeticiones de un elemento periódico.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, se requiere un valor de texto que represente una fecha. El valor no puede ser inferior a Apr, 1, 1601 00:00:00.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

