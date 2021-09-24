---
title: messageSnapshot
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- messageSnapshot
api_type:
- schema
ms.assetid: f157e44c-b950-463f-b086-31d5da94b7ff
description: 'Last modified: September 17, 2015'
ms.openlocfilehash: 2ac38dd3f50b5d9d070262f3daffb72b02df5d82
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525459"
---
# <a name="messagesnapshot"></a>messageSnapshot

**Se aplica a:** Exchange Server 2013
  
El **elemento messageSnapshot** contiene un atributo que especifica si la característica de seguimiento de canalización está habilitada para el servidor Exchange que tiene instalado el acceso de cliente o el rol de servidor Buzón de correo. 
  
- [configuración](configuration.md)  
- [mexRuntime](mexruntime.md) 
- [supervisión](monitoring.md) 
- [messageSnapshot](messagesnapshot.md)
  
```XML
<messageSnapshot enabled="" />
```

**messageSnapshotType (booleano)**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**enabled** <br/> |Valor booleano que indica si la característica de seguimiento de canalización está habilitada para el acceso de cliente o el servidor de buzones de correo. El valor es **true si** el seguimiento de canalización está habilitado; de lo contrario, el valor es **false** o el elemento no está presente.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[supervisión](monitoring.md) <br/> |Contiene información de configuración que define cómo y cuándo el servicio de transporte supervisa los agentes que están instalados.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |Este archivo no define un espacio de nombres.  <br/> |
|Nombre de esquema  <br/> |No disponible.  <br/> |
|Archivo de validación  <br/> |No disponible.  <br/> |
|Puede estar vacío  <br/> |Falso.  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos de archivo de configuración de agentes para Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

