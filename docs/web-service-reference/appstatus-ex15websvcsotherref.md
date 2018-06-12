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
ms.openlocfilehash: cf213fc3d7be02c411e9c2e83a4ff153dbefe098
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763543"
---
# <a name="appstatus"></a>AppStatus

El valor del elemento **AppStatus** indica el estado de la aplicación de correo. 
  
```XML
<AppStatus/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[Metadatos](metadata-ex15websvcsotherref.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **AppStatus** indica el estado de la aplicación de correo. Si el usuario puede corregir un problema relacionado con el estado de la aplicación de correo, el elemento [ActionUrl](actionurl.md) proporciona la dirección URL para realizar la corrección. 
  
**La tabla 1. Valores de AppStatus**

|**Valor**|**Descripción**|
|:-----|:-----|
|Null o 0  <br/> |La aplicación de correo tiene un estado correcto.  <br/> |
|1.0  <br/> |No se pudo actualizar automáticamente la aplicación de correo. La aplicación de correo debe estar instalado volver a desde el almacén de Office.  <br/> |
|1.1  <br/> |No se pudo actualizar automáticamente la aplicación de correo. La aplicación de correo requiere permisos mayor, y esto requiere la revisión y la confirmación para instalar.  <br/> |
|1.2  <br/> |La aplicación de correo no se ha podido actualizarse automáticamente. La licencia actual ha expirado o no es válida. Por favor, actualice la aplicación de correo desde la tienda de Office.  <br/> |
|2.0  <br/> |No se pudo actualizar automáticamente la licencia de la aplicación de correo. Se necesita la licencia para la aplicación de correo que se va a recuperar de la tienda Office.  <br/> |
|2.1  <br/> |No se pudo actualizar automáticamente la licencia de la aplicación de correo. La licencia actual ha caducado. Una nueva licencia para esta aplicación debe instalarse desde la tienda de Office.  <br/> |
|3.0  <br/> |Ha cambiado el estado del almacén de Office para la aplicación de correo. Esto puede indicar que hay un problema con la aplicación de correo. Vaya a la página de la aplicación de correo en la tienda de Office para obtener más información.  <br/> |
|3.1  <br/> |La aplicación de correo se ha quitado de la tienda de Office.  <br/> |
|3.2  <br/> |Se ha detectado un problema con la aplicación de correo y temporalmente haya sido retirado de la tienda Office.  <br/> |
|3.3  <br/> |La aplicación de correo se quitarán de la tienda Office dentro de 30 días.  <br/> |
|4.0  <br/> |La aplicación de correo está deshabilitada automáticamente por el cliente de correo.  <br/> |
|4.1  <br/> |La aplicación de correo está deshabilitada por Outlook por motivos de rendimiento.  <br/> |
   
## <a name="remarks"></a>Notas

Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> | http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |No disponible  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Metadatos](metadata-ex15websvcsotherref.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

