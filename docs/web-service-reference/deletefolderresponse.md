---
title: DeleteFolderResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolderResponse
api_type:
- schema
ms.assetid: 27578bda-ef0a-4a33-bccc-2c1bc1735424
description: El elemento DeleteFolderResponse define una respuesta a una solicitud DeleteFolder.
ms.openlocfilehash: 58b814662c769784c5fd682a9e039863a9787d8d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458491"
---
# <a name="deletefolderresponse"></a>DeleteFolderResponse

El elemento **DeleteFolderResponse** define una respuesta a una solicitud DeleteFolder. 
  
```xml
<DeleteFolderResponse>
   <ResponseMessages/>
</DeleteFolderResponse>
```

 **DeleteFolderResponseType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación DeleteFolder](deletefolder-operation.md) 
- [DeleteFolder](deletefolder.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

