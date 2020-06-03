---
title: SearchParameters
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SearchParameters
api_type:
- schema
ms.assetid: 34602cb1-dc33-4552-a98c-3e77f614daa3
description: El elemento SearchParameters representa los parámetros que definen una carpeta de búsqueda.
ms.openlocfilehash: cd9f255621b17d01113392e67a0301b01b70f326
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466671"
---
# <a name="searchparameters"></a>SearchParameters

El elemento **SearchParameters** representa los parámetros que definen una carpeta de búsqueda. 
  
```xml
<SearchParameters Traversal="">
   <Restriction/>
   <BaseFolderIds/>
</SearchParameters>
```

 **SearchParametersType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Transversal** <br/> |Describe cómo una carpeta de búsqueda atraviesa la jerarquía de carpetas. Las opciones son para una búsqueda en **profundidad** o **superficial** .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones de carpeta de búsqueda FindItem/FindFolder.  <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |Representa la colección de carpetas que se extendrán para determinar el contenido de una carpeta de búsqueda.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda contenida en un buzón.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

