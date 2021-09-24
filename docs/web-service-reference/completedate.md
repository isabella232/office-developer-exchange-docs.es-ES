---
title: CompleteDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CompleteDate
api_type:
- schema
ms.assetid: b2b53b87-6a0b-4a55-bcfc-3bf67d3c1700
description: El elemento CompleteDate representa la fecha en la que se completó un elemento.
ms.openlocfilehash: 07f6034b4fd91d22ad07167d931bcd02a74782f9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518781"
---
# <a name="completedate"></a>CompleteDate

El **elemento CompleteDate** representa la fecha en la que se completó un elemento. 
  
```xml
<CompleteDate/>
```

 **DateTime**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Tarea](task.md) <br/> |Representa una tarea en el Exchange almacén.  <br/> |
|[Flag](flag.md) <br/> |Especifica una marca en un elemento de buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto que representa la fecha y la hora es necesario si se usa este elemento.
  
## <a name="remarks"></a>Comentarios

Establecer **CompleteDate** tiene el mismo efecto que establecer [PercentComplete](percentcomplete.md) en 100 o [Status](status.md) en **Completed**. En una solicitud que establece al menos dos de estas propiedades, la última propiedad procesada determinará el valor que se establece para estos elementos. Por ejemplo, si [PercentComplete](percentcomplete.md) es 100, **CompleteDate** es el 1 de enero de 2007 y [Status](status.md) es **NotStarted** y las propiedades se transmiten en ese orden, el efecto será establecer el estado de la tarea en **NotStarted**, [completedate](completedate.md) en **null** y [PercentComplete](percentcomplete.md) en 0. [](status.md) 
  
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


[Creación de tareas](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[Eliminación de tareas](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

