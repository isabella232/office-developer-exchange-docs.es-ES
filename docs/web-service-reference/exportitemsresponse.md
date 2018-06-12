---
title: ExportItemsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExportItemsResponse
api_type:
- schema
ms.assetid: ef44354b-fbdb-4f7c-b6bd-b27f56a1d018
description: El elemento ExportItemsResponse representa la respuesta a una única solicitud de ExportItems.
ms.openlocfilehash: 08033532d9cc381be8c544d790e9fe43840efb7b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764497"
---
# <a name="exportitemsresponse"></a>ExportItemsResponse

El elemento **ExportItemsResponse** representa la respuesta a una única solicitud de **ExportItems** . 
  
[ExportItemsResponse](exportitemsresponse.md)
  
```XML
<ExportItemsResponse>
   <ResponseMessages/>
</ExportItemsResponse>
```

 **ExportItemsResponseType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación ExportItems](exportitems-operation.md)
  
[Operación UploadItems](uploaditems-operation.md)

