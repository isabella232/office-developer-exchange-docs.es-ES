---
title: SourceIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SourceIds
api_type:
- schema
ms.assetid: 0043abd5-ba9c-4d67-8832-325f32bf7651
description: El elemento SourceIds contiene los identificadores de origen que se van a convertir.
ms.openlocfilehash: 1c4990f2185788c5cfaab5483cb6a54a0d850596
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466111"
---
# <a name="sourceids"></a>SourceIds

El elemento **SourceIds** contiene los identificadores de origen que se van a convertir. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AlternateId](alternateid.md) <br/> |Describe un identificador de elemento o carpeta que se va a convertir.  <br/> |
|[AlternatePublicFolderId](alternatepublicfolderid.md) <br/> |Describe un identificador de carpeta pública que se va a convertir.  <br/> |
|[AlternatePublicFolderItemId](alternatepublicfolderitemid.md) <br/> |Describe un identificador de elemento de carpeta pública que se va a convertir.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ConvertId](convertid.md) <br/> |Define una solicitud para convertir los identificadores de elemento y carpeta entre los formatos admitidos por Exchange.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación ConvertId](convertid-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


[Convertir identificadores](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

