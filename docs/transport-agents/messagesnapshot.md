---
title: messageSnapshot
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- messageSnapshot
api_type:
- schema
ms.assetid: f157e44c-b950-463f-b086-31d5da94b7ff
description: 'Última modificación: 17 de septiembre de 2015'
ms.openlocfilehash: 4b814def8eef8fb452d2e754c5f6787d644055f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763372"
---
# <a name="messagesnapshot"></a>messageSnapshot

**Se aplica a:** Exchange Server 2013
  
El elemento **messageSnapshot** contiene un atributo que especifica si está habilitada la característica de seguimiento de canalización para el servidor de Exchange que tiene el acceso de cliente o el rol de servidor de buzón de correo instalado. 
  
- [configuración](configuration.md)  
- [mexRuntime](mexruntime.md) 
- [supervisión](monitoring.md) 
- [messageSnapshot](messagesnapshot.md)
  
```XML
<messageSnapshot enabled="" />
```

**messageSnapshotType (booleano)**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**habilitado** <br/> |Un valor booleano que indica si está habilitada la característica de seguimiento de canalización para el acceso de cliente o el servidor de buzones. El valor es **true** si está habilitado el seguimiento de canalización; de lo contrario, el valor es **false** o el elemento no está presente.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[supervisión](monitoring.md) <br/> |Contiene información de configuración que define cómo y cuándo el servicio de transporte supervisa a los agentes que se instalan.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |Este archivo no define un espacio de nombres.  <br/> |
|Nombre de esquema  <br/> |No está disponible.  <br/> |
|Archivo de validación  <br/> |No está disponible.  <br/> |
|Puede estar vacío  <br/> |Falso.  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos del archivo de configuración de los agentes para Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

