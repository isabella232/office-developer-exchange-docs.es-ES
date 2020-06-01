---
title: Atribución (PersonaAttributionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc59e17e-baea-4617-8ca1-4382a89de0d7
description: El elemento de atribución especifica una instancia en una matriz de atributos para un elemento PersonaType.
ms.openlocfilehash: 05b0d41c116f2ed7b8dbb3ac44108bb879256b5c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464178"
---
# <a name="attribution-personaattributiontype"></a>Atribución (PersonaAttributionType)

El elemento de **atribución** especifica una instancia en una matriz de atributos para un elemento **PersonaType** . 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ID (cadena)](id-string.md) <br/> |Especifica una cadena que identifica de forma única una aplicación o una atribución en un rol.  <br/> |
|[SourceId](sourceid.md) <br/> |Especifica el identificador del destinatario de contacto o de Active Directory.  <br/> |
|[DisplayName (cadena)](displayname-string.md) <br/> |Define el nombre para mostrar de una carpeta, un contacto, una lista de distribución, un usuario delegado o una regla.  <br/> |
|[IsWritable](iswritable.md) <br/> |Especifica si se puede escribir en el contacto subyacente o en el destinatario de Active Directory.  <br/> |
|[IsQuickContact](isquickcontact.md) <br/> |Especifica un valor booleano que indica si el contacto subyacente o el destinatario de Active Directory es un contacto rápido.  <br/> |
|[IsHidden](ishidden.md) <br/> |Contiene un valor booleano que indica si el contacto subyacente o el destinatario de Active Directory se deben ocultar o mostrar como parte del rol.  <br/> |
|[FolderId](folderid.md) <br/> |Contiene el identificador y la clave de cambio de una carpeta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Atribuciones (ArrayOfPersonaAttributionsType)](attributions-arrayofpersonaattributionstype.md) <br/> |Especifica una matriz de información de atribución de uno o varios de los contactos o de los destinatarios de Active Directory (AD) agregados al rol asociado.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

