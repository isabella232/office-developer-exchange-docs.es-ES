---
title: AlternatePublicFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AlternatePublicFolderId
api_type:
- schema
ms.assetid: 0a4dc1cc-959e-4b93-aa3a-3020ca8b8a02
description: El elemento AlternatePublicFolderId describe un identificador de la carpeta pública para convertir a otro formato de identificador. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 32e6e75eb381e479baf5fdb5ad0a40b32c1b02a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763435"
---
# <a name="alternatepublicfolderid"></a>AlternatePublicFolderId

El elemento **AlternatePublicFolderId** describe un identificador de la carpeta pública para convertir a otro formato de identificador. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
- [ConvertId](convertid.md)
  
- [SourceIds](sourceids.md)
  
- [AlternatePublicFolderId](alternatepublicfolderid.md)
  
```xml
<AlternatePublicFolderId FolderId="" Format="" />
```

 **AlternatePublicFolderIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|FolderId  <br/> |Contiene el identificador de la carpeta pública para convertir. Este atributo es necesario.  <br/> |
|Format  <br/> |Identifica el formato que describe el identificador de carpeta pública para convertir. Este atributo es necesario.  <br/> |
   
#### <a name="format-attribute"></a>Atributo de formato

|**Valor**|**Descripción**|
|:-----|:-----|
|EwsLegacyId  <br/> |Describe identificadores producidos por servicios Web de Exchange en la versión inicial de Exchange 2007.  <br/> |
|EwsId  <br/> |Describe identificadores producidos por los servicios Web Exchange comenzando con Exchange 2007 SP1.  <br/> |
|Propiedad EntryId  <br/> |Describe identificadores de MAPI, como se muestra en la propiedad de entrada del objeto.  <br/> |
|HexEntryId  <br/> |Describe una representación codificada en hexadecimal de la propiedad de entrada del objeto. Éste es el formato de los identificadores de eventos de calendario de disponibilidad.  <br/> |
|StoreId  <br/> |Describe identificadores de almacén de Exchange.  <br/> |
|OwaId  <br/> |Se describe un identificador de Outlook Web Access.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |Contiene los identificadores de origen para convertir. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación ConvertId](convertid-operation.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)
- [Convertir identificadores](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

