---
title: Cadena
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- String
api_type:
- schema
ms.assetid: e6e362b1-4526-49e1-b283-1c4bc4295874
description: El elemento String representa una cadena que usan elementos, contactos, tareas y conversaciones.
ms.openlocfilehash: dd85cae34ddf829f00660c8b87feb9331505183c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509297"
---
# <a name="string"></a>Cadena

El **elemento String** representa una cadena que usan elementos, contactos, tareas y conversaciones. 
  
```XML
<String/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Categories](categories-ex15websvcsotherref.md) <br/> |Contiene una colección de cadenas que identifican a qué categorías pertenece un elemento del buzón.  <br/> |
|[Niños](children.md) <br/> |Contiene los nombres de los elementos secundarios de un contacto.  <br/> |
|[Companies](companies.md) <br/> |Representa la colección de empresas asociadas a un contacto o tarea.  <br/> |
|[Contactos](contacts-ex15websvcsotherref.md) <br/> |Contiene una lista de contactos asociados a una tarea.  <br/> |
|[GlobalCategories](globalcategories.md) <br/> |Contiene la lista de categorías de todos los elementos de conversación de un buzón.  <br/> |
|[GlobalUniqueRecipients](globaluniquerecipients.md) <br/> |Contiene la lista de destinatarios de una conversación agregada en un buzón.  <br/> |
|[GlobalUniqueSenders](globaluniquesenders.md) <br/> |Contiene una lista de todos los remitentes de elementos de conversación en el buzón.  <br/> |
|[GlobalUniqueUnreadSenders](globaluniqueunreadsenders.md) <br/> |Contiene una lista de todas las personas que han enviado mensajes que actualmente no están leídos en esta conversación en todas las carpetas del buzón.  <br/> |
|[ItemClasses](itemclasses.md) <br/> |Contiene una lista de las clases de elementos que se deben marcar en los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[MessageClassifications](messageclassifications.md) <br/> |Contiene una lista de las clasificaciones de mensajes que deben marcarse en los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
|[UniqueRecipients](uniquerecipients.md) <br/> |Contiene la lista de destinatarios de la conversación. Este elemento es de solo lectura.  <br/> |
|[UniqueSenders](uniquesenders.md) <br/> |Contiene una lista de todos los remitentes de elementos de conversación de la carpeta actual. Este elemento es de solo lectura.  <br/> |
|[UniqueUnreadSenders](uniqueunreadsenders.md) <br/> |Contiene una lista de todas las personas que han enviado mensajes que actualmente no están leídos en esta conversación en la carpeta actual.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto de este elemento es una cadena que representa una categoría, el elemento secundario de un contacto, una empresa, un destinatario único de una conversación o un contacto asociado a una tarea.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Web Services.Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindConversation](findconversation-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

