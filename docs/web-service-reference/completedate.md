---
title: CompleteDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CompleteDate
api_type:
- schema
ms.assetid: b2b53b87-6a0b-4a55-bcfc-3bf67d3c1700
description: El elemento CompleteDate representa la fecha en que se completó un elemento.
ms.openlocfilehash: fff3d5d3105bf63c9cdd34cbcf828d57ca287b86
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461425"
---
# <a name="completedate"></a>CompleteDate

El elemento **CompleteDate** representa la fecha en que se completó un elemento. 
  
```xml
<CompleteDate/>
```

 **DateTime**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Tarea](task.md) <br/> |Representa una tarea del almacén de Exchange.  <br/> |
|[Flag](flag.md) <br/> |Especifica una marca en un elemento de buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, se necesita un valor de texto que represente la fecha y la hora.
  
## <a name="remarks"></a>Comentarios

La configuración de **CompleteDate** tiene el mismo efecto que establecer [PercentComplete](percentcomplete.md) en 100 o [status](status.md) en **completed**. En una solicitud que establece al menos dos propiedades, la última propiedad procesada determinará el valor que se establece para estos elementos. Por ejemplo, si [PercentComplete](percentcomplete.md) es 100, **CompleteDate** es el 1 de enero de 2007 y [status](status.md) es **NotStarted**, y las propiedades se transmiten en ese orden, el efecto será establecer el [Estado](status.md) de la tarea en **notstarted**, [CompleteDate](completedate.md) en **null**y [PercentComplete](percentcomplete.md) en 0. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


[Creación de tareas](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[Eliminación de tareas](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

