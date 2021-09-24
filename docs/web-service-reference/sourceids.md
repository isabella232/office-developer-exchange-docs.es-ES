---
title: SourceIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SourceIds
api_type:
- schema
ms.assetid: 0043abd5-ba9c-4d67-8832-325f32bf7651
description: El elemento SourceIds contiene los identificadores de origen que se convertirán.
ms.openlocfilehash: e6a0767de0928578fb6ae16996ff39908580d45c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521343"
---
# <a name="sourceids"></a>SourceIds

El **elemento SourceIds** contiene los identificadores de origen que se convertirán. 
  
[ConvertId](convertid.md)
  
[SourceIds](sourceids.md)
  
```xml
<SourceIds>
   <AlternateId/>
   <AlternatePublicFolderId/>
   <AlternatePublicFolderItemId/>
</SourceIds>
```

 **NonEmptyArrayOfAlternateIdsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AlternateId](alternateid.md) <br/> |Describe un identificador de elemento o carpeta que se debe convertir.  <br/> |
|[AlternatePublicFolderId](alternatepublicfolderid.md) <br/> |Describe un identificador de carpeta pública que se debe convertir.  <br/> |
|[AlternatePublicFolderItemId](alternatepublicfolderitemid.md) <br/> |Describe un identificador de elemento de carpeta pública que se debe convertir.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ConvertId](convertid.md) <br/> |Define una solicitud para convertir identificadores de elementos y carpetas entre Exchange formatos admitidos.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Exchange Server que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación ConvertId](convertid-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Conversión de identificadores](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

