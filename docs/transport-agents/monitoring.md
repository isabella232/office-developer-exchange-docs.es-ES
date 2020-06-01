---
title: monitor
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
ms.openlocfilehash: 5614ac2c6428da9b6845769a9335486d3ded5754
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455831"
---
# <a name="monitoring"></a>monitor
  
**Se aplica a:** Exchange Server 2013
  
El elemento **Monitoring** contiene información de configuración que define cómo y cuándo el servicio de transporte front-end o el servicio de transporte supervisa los agentes que están instalados. 
  
- [configuración](configuration.md)  
- [mexRuntime](mexruntime.md)  
- [monitor](monitoring.md)
  
```XML
<monitoring>
   <agentExecution/>
   <messageSnapshot/>
</monitoring>
```

**monitoringType (complexType)**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[agentExecution](agentexecution.md) <br/> |Define el tiempo, en milisegundos, para el acceso de cliente o el servidor de buzones que se va a esperar a que un agente vuelva de un evento antes de escribir en el registro de eventos.  <br/> |
|[messageSnapshot](messagesnapshot.md) <br/> |Contiene un atributo que especifica si la característica de seguimiento de canalización está habilitada para el servidor de acceso de cliente o de buzones.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[mexRuntime](mexruntime.md) <br/> |Contiene elementos que definen la información de configuración para la supervisión de agentes y la información de configuración para SMTP y los agentes de enrutamiento que están instalados.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |Este archivo no define un espacio de nombres.  <br/> |
|Nombre de esquema  <br/> |No disponible.  <br/> |
|Archivo de validación  <br/> |No disponible.  <br/> |
|Puede estar vacío  <br/> |Falso.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos del archivo de configuración de agentes para Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

