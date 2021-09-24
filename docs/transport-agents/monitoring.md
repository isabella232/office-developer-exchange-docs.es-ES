---
title: monitoring
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- monitoring
api_type:
- schema
ms.assetid: 350d7b46-9260-41a7-8613-3cb8cc1b29a5
description: 'Last modified: September 17, 2015'
ms.openlocfilehash: 215737fb43e1dbef9b7dd11baea1d3f922df7d34
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540372"
---
# <a name="monitoring"></a>monitoring
  
**Se aplica a:** Exchange Server 2013
  
El **elemento de** supervisión contiene información de configuración que define cómo y cuándo el servicio de transporte front-end o el servicio de transporte supervisan los agentes que están instalados. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[agentExecution](agentexecution.md) <br/> |Define el tiempo, en milisegundos, para que el acceso de cliente o el servidor de buzones de correo esperen a que un agente vuelva de un evento antes de escribir en el registro de eventos.  <br/> |
|[messageSnapshot](messagesnapshot.md) <br/> |Contiene un atributo que especifica si la característica de seguimiento de canalización está habilitada para el acceso de cliente o el servidor de buzones de correo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[mexRuntime](mexruntime.md) <br/> |Contiene elementos que definen la información de configuración para la supervisión de agentes y la información de configuración para smtp y agentes de enrutamiento que están instalados.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |Este archivo no define un espacio de nombres.  <br/> |
|Nombre de esquema  <br/> |No disponible.  <br/> |
|Archivo de validación  <br/> |No disponible.  <br/> |
|Puede estar vacío  <br/> |Falso.  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos de archivo de configuración de agentes para Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

