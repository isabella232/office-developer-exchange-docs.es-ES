---
title: ViewPrivateItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ViewPrivateItems
api_type:
- schema
ms.assetid: 80b949ac-440c-4a01-b428-ebafb5b1b802
description: El elemento ViewPrivateItems indica si una aplicación de cliente o usuario delegado tiene permiso para ver elementos privados en el buzón de la entidad de seguridad.
ms.openlocfilehash: c35f24ae79e907424cb5cfb0efeec2307334ca12
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840970"
---
# <a name="viewprivateitems"></a>ViewPrivateItems

El elemento **ViewPrivateItems** indica si una aplicación de cliente o usuario delegado tiene permiso para ver elementos privados en el buzón de la entidad de seguridad. 
  
```XML
<ViewPrivateItems>true | false</ViewPrivateItems>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[UsuarioDelegado](delegateuser.md) <br/> |Identifica un único delegado para agregar o actualizar en un buzón de correo.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta. Este elemento es de sólo lectura.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de **true** indica que el delegado o el cliente puede ver elementos privados en el buzón de la entidad de seguridad. Un valor de **false** indica que los elementos privados no están visibles para un cliente o un delegado. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación AddDelegate](adddelegate-operation.md)
  
[Operación UpdateDelegate](updatedelegate-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


[Adición de delegados](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

