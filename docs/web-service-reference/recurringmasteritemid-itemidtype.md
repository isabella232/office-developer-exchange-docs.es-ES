---
title: RecurringMasterItemId (ItemIdType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 48d831cf-10d8-480b-86d2-f9c0b14b8167
description: El elemento RecurringMasterItemId (ItemIdType) identifica un elemento de patrón de periodicidad mediante la identificación de los identificadores de uno de sus elementos de repetición relacionados.
ms.openlocfilehash: 89089067963e99ac1a6cae6ea6e1e8350d148e82
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837010"
---
# <a name="recurringmasteritemid-itemidtype"></a>RecurringMasterItemId (ItemIdType)

El elemento **RecurringMasterItemId (ItemIdType)** identifica un elemento de patrón de periodicidad mediante la identificación de los identificadores de uno de sus elementos de repetición relacionados. 
  
```XML
<RecurringMasterItemId Id="" ChangeKey=""/>
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

****

|**Attribute**|**Descripción**|
|:-----|:-----|
|Id  <br/> |Identifica una sola aparición de un elemento maestro periódico. Este atributo es necesario.  <br/> |
|ChangeKey  <br/> |Identifica una versión específica de una sola aparición de un elemento maestro periódico. Además, el elemento maestro periódico también se identifica porque se y la aparición único va a contener la misma clave de cambio. Este atributo es opcional.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[Aviso](reminder.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Aviso](reminder.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

