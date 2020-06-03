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
ms.openlocfilehash: 8a58444580c803efb7312df95d75d697bc42e8e0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461845"
---
# <a name="messagesnapshot"></a>messageSnapshot

**Se aplica a:** Exchange Server 2013
  
El elemento **messageSnapshot** contiene un atributo que especifica si la característica de seguimiento de canalización está habilitada para el servidor de Exchange que tiene instalado el rol de servidor acceso de cliente o buzón. 
  
- [configuración](configuration.md)  
- [mexRuntime](mexruntime.md) 
- [monitor](monitoring.md) 
- [messageSnapshot](messagesnapshot.md)
  
```XML
<messageSnapshot enabled="" />
```

**messageSnapshotType (Boolean)**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**enabled** <br/> |Un valor booleano que indica si la característica de seguimiento de canalización está habilitada para el servidor de acceso de cliente o de buzones. El valor es **true** si está habilitado el seguimiento de canalización; de lo contrario, el valor es **false** o el elemento no está presente.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[monitor](monitoring.md) <br/> |Contiene información de configuración que define cómo y cuándo el servicio de transporte supervisa los agentes que están instalados.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |Este archivo no define un espacio de nombres.  <br/> |
|Nombre de esquema  <br/> |No disponible.  <br/> |
|Archivo de validación  <br/> |No disponible.  <br/> |
|Puede estar vacío  <br/> |Falso.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos del archivo de configuración de agentes para Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

