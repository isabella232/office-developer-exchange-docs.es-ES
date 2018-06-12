---
title: Cadena
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- String
api_type:
- schema
ms.assetid: e6e362b1-4526-49e1-b283-1c4bc4295874
description: El elemento de cadena representa una cadena que se usa en los elementos, contactos, tareas y las conversaciones.
ms.openlocfilehash: 66260c7ebcb56049a78c5eddbe057dfa8d61f193
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837607"
---
# <a name="string"></a>Cadena

El elemento de **cadena** representa una cadena que se usa en los elementos, contactos, tareas y las conversaciones. 
  
```XML
<String/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Categories](categories-ex15websvcsotherref.md) <br/> |Contiene una colección de cadenas que identifican a qué categorías pertenece un elemento en el buzón de correo.  <br/> |
|[Niños](children.md) <br/> |Contiene los nombres de los elementos secundarios de un contacto.  <br/> |
|[Empresas](companies.md) <br/> |Representa la colección de las empresas que están asociados con un contacto o una tarea.  <br/> |
|[Contacts](contacts-ex15websvcsotherref.md) <br/> |Contiene una lista de contactos que están asociados con una tarea.  <br/> |
|[GlobalCategories](globalcategories.md) <br/> |Contiene la lista de categorías para todos los elementos de la conversación en un buzón de correo.  <br/> |
|[GlobalUniqueRecipients](globaluniquerecipients.md) <br/> |Contiene la lista de destinatarios de una conversación agregada a través de un buzón de correo.  <br/> |
|[GlobalUniqueSenders](globaluniquesenders.md) <br/> |Contiene una lista de todos los remitentes de los elementos de la conversación en el buzón de correo.  <br/> |
|[GlobalUniqueUnreadSenders](globaluniqueunreadsenders.md) <br/> |Contiene una lista de todas las personas que han enviado los mensajes que están actualmente no leídos en esta conversación a través de todas las carpetas del buzón de correo.  <br/> |
|[ItemClasses](itemclasses.md) <br/> |Contiene una lista de las clases de elemento deben estar marcados en los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[MessageClassifications](messageclassifications.md) <br/> |Contiene una lista de las clasificaciones de mensajes deben estar marcados en los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.  <br/> |
|[UniqueRecipients](uniquerecipients.md) <br/> |Contiene la lista de destinatarios de la conversación. Este elemento es de sólo lectura.  <br/> |
|[UniqueSenders](uniquesenders.md) <br/> |Contiene una lista de todos los remitentes de los elementos de una conversación en la carpeta actual. Este elemento es de sólo lectura.  <br/> |
|[UniqueUnreadSenders](uniqueunreadsenders.md) <br/> |Contiene una lista de todas las personas que han enviado los mensajes que están actualmente no leídos en esta conversación en la carpeta actual.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto de este elemento es una cadena que representa una categoría, el elemento secundario de un contacto, una empresa, un destinatario único de una conversación o a un contacto que está asociado con una tarea.
  
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación de FindConversation](findconversation-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

