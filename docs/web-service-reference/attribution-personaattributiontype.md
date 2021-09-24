---
title: Attribution (PersonaAttributionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: dc59e17e-baea-4617-8ca1-4382a89de0d7
description: El elemento Atribución especifica una instancia en una matriz de atributos para un elemento PersonaType.
ms.openlocfilehash: eb2fe66042b6c7f52732be20195f0f4b94ab867c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524381"
---
# <a name="attribution-personaattributiontype"></a>Attribution (PersonaAttributionType)

El **elemento Atribución** especifica una instancia en una matriz de atributos para un **elemento PersonaType.** 
  
```XML
<Attribution>
    <Id></Id>
    <SourceId></SourceId>
    <DisplayName></DisplayName>
    <IsWritable></IsWritable>
    <IsQuickContact></IsQuickContact>
    <IsHidden></IsHidden>
    <FolderId></FolderId>
</Attribution>
```

 **PersonaAttributionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ID (Cadena)](id-string.md) <br/> |Especifica una cadena que identifica de forma única una aplicación o una atribución en una persona.  <br/> |
|[SourceId](sourceid.md) <br/> |Especifica el identificador del contacto o del destinatario de Active Directory.  <br/> |
|[DisplayName (cadena)](displayname-string.md) <br/> |Define el nombre para mostrar de una carpeta, contacto, lista de distribución, usuario delegado o regla.  <br/> |
|[IsWritable](iswritable.md) <br/> |Especifica si se puede escribir el contacto subyacente o el destinatario de Active Directory.  <br/> |
|[IsQuickContact](isquickcontact.md) <br/> |Especifica un valor booleano que indica si el contacto subyacente o el destinatario de Active Directory es un contacto rápido.  <br/> |
|[IsHidden](ishidden.md) <br/> |Contiene un valor booleano que indica si el contacto subyacente o el destinatario de Active Directory deben ocultarse o mostrarse como parte de la persona.  <br/> |
|[FolderId](folderid.md) <br/> |Contiene el identificador y la clave de cambio de una carpeta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Attributions (ArrayOfPersonaAttributionsType)](attributions-arrayofpersonaattributionstype.md) <br/> |Especifica una matriz de información de atribución para uno o varios de los contactos o destinatarios de Active Directory (AD) agregados a la persona asociada.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

