---
title: MustDisplayComment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MustDisplayComment
api_type:
- schema
ms.assetid: 11d4d3c3-4652-4ed4-9b29-a0b5f85b82b7
description: El elemento MustDisplayComment indica si se debe mostrar el comentario de carpeta administrada.
ms.openlocfilehash: da1a5e01c1cf244385964db0a3c1a4be705cc25f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518130"
---
# <a name="mustdisplaycomment"></a>MustDisplayComment

El **elemento MustDisplayComment** indica si se debe mostrar el comentario de carpeta administrada. 
  
```xml
<MustDisplayComment/>
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

El valor de texto representa un valor booleano. Un valor **de true** indica que se debe mostrar el comentario; un valor **de false** indica que no es necesario mostrar el comentario. 
  
## <a name="remarks"></a>Comentarios

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

