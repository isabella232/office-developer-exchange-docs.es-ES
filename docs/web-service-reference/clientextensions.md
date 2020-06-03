---
title: ClientExtensions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0073d195-75fd-4c89-97e0-2ad6d91f99f9
description: El elemento ClientExtensions contiene una matriz de información de usuario y configuración acerca de las aplicaciones.
ms.openlocfilehash: 016b4c910f3c21a20d72b926a1c568925aa9d37e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461460"
---
# <a name="clientextensions"></a>ClientExtensions

El elemento **ClientExtensions** contiene una matriz de información de usuario y configuración acerca de las aplicaciones. 
  
```XML
<ClientExtensions>
   <ClientExtension/>
</ClientExtensions>
```

 **ArrayOfClientExtensionsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ClientExtension](clientextension.md) <br/> |Contiene la información de usuario y configuración de una aplicación.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetClientExtensionResponse](getclientextensionresponse.md) <br/> |Representa una respuesta para obtener la información de configuración de una aplicación.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

||
|:-----|
|Namespace  <br/> |
|Nombre de esquema  <br/> |
|Archivo de validación  <br/> |
|Puede estar vacío  <br/> |
   

