---
title: GetNonIndexableItemDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ce3994c1-3bb4-4571-b026-34a6c5705410
description: El elemento GetNonIndexableItemDetails especifica una solicitud para recuperar detalles de elementos no indexables.
ms.openlocfilehash: 896b978b9b222454b9e3f016aa0593521e92e33d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533614"
---
# <a name="getnonindexableitemdetails"></a>GetNonIndexableItemDetails

El **elemento GetNonIndexableItemDetails** especifica una solicitud para recuperar detalles de elementos no indexables. 
  
```XML
<GetNonIndexableItemDetails>
    <Mailboxes/>
    <PageSize/>
    <PageItemReference/>
    <PageDirection/>
</GetNonIndexableItemDetails>
```

 **GetNonIndexableItemDetailsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Mailboxes (NonEmptyArrayOfLegacyDNsType)](mailboxes-nonemptyarrayoflegacydnstype.md) <br/> |Especifica una matriz de **elementos Mailbox.**  <br/> |
|[PageSize](pagesize.md) <br/> |Contiene el número de elementos que se devolverán en una sola página para un resultado de búsqueda.  <br/> |
|[PageItemReference](pageitemreference.md) <br/> |Especifica la referencia de un elemento de página.  <br/> |
|[PageDirection](pagedirection.md) <br/> |Contiene la dirección de paginación en el resultado de la búsqueda.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

