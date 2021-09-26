---
title: AlternatePublicFolderItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AlternatePublicFolderItemId
api_type:
- schema
ms.assetid: a67df9b9-8fdb-42de-b9c5-8377b71fa3d9
description: El elemento AlternatePublicFolderItemId describe un identificador de elemento de carpeta pública para convertirlo a otro formato de identificador. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: e3d71d17c6e9321a1accfbaf90967d2b504f5efe
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543717"
---
# <a name="alternatepublicfolderitemid"></a>AlternatePublicFolderItemId

El **elemento AlternatePublicFolderItemId** describe un identificador de elemento de carpeta pública para convertirlo a otro formato de identificador. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
- [ConvertId](convertid.md)
  
- [SourceIds](sourceids.md)
  
- [AlternatePublicFolderItemId](alternatepublicfolderitemid.md)
  
```xml
<AlternatePublicFolderItemId FolderId="" Format="" ItemId=""/>
```

 **AlternatePublicFolderItemIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|FolderId  <br/> |Identifica la carpeta pública que contiene el elemento de carpeta pública. Este atributo es obligatorio.  <br/> |
|Formato  <br/> |Identifica el formato que describe el identificador de elemento de carpeta pública que se debe convertir. Este atributo es obligatorio.  <br/> |
|ItemId  <br/> |Identificador del elemento de carpeta pública que se convertirá. Este atributo es obligatorio.  <br/> |
   
#### <a name="format-attribute-values"></a>Valores de atributo Format

|**Valor**|**Descripción**|
|:-----|:-----|
|EwsLegacyId  <br/> |Describe los identificadores generados por Exchange Web Services en la versión de lanzamiento inicial de Exchange 2007.  <br/> |
|EwsId  <br/> |Describe los identificadores generados por Exchange Web Services a partir Exchange 2007 SP1.  <br/> |
|EntryID  <br/> |Describe los identificadores MAPI, como en la PR_ENTRYID propiedad.  <br/> |
|HexEntryId  <br/> |Describe una representación con codificación hexadecimal de la PR_ENTRYID propiedad. Este es el formato de los identificadores de eventos del calendario de disponibilidad.  <br/> |
|StoreId  <br/> |Describe Exchange identificadores de almacén.  <br/> |
|OwaId  <br/> |Describe un identificador Outlook Web Access.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |Contiene los identificadores de origen que se convertirán. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Operación ConvertId](convertid-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)
- [Conversión de identificadores](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

