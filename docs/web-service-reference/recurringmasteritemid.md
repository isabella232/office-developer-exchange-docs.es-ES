---
title: RecurringMasterItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringMasterItemId
api_type:
- schema
ms.assetid: 5800b58c-f3d7-4d8f-acc0-d13e02f4e258
description: El elemento RecurringMasterItemId identifica un elemento principal de periodicidad mediante la identificación de los identificadores de uno de los elementos de repeticiones relacionados.
ms.openlocfilehash: 896a9ce95d619e7bb44c8158288bc4f62ce417d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529885"
---
# <a name="recurringmasteritemid"></a>RecurringMasterItemId

El elemento **RecurringMasterItemId** identifica un elemento principal de periodicidad mediante la identificación de los identificadores de uno de los elementos de repeticiones relacionados. 
  
```XML
<RecurringMasterItemId OccurrenceId="" ChangeKey="" />
```

 **RecurringMasterItemIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**OccurrenceId** <br/> |Identifica una única ocurrencia de un elemento maestro periódico. Este atributo es obligatorio.  <br/> |
|**ChangeKey** <br/> |Identifica una versión específica de una ocurrencia única de un elemento maestro periódico. Además, el elemento maestro periódico también se identifica porque éste y la única instancia contendrán la misma clave de cambio. Este atributo es opcional.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |Contiene la colección de identificadores de elemento para todos los elementos de conversación en un buzón.  <br/> |
|[ItemChange](itemchange.md) <br/> |Contiene un identificador de elemento y las actualizaciones que se aplican al elemento. <br/> <br/> La siguiente es la expresión XPath a este elemento: <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[ItemIds](itemids.md) <br/> | Contiene las identidades únicas de los elementos, los elementos de ocurrencia y los elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos en el almacén de Exchange. <br/> <br/>  Las siguientes son las expresiones XPath de este elemento:  <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se identifica el elemento maestro periódico mediante la identificación de una de sus repeticiones con el identificador 56lkjh6.
  
```XML
<RecurringMasterItemId OccurrenceId="56lkjh6" />
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [OccurrenceItemId](occurrenceitemid.md)
- [Operación FindConversation](findconversation-operation.md)

