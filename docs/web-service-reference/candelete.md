---
title: CanDelete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CanDelete
api_type:
- schema
ms.assetid: 55e17121-aad0-4f90-889f-2c3512e9579c
description: El elemento CanDelete indica si un cliente puede eliminar una carpeta administrada.
ms.openlocfilehash: ad7e573aeb2bb72d19f05421d0eab5a2f6ac5539
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516002"
---
# <a name="candelete"></a>CanDelete

El **elemento CanDelete** indica si un cliente puede eliminar una carpeta administrada. 
  
```xml
<CanDelete/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |Contiene información sobre una carpeta administrada.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto que representa un valor booleano es necesario si este elemento está presente. Un valor **de true** indica que se puede eliminar la carpeta; un valor de **false** significa que la carpeta no se puede eliminar. 
  
## <a name="remarks"></a>Comentarios

Para eliminar una carpeta administrada, use la [operación DeleteFolder](deletefolder-operation.md).
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación CreateManagedFolder](createmanagedfolder-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Eliminación de carpetas](https://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

