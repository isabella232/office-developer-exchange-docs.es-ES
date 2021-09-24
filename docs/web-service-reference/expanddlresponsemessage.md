---
title: ExpandDLResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ExpandDLResponseMessage
api_type:
- schema
ms.assetid: 1140601b-98cf-4cb4-a019-321c7f63d5be
description: El elemento ExpandDLResponseMessage contiene el estado y el resultado de una única solicitud de operación ExpandDL.
ms.openlocfilehash: 4683195af3daa462758acbfac4903994818a120e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517073"
---
# <a name="expanddlresponsemessage"></a>ExpandDLResponseMessage

El **elemento ExpandDLResponseMessage** contiene el estado y el resultado de una única [solicitud de operación ExpandDL.](expanddl-operation.md) 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**ResponseClass** <br/> | Describe el estado de una respuesta de [operación ExpandDL.](expanddl-operation.md)<br/><br/>Los siguientes valores son válidos para este atributo: <br/> <br/>- Éxito  <br/>- Advertencia  <br/>- Error  <br/> |
|**IndexedPagingOffset** <br/> |Representa el siguiente índice que se debe usar para la siguiente solicitud cuando se usa una vista de paginación indizada.  <br/> |
|**NumeratorOffset** <br/> |Representa el nuevo valor de numerador que se usará para la siguiente solicitud cuando se usen vistas de página de fracción.  <br/> |
|**AbsoluteDenominator** <br/> |Representa el siguiente denominador que se usará para la siguiente solicitud al realizar la paginación fraccional.  <br/> |
|**IncludesLastItemInRange** <br/> |Indica que no se necesita paginación adicional. Este atributo será true si los resultados actuales contienen el último elemento de la consulta.  <br/> |
|**TotalItemsInView** <br/> |Representa el número total de elementos que pasan la restricción.  <br/> |
   
#### <a name="responseclass-attribute-values"></a>Valores de atributo ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|**Success** <br/> |Describe una solicitud que se ha cumplido.  <br/> |
|**Advertencia** <br/> | Describe una solicitud que no se ha procesado. Se puede devolver una advertencia si se produjo un error mientras se procesaba un elemento de la solicitud y no se pudieron procesar los elementos posteriores.<br/><br/> A continuación se muestran ejemplos de orígenes de advertencias:<br/>  <br/>- El Exchange está sin conexión durante el lote.  <br/>- Servicios de dominio de Active Directory (AD DS) está sin conexión.  <br/>- Los buzones se mueven.  <br/>- La base de datos de buzones de correo (MDB) está sin conexión.  <br/>- Una contraseña ha expirado.  <br/>- Se superó una cuota.  <br/> |
|**Error** <br/> | Describe una solicitud que no se puede cumplir.<br/><br/> A continuación se muestran ejemplos de orígenes de errores:  <br/><br/>- Atributos o elementos no válidos  <br/>- Atributos o elementos que están fuera del intervalo  <br/>- Una etiqueta desconocida  <br/>- Un atributo o elemento que no es válido en el contexto  <br/>- Un intento de acceso no autorizado por cualquier cliente  <br/>- Un error del lado servidor en respuesta a una llamada válida del lado cliente <br/> <br/>  Encontrará información sobre el error en los [elementos ResponseCode](responsecode.md) y [MessageText.](messagetext.md)  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona un código de error que identifica el error específico que encontró la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no se usa y está reservado para su uso futuro. Contiene un valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información adicional de respuesta a errores.  <br/> |
|[DLExpansion](dlexpansion.md) <br/> |Contiene una matriz de buzones que se encuentran en una lista de distribución.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contiene los mensajes de respuesta de una Exchange de servicios web.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que se ejecuta Exchange Server con el rol de servidor acceso de cliente instalado.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación ExpandDL](expanddl-operation.md)
- [Referencia EWS para Exchange](ews-reference-for-exchange.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

