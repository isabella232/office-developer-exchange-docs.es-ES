---
title: ExpandDLResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExpandDLResponseMessage
api_type:
- schema
ms.assetid: 1140601b-98cf-4cb4-a019-321c7f63d5be
description: El elemento ExpandDLResponseMessage contiene el estado y el resultado de una única solicitud de operación de ExpandDL.
ms.openlocfilehash: 62a81574f9c513b905a92876b3d757c635b4f07b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764496"
---
# <a name="expanddlresponsemessage"></a>ExpandDLResponseMessage

El elemento **ExpandDLResponseMessage** contiene el estado y el resultado de una única solicitud de [la operación de ExpandDL](expanddl-operation.md) . 
  
- [ExpandDLResponse](expanddlresponse.md)  
- [ResponseMessages](responsemessages.md) 
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
  
```xml
<ExpandDLResponseMessage ResponseClass="" IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DLExpansion/>
</ExpandDLResponseMessage>
```

**ExpandDLResponseMessageType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**ResponseClass** <br/> | Describe el estado de una respuesta de [la operación de ExpandDL](expanddl-operation.md) .<br/><br/>Los siguientes valores son válidos para este atributo: <br/> <br/>-Éxito  <br/>-Advertencia  <br/>-Error  <br/> |
|**IndexedPagingOffset** <br/> |Representa el siguiente índice que se debe usar para la solicitud siguiente cuando se usa una vista indizada de paginación.  <br/> |
|**NumeratorOffset** <br/> |Representa el nuevo valor: número que se usará para la solicitud siguiente cuando se usan las vistas de página de fracción.  <br/> |
|**AbsoluteDenominator** <br/> |Representa el denominador siguiente para usar para la solicitud siguiente al realizar la paginación fraccionaria.  <br/> |
|**IncludesLastItemInRange** <br/> |Indica que no es necesario paginación adicional. Este atributo será true si los resultados actuales contienen el último elemento de la consulta.  <br/> |
|**TotalItemsInView** <br/> |Representa el número total de elementos que pase la restricción.  <br/> |
   
#### <a name="responseclass-attribute-values"></a>Valores de atributo de ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|**Operación correcta** <br/> |Describe una solicitud que se cumplen los requisitos.  <br/> |
|**Warning** <br/> | Describe una solicitud que no se procesó. Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.<br/><br/> Los siguientes son ejemplos de fuentes de advertencias:<br/>  <br/>-El almacén de Exchange está sin conexión durante el proceso por lotes.  <br/>-Los servicios de dominio de Active Directory (AD DS) está sin conexión.  <br/>-Se mueven los buzones de correo.  <br/>-La base de datos de buzón (MDB) está sin conexión.  <br/>-Una contraseña ha expirado.  <br/>-Se superó una cuota.  <br/> |
|**Error** <br/> | Describe una solicitud que no se cumplen los requisitos.<br/><br/> Los siguientes son ejemplos de orígenes de errores:  <br/><br/>-No válida Atributos o elementos  <br/>-Los atributos o elementos que están fuera del intervalo  <br/>-Una etiqueta desconocida  <br/>-Un atributo o un elemento que no es válido en el contexto  <br/>-Un intento de acceso no autorizado por cualquier cliente  <br/>-Un error del lado del servidor en respuesta a una llamada de cliente válida <br/> <br/>  Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no se utiliza y está reservado para uso futuro. Contiene un valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información de la respuesta de error adicionales.  <br/> |
|[DLExpansion](dlexpansion.md) <br/> |Contiene una matriz de los buzones de correo que están contenidos en una lista de distribución.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación de ExpandDL](expanddl-operation.md)
- [Referencia EWS para Exchange](ews-reference-for-exchange.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

