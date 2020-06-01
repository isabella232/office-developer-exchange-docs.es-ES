---
title: agentExecution
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- agentExecution
api_type:
- schema
ms.assetid: 600c4690-941c-45af-a906-5528748d09cd
description: 'Última modificación: 17 de septiembre de 2015'
ms.openlocfilehash: 457257e59fb37659daf2f91b0fa5dfced5c48c03
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44446493"
---
# <a name="agentexecution"></a>agentExecution
  
**Se aplica a:** Exchange Server 2013 
  
El elemento **agentExecution** define el tiempo, en milisegundos, para que el servidor de acceso de cliente o de buzones de correo espere a que un agente vuelva de un evento antes de escribir en el registro de eventos. 
  
- [configuración](configuration.md)  
- [monitor](monitoring.md)
- [agentExecution](agentexecution.md)
  
```XML
<agentExecution timeLimitInMilliseconds="" />
```

**agentExecutionType (complexType)**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**timeLimitInMilliseconds** <br/> |Un valor entero positivo que especifica el tiempo en milisegundos que debe transcurrir para que el servidor espere a que un agente vuelva de un evento antes de escribir una advertencia en el registro de eventos. El rendimiento puede disminuir si este valor es demasiado pequeño. El valor sugerido para este atributo es 300.000, que equivale a 5 minutos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[monitor](monitoring.md) <br/> |Contiene información de configuración que define cómo y cuándo el servicio de transporte front-end o el servicio de transporte supervisa los agentes que están instalados.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |Este archivo no define un espacio de nombres.  <br/> |
|Nombre de esquema  <br/> |No disponible.  <br/> |
|Archivo de validación  <br/> |No disponible.  <br/> |
|Puede estar vacío  <br/> |Falso.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos del archivo de configuración de agentes para Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

