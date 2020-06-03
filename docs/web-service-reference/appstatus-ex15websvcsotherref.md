---
title: AppStatus
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f3ab8bf1-abc5-45cf-a2e1-d7602f2c24ec
description: El valor del elemento AppStatus indica el estado de la aplicación de correo.
ms.openlocfilehash: d833947fd62d500418f257829d241a2e0b3bca9c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464780"
---
# <a name="appstatus"></a>AppStatus

El valor del elemento **AppStatus** indica el estado de la aplicación de correo. 
  
```XML
<AppStatus/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[Metadatos](metadata-ex15websvcsotherref.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **AppStatus** indica el estado de la aplicación de correo. Si el usuario puede corregir un problema relacionado con el estado de la aplicación de correo, el elemento [ActionUrl](actionurl.md) proporciona la dirección URL para realizar la corrección. 
  
**Tabla 1. Valores de AppStatus**

|**Valor**|**Descripción**|
|:-----|:-----|
|Null o 0  <br/> |La aplicación de correo tiene un estado correcto.  <br/> |
|1.0  <br/> |La aplicación de correo no se pudo actualizar automáticamente. La aplicación de correo debe volver a instalarse desde la tienda Office.  <br/> |
|1.1  <br/> |La aplicación de correo no se pudo actualizar automáticamente. La aplicación de correo requiere mayor cantidad de permisos y esto requiere la revisión y la confirmación de la instalación.  <br/> |
|1.2  <br/> |La aplicación de correo no se pudo actualizar automáticamente. La licencia actual ha expirado o no es válida. Actualice la aplicación de correo desde la tienda Office.  <br/> |
|2.0  <br/> |La licencia de la aplicación de correo no se pudo actualizar automáticamente. La licencia de la aplicación de correo debe recuperarse de la tienda Office.  <br/> |
|2.1  <br/> |La licencia de la aplicación de correo no se pudo actualizar automáticamente. La licencia actual ha expirado. Se debe instalar una nueva licencia para esta aplicación desde la tienda Office.  <br/> |
|3,0  <br/> |El estado de la tienda Office de la aplicación de correo ha cambiado. Esto puede indicar que hay un problema con la aplicación de correo. Vaya a la página de la aplicación de correo en la tienda Office para obtener más información.  <br/> |
|3.1  <br/> |La aplicación de correo se ha quitado de la tienda Office.  <br/> |
|3.2  <br/> |Se ha detectado un problema con la aplicación de correo y se ha retirado temporalmente de la tienda Office.  <br/> |
|3.3  <br/> |La aplicación de correo se quitará de la tienda Office en un plazo de 30 días.  <br/> |
|4,0  <br/> |El cliente de correo ha deshabilitado automáticamente la aplicación de correo.  <br/> |
|4.1  <br/> |Outlook ha deshabilitado la aplicación de correo por motivos de rendimiento.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> | https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |No aplicable  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Metadatos](metadata-ex15websvcsotherref.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

