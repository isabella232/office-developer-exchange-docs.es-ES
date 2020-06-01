---
title: Atribuciones (ArrayOfPersonaAttributionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61d843c-bca5-4c88-9667-fd03d2a963a1
description: El elemento atribuciones especifica una matriz de información de atribución de uno o varios de los contactos o de los destinatarios de Active Directory agregados al rol asociado.
ms.openlocfilehash: a9883e06a8adbd5c9d3bc7e1edd28c62418df653
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460326"
---
# <a name="attributions-arrayofpersonaattributionstype"></a>Atribuciones (ArrayOfPersonaAttributionsType)

El elemento **atribuciones** especifica una matriz de información de atribución de uno o varios de los contactos o de los destinatarios de Active Directory agregados al rol asociado. 
  
```XML
<Attributions>
    <Attribution></Attribution>
</Attributions>
```

 **ArrayOfPersonaAttributionsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Atribución (PersonaAttributionType)](attribution-personaattributiontype.md) <br/> |Especifica una instancia de una matriz de atributos para un elemento **PersonaType** .  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Rol](persona.md) <br/> |Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .  <br/> |
   
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

