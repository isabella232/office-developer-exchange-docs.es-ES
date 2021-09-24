---
title: Occurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Occurrence
api_type:
- schema
ms.assetid: d292b99c-b896-40b7-be5d-2cb314c9481f
description: El elemento Occurrence representa una única aparición modificada de un elemento de calendario periódico.
ms.openlocfilehash: 465c02263eadfc74629a8e21ebccf076206ec0d2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518095"
---
# <a name="occurrence"></a>Occurrence

El **elemento Occurrence** representa una única aparición modificada de un elemento de calendario periódico. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Contiene el identificador único y la clave de cambio de una repetición modificada de un elemento de calendario periódico.  <br/> |
|[Start](start.md) <br/> |Representa la hora de inicio de una aparición modificada de un elemento de calendario periódico.  <br/> |
|[Fin ](end-ex15websvcsotherref.md) <br/> |Representa la hora de finalización de una aparición modificada de un elemento de calendario periódico.  <br/> |
|[OriginalStart](originalstart.md) <br/> |Representa la hora de inicio original de una aparición modificada de un elemento de calendario periódico.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |Contiene una colección de repeticiones periódicas de elementos de calendario que se han modificado para que sean diferentes del elemento maestro de periodicidad.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

