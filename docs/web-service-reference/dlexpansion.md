---
title: DLExpansion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DLExpansion
api_type:
- schema
ms.assetid: 9e50278d-fe6a-45e2-a72b-0fb06809e128
description: El elemento DLExpansion contiene una matriz de los buzones de correo que están contenidos en una lista de distribución.
ms.openlocfilehash: 06081b4aba761a7137f921b3bc1c8d6b2afab88c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764257"
---
# <a name="dlexpansion"></a>DLExpansion

El elemento **DLExpansion** contiene una matriz de los buzones de correo que están contenidos en una lista de distribución. 
  
- [ExpandDLResponse](expanddlresponse.md) 
- [ResponseMessages](responsemessages.md) 
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
- [DLExpansion](dlexpansion.md)
  
```xml
<DLExpansion AbsoluteDenominator"" IncludesLastItemInRange="" IndexedPagingOffset="" NumeratorOffset="" TotalItemsInView="">
   <Mailbox/>
</DLExpansion>
```

 **ArrayOfDLExpansionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**IndexedPagingOffset** <br/> |Representa el siguiente índice que se debe usar para la solicitud siguiente cuando se usa una vista de página indizados.  <br/> |
|**NumeratorOffset** <br/> |Representa el nuevo valor: número que se usará para la solicitud siguiente cuando se utilizan vistas de página de fracción.  <br/> |
|**AbsoluteDenominator** <br/> |Representa el denominador siguiente para usar para la solicitud siguiente cuando se utilizan vistas de página de fracción.  <br/> |
|**IncludesLastItemInRange** <br/> |Indica si los resultados actuales contienen el último elemento de la consulta de modo que no es necesaria la paginación adicional.  <br/> |
|**TotalItemsInView** <br/> |Representa el número total de elementos en la vista.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Buzón de correo](mailbox.md) <br/> |Identifica un objeto de servicio de directorio de Active Directory habilitados para correo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud ExpandDL.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación de ExpandDL](expanddl-operation.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md) 
- [Referencia EWS para Exchange](ews-reference-for-exchange.md)

