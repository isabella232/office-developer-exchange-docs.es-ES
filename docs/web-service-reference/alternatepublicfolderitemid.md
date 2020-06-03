---
title: AlternatePublicFolderItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AlternatePublicFolderItemId
api_type:
- schema
ms.assetid: a67df9b9-8fdb-42de-b9c5-8377b71fa3d9
description: El elemento AlternatePublicFolderItemId describe un identificador de elemento de carpeta pública para convertir a otro formato de identificador. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 11a9fafec78a9bd14e4d98982fd38954d45e4d1a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464773"
---
# <a name="alternatepublicfolderitemid"></a>AlternatePublicFolderItemId

El elemento **AlternatePublicFolderItemId** describe un identificador de elemento de carpeta pública para convertir a otro formato de identificador. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
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
|Formato  <br/> |Identifica el formato que describe el identificador de elemento de carpeta pública que se va a convertir. Este atributo es obligatorio.  <br/> |
|ItemId  <br/> |Identificador el elemento de carpeta pública que se va a convertir. Este atributo es obligatorio.  <br/> |
   
#### <a name="format-attribute-values"></a>Valores de atributo de formato

|**Valor**|**Descripción**|
|:-----|:-----|
|EwsLegacyId  <br/> |Describe los identificadores producidos por los servicios Web de Exchange en la versión de lanzamiento inicial de Exchange 2007.  <br/> |
|EwsId  <br/> |Describe los identificadores que crean los servicios Web de Exchange a partir de Exchange 2007 SP1.  <br/> |
|EntryId  <br/> |Describe los identificadores de MAPI, como en la propiedad PR_ENTRYID.  <br/> |
|HexEntryId  <br/> |Describe una representación codificada en hexadecimal de la propiedad PR_ENTRYID. Este es el formato de los identificadores de evento de calendario de disponibilidad.  <br/> |
|StoreId  <br/> |Describe los identificadores de almacén de Exchange.  <br/> |
|OwaId  <br/> |Describe un identificador de Outlook Web Access.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |Contiene los identificadores de origen que se van a convertir. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación ConvertId](convertid-operation.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)
- [Convertir identificadores](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

