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
description: El elemento RecurringMasterItemId identifica un elemento de patrón de periodicidad mediante la identificación de los identificadores de uno de sus elementos de repetición relacionados.
ms.openlocfilehash: ae59e33ece55d85435ece4c9030ccda32eb62eab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837015"
---
# <a name="recurringmasteritemid"></a>RecurringMasterItemId

El elemento **RecurringMasterItemId** identifica un elemento de patrón de periodicidad mediante la identificación de los identificadores de uno de sus elementos de repetición relacionados. 
  
```XML
<RecurringMasterItemId OccurrenceId="" ChangeKey="" />
```

 **RecurringMasterItemIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**Repetición** <br/> |Identifica una sola aparición de un elemento maestro periódico. Este atributo es necesario.  <br/> |
|**ChangeKey** <br/> |Identifica una versión específica de una sola aparición de un elemento maestro periódico. Además, el elemento maestro periódico también se identifica porque se y la aparición único va a contener la misma clave de cambio. Este atributo es opcional.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |Contiene la colección de identificadores de elemento para todos los elementos de la conversación en un buzón de correo.  <br/> |
|[ItemChange](itemchange.md) <br/> |Contiene un identificador de elemento y las actualizaciones que se debe aplicar al elemento. <br/> <br/> La siguiente es la expresión de XPath para este elemento: <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[ItemId](itemids.md) <br/> | Contiene las identidades únicas de los elementos, elementos de aparición y elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos en el almacén de Exchange. <br/> <br/>  Los siguientes son las expresiones de XPath para este elemento:  <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se identifica el elemento maestro periódico mediante la identificación de uno de sus apariciones con el identificador 56lkjh6.
  
```XML
<RecurringMasterItemId OccurrenceId="56lkjh6" />
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [OccurrenceItemId](occurrenceitemid.md)
- [Operación de FindConversation](findconversation-operation.md)

