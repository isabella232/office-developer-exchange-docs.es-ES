---
title: Repetición
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
description: El elemento de repetición representa una sola aparición de modificación de un elemento periódico del calendario.
ms.openlocfilehash: 5a40faa9b885a235d30e7f41830d1eefe2ed23c3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836653"
---
# <a name="occurrence"></a>Repetición

El elemento de **repetición** representa una sola aparición de modificación de un elemento periódico del calendario. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Contiene la clave exclusiva de identificador y el cambio de una ocurrencia modificada de un elemento periódico del calendario.  <br/> |
|[Start](start.md) <br/> |Representa la hora de inicio de una repetición modificada de un elemento periódico del calendario.  <br/> |
|[End](end-ex15websvcsotherref.md) <br/> |Representa la hora de finalización de una ocurrencia modificada de un elemento periódico del calendario.  <br/> |
|[OriginalStart](originalstart.md) <br/> |Representa la hora de inicio original de una ocurrencia modificada de un elemento periódico del calendario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |Contiene una colección de periódica repeticiones del elemento de calendario que se han modificado para que sean diferentes que el elemento de patrón de periodicidad.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

