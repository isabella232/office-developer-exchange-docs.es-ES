---
title: Suceda
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Occurrence
api_type:
- schema
ms.assetid: d292b99c-b896-40b7-be5d-2cb314c9481f
description: El elemento Representation representa una única ocurrencia modificada de un elemento de calendario periódico.
ms.openlocfilehash: c3a6bcce23f0bb1125dbd2a5bb86e9b20039a4e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466321"
---
# <a name="occurrence"></a>Suceda

El **elemento** Representation representa una única ocurrencia modificada de un elemento de calendario periódico. 
  
```xml
<Occurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</Occurrence>
```

**OccurrenceInfoType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Contiene el identificador único y la clave de cambio de una repetición modificada de un elemento de calendario periódico.  <br/> |
|[Start](start.md) <br/> |Representa la hora de inicio de una repetición modificada de un elemento de calendario periódico.  <br/> |
|[Centraliza](end-ex15websvcsotherref.md) <br/> |Representa la hora de finalización de una repetición modificada de un elemento de calendario periódico.  <br/> |
|[OriginalStart](originalstart.md) <br/> |Representa la hora de inicio original de una repetición modificada de un elemento de calendario periódico.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |Contiene una colección de repeticiones de elementos de calendario periódicas que se han modificado para que sean diferentes del elemento principal de periodicidad.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

