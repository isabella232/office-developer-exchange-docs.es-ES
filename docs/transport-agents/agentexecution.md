---
title: agentExecution
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- agentExecution
api_type:
- schema
ms.assetid: 600c4690-941c-45af-a906-5528748d09cd
description: 'Last modified: September 17, 2015'
ms.openlocfilehash: 04a53e2698c66326943bcd083c775b53f5c6d5d5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513062"
---
# <a name="agentexecution"></a>agentExecution
  
**Se aplica a:** Exchange Server 2013 
  
El **elemento agentExecution** define el tiempo, en milisegundos, para que el servidor de acceso de cliente o buzón espere a que un agente vuelva de un evento antes de escribir en el registro de eventos. 
  
- [configuración](configuration.md)  
- [supervisión](monitoring.md)
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
|**timeLimitInMilliseconds** <br/> |Valor entero positivo que especifica el tiempo, en milisegundos, para que el servidor espere a que un agente vuelva de un evento antes de escribir una advertencia en el registro de eventos. El rendimiento puede disminuir si este valor es demasiado pequeño. El valor sugerido para este atributo es 300.000, lo que equivale a 5 minutos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[supervisión](monitoring.md) <br/> |Contiene información de configuración que define cómo y cuándo el servicio de transporte front-end o el servicio de transporte supervisan los agentes que están instalados.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |Este archivo no define un espacio de nombres.  <br/> |
|Nombre de esquema  <br/> |No disponible.  <br/> |
|Archivo de validación  <br/> |No disponible.  <br/> |
|Puede estar vacío  <br/> |Falso.  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos de archivo de configuración de agentes para Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

