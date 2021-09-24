---
title: DLExpansion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DLExpansion
api_type:
- schema
ms.assetid: 9e50278d-fe6a-45e2-a72b-0fb06809e128
description: El elemento DLExpansion contiene una matriz de buzones que se encuentran en una lista de distribución.
ms.openlocfilehash: 7c214948b133ea2f30a47b2321c27b555b90e2fa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517213"
---
# <a name="dlexpansion"></a>DLExpansion

El **elemento DLExpansion** contiene una matriz de buzones que se encuentran en una lista de distribución. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**IndexedPagingOffset** <br/> |Representa el siguiente índice que se debe usar para la siguiente solicitud cuando se usa una vista de página indizada.  <br/> |
|**NumeratorOffset** <br/> |Representa el nuevo valor de numerador que se usará para la siguiente solicitud cuando se usan vistas de página de fracción.  <br/> |
|**AbsoluteDenominator** <br/> |Representa el siguiente denominador que se usará para la siguiente solicitud cuando se usan vistas de página de fracción.  <br/> |
|**IncludesLastItemInRange** <br/> |Indica si los resultados actuales contienen el último elemento de la consulta para que no se necesite paginación adicional.  <br/> |
|**TotalItemsInView** <br/> |Representa el número total de elementos de la vista.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Buzón](mailbox.md) <br/> |Identifica un objeto de servicio de directorio de Active Directory habilitado para correo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |Contiene el estado y el resultado de una única solicitud ExpandDL.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación ExpandDL](expanddl-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md) 
- [Referencia EWS para Exchange](ews-reference-for-exchange.md)

