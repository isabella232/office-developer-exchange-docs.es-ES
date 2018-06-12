---
title: Atribución (PersonaAttributionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc59e17e-baea-4617-8ca1-4382a89de0d7
description: El elemento de atribución especifica una instancia de una matriz de atributos para un elemento PersonaType.
ms.openlocfilehash: 0e800c92c75bf0c475d4bffd33d6ab49f9ad9a9a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763581"
---
# <a name="attribution-personaattributiontype"></a>Atribución (PersonaAttributionType)

El elemento de **atribución** especifica una instancia de una matriz de atributos para un elemento **PersonaType** . 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Identificador (cadena)](id-string.md) <br/> |Especifica una cadena que identifica de forma exclusiva una aplicación o una atribución en un rol.  <br/> |
|[SourceId](sourceid.md) <br/> |Especifica el identificador del contacto o destinatario de Active Directory.  <br/> |
|[DisplayName (cadena)](displayname-string.md) <br/> |Define el nombre para mostrar de una carpeta, contacto, lista de distribución, usuario delegado o regla.  <br/> |
|[IsWritable](iswritable.md) <br/> |Especifica si se puede escribir en el contacto subyacente o el destinatario de Active Directory.  <br/> |
|[IsQuickContact](isquickcontact.md) <br/> |Especifica un valor booleano que indica si el contacto subyacente o el destinatario de Active Directory es un contacto rápido.  <br/> |
|[IsHidden](ishidden.md) <br/> |Contiene un valor booleano que indica si el contacto subyacente o el destinatario de Active Directory debe ser oculto o que se muestra como parte del rol.  <br/> |
|[FolderId](folderid.md) <br/> |Contiene el identificador y cambiar la clave de una carpeta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Atribuciones (ArrayOfPersonaAttributionsType)](attributions-arrayofpersonaattributionstype.md) <br/> |Especifica una matriz de información de atribución para uno o varios de los contactos o los destinatarios de active directory (AD) agregados a la persona asociada.  <br/> |
   
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

