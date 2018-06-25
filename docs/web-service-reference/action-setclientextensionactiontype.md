---
title: Acción (SetClientExtensionActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5624a87-3436-40ce-8d6b-cc01eecab64d
description: El elemento de acción contiene la acción que debe realizar el servidor de Exchange en una aplicación.
ms.openlocfilehash: a231cedfa6e4759dabfcbecfbe9a9b851f834247
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763389"
---
# <a name="action-setclientextensionactiontype"></a>Acción (SetClientExtensionActionType)

El elemento de **acción** contiene la acción que debe realizar el servidor de Exchange en una aplicación. 
  
```XML
<Action ActionId="" ExtensionId="">
   <ClientExtension/>
</Action>
```

 **SetClientExtensionActionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|ActionId  <br/> |Especifica el identificador de la acción. Este atributo es necesario.  <br/> |
|ExtensionId  <br/> |Especifica el identificador de la extensión. Este atributo es opcional.  <br/> |
   
#### <a name="actionid"></a>ActionId

|**Valor**|**Descripción**|
|:-----|:-----|
|Configurar  <br/> |Indica una acción de configuración.  <br/> |
|Instalar  <br/> |Indica una acción de instalación.  <br/> |
|Desinstalar  <br/> |Indica una acción de desinstalación.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ClientExtension](clientextension.md) <br/> |Contiene información de usuario y de configuración sobre una aplicación.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Acciones (ArrayOfSetClientExtensionActionsType)](actions-arrayofsetclientextensionactionstype.md) <br/> |Especifica una matriz de elementos de **acción** .  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

