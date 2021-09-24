---
title: HomePage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HomePage
api_type:
- schema
ms.assetid: eec2c41e-a975-42f6-8150-caf8c6e26462
description: El elemento HomePage especifica la dirección URL que será la página principal predeterminada de la carpeta administrada.
ms.openlocfilehash: 32b943570802b440c347abcf8ffdf4ff675c92b0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541171"
---
# <a name="homepage"></a>HomePage

El **elemento HomePage** especifica la dirección URL que será la página principal predeterminada de la carpeta administrada. 
  
```xml
<HomePage/>
```

 **String**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |Contiene información sobre una carpeta administrada.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto es un valor de cadena que representa una dirección URL.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación CreateManagedFolder](createmanagedfolder-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Agregar carpetas administradas](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

