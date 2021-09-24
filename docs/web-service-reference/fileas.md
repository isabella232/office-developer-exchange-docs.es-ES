---
title: FileAs
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FileAs
api_type:
- schema
ms.assetid: df50524e-471c-49d2-89fe-b2d0f61a1365
description: El elemento FileAs representa cómo se presenta una lista de contactos o distribución en la carpeta Contactos.
ms.openlocfilehash: 1ebed8365396feb42f4bfceac646ae7692dd6579
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530579"
---
# <a name="fileas"></a>FileAs

El **elemento FileAs** representa cómo se presenta una lista de contactos o distribución en la carpeta Contactos. 
  
```xml
<FileAs/>
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
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Contact](contact.md) <br/> |Representa un Exchange de contacto.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, se requiere un valor de texto que representa una cadena.
  
## <a name="remarks"></a>Comentarios

El **elemento FileAs** se usa para ordenar los contactos y las listas de distribución por un nombre que no sea un nombre completo o un nombre de empresa. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

