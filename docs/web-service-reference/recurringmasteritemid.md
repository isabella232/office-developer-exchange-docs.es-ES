---
title: RecurringMasterItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RecurringMasterItemId
api_type:
- schema
ms.assetid: 5800b58c-f3d7-4d8f-acc0-d13e02f4e258
description: El elemento RecurringMasterItemId identifica un elemento maestro de periodicidad identificando los identificadores de uno de sus elementos de repetición relacionados.
ms.openlocfilehash: d00794f2b5b1893e1829a3f09df9f3e88266964d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523632"
---
# <a name="recurringmasteritemid"></a>RecurringMasterItemId

El **elemento RecurringMasterItemId** identifica un elemento maestro de periodicidad identificando los identificadores de uno de sus elementos de repetición relacionados. 
  
```XML
<RecurringMasterItemId OccurrenceId="" ChangeKey="" />
```

 **RecurringMasterItemIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**OccurrenceId** <br/> |Identifica una única aparición de un elemento maestro periódico. Este atributo es obligatorio.  <br/> |
|**ChangeKey** <br/> |Identifica una versión específica de una única aparición de un elemento maestro periódico. Además, el elemento maestro periódico también se identifica porque él y la única repetición contendrán la misma clave de cambio. Este atributo es opcional.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |Contiene la colección de identificadores de elementos para todos los elementos de conversación de un buzón.  <br/> |
|[ItemChange](itemchange.md) <br/> |Contiene un identificador de elemento y las actualizaciones que se aplicarán al elemento. <br/> <br/> A continuación se muestra la expresión XPath de este elemento: <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[ItemIds](itemids.md) <br/> | Contiene las identidades únicas de los elementos, los elementos de repetición y los elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos en el Exchange almacén. <br/> <br/>  Las siguientes son las expresiones XPath de este elemento:  <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se identifica el elemento maestro periódico identificando una de sus repeticiones con el identificador 56lkjh6.
  
```XML
<RecurringMasterItemId OccurrenceId="56lkjh6" />
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [OccurrenceItemId](occurrenceitemid.md)
- [Operación FindConversation](findconversation-operation.md)

