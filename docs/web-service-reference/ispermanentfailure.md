---
title: IsPermanentFailure
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 18dc3a97-cc0a-4092-934e-a6e86f52e668
description: El elemento IsPermanentFailure indica si un intento anterior de indizar el elemento no tuvo éxito.
ms.openlocfilehash: e5ed20de3c3de9c39d1487e3177c1b6ec358d990
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59532729"
---
# <a name="ispermanentfailure"></a>IsPermanentFailure

El **elemento IsPermanentFailure** indica si un intento anterior de indizar el elemento no tuvo éxito. 
  
```XML
<IsPermanentFailure>true | false</IsPermanentFailure>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[NonIndexableItemDetail](nonindexableitemdetail.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el elemento **IsPermanentFailure** indica que un intento anterior de indizar el elemento de buzón no se ha hecho correctamente. Un valor de **false** indica que un intento anterior de indizar el elemento de buzón se ha realizado correctamente. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

