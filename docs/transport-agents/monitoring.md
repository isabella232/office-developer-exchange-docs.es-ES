---
title: supervisión
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- monitoring
api_type:
- schema
ms.assetid: 350d7b46-9260-41a7-8613-3cb8cc1b29a5
description: 'Última modificación: 17 de septiembre de 2015'
ms.openlocfilehash: 1b5484467def0bf3d22ba0707357977d5ed461ff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763371"
---
# <a name="monitoring"></a>supervisión
  
**Se aplica a:** Exchange Server 2013
  
El elemento de **supervisión** contiene información de configuración que define cómo y cuándo el servicio de transporte de Front-End o el servicio de transporte supervisa a los agentes que se instalan. 
  
- [configuración](configuration.md)  
- [mexRuntime](mexruntime.md)  
- [supervisión](monitoring.md)
  
```XML
<monitoring>
   <agentExecution/>
   <messageSnapshot/>
</monitoring>
```

**monitoringType (complexType)**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[agentExecution](agentexecution.md) <br/> |Define el tiempo, en milisegundos, para el acceso de cliente o el servidor de buzones que hay que esperar un agente devolver desde un evento antes de que escribe en el registro de eventos.  <br/> |
|[messageSnapshot](messagesnapshot.md) <br/> |Contiene un atributo que especifica si está habilitada la característica de seguimiento de canalización para el acceso de cliente o el servidor de buzones.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[mexRuntime](mexruntime.md) <br/> |Contiene elementos que definen la información de configuración de supervisión del agente y la información de configuración de SMTP y agentes de enrutamiento que se instalan.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |Este archivo no define un espacio de nombres.  <br/> |
|Nombre de esquema  <br/> |No está disponible.  <br/> |
|Archivo de validación  <br/> |No está disponible.  <br/> |
|Puede estar vacío  <br/> |Falso.  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos del archivo de configuración de los agentes para Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

