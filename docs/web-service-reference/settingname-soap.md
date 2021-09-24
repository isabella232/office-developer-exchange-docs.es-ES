---
title: SettingName (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 8bcb0411-58b0-4e37-b97e-00c07dcbecb1
description: El elemento SettingName representa el nombre de una configuración de la respuesta.
ms.openlocfilehash: 1a676f55ad86496ae8bdbdfbeaeb9827b1aa6646
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531884"
---
# <a name="settingname-soap"></a>SettingName (SOAP)

El **elemento SettingName** representa el nombre de una configuración de la respuesta. 
  
```XML
<SettingName/>
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
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |Representa un error que se devuelve al recuperar una configuración de usuario.  <br/> |
|[DomainSettingError (SOAP)](domainsettingerror-soap.md) <br/> |Representa un error que se produjo al recuperar una configuración de dominio. Esto representa un error de una **solicitud GetDomainSettings.**  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor del **elemento SettingName** representa el nombre de una configuración en una respuesta. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   

