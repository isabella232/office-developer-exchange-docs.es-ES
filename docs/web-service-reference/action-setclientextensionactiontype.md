---
title: Acción (SetClientExtensionActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5624a87-3436-40ce-8d6b-cc01eecab64d
description: El elemento Action contiene la acción que el servidor Exchange debe realizar en una aplicación.
ms.openlocfilehash: 29579e26377edacb5fb0bb8406144eeb116b8d15
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529689"
---
# <a name="action-setclientextensionactiontype"></a>Acción (SetClientExtensionActionType)

El elemento **Action** contiene la acción que el servidor Exchange debe realizar en una aplicación. 
  
```XML
<Action ActionId="" ExtensionId="">
   <ClientExtension/>
</Action>
```

 **SetClientExtensionActionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|ActionId  <br/> |Especifica el identificador de la acción. Este atributo es obligatorio.  <br/> |
|ExtensionId  <br/> |Especifica el identificador de la extensión. Este atributo es opcional.  <br/> |
   
#### <a name="actionid"></a>ActionId

|**Valor**|**Descripción**|
|:-----|:-----|
|Configurar  <br/> |Indica una acción de configuración.  <br/> |
|Instalar  <br/> |Indica una acción de instalación.  <br/> |
|Uninstall  <br/> |Indica una acción de desinstalación.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ClientExtension](clientextension.md) <br/> |Contiene la información de usuario y configuración de una aplicación.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Acciones (ArrayOfSetClientExtensionActionsType)](actions-arrayofsetclientextensionactionstype.md) <br/> |Especifica una matriz de elementos **Action** .  <br/> |
   
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

