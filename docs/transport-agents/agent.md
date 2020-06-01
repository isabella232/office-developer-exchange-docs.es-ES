---
title: Representante
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- agent
api_type:
- schema
ms.assetid: 0bf744a5-9d79-4c82-8ea7-45fdb3f55300
description: 'Última modificación: 17 de septiembre de 2015'
ms.openlocfilehash: a810bb229015054e0f244773760235114655a982
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455684"
---
# <a name="agent"></a>Representante
  
**Se aplica a:** Exchange Server 2013
  
El elemento **Agent** contiene información de configuración sobre un agente instalado. 
  
- [configuración](configuration.md) 
- [mexRuntime](mexruntime.md)
- [agentList](agentlist.md)
- [Representante](agent.md)
  
```XML
<agent
        name=""
        baseType=""
        classFactory=""
        assemblyPath=""
        enabled="" />
</agent>
```

**agentType (complexType)**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre que se especificó cuando se instaló el agente. Este atributo requiere un valor de cadena no vacío que contenga un máximo de 64 caracteres.  <br/> |
|**baseType** <br/> |Nombre completo, incluido el espacio de nombres, de la clase de la que se deriva el agente. Este atributo requiere un valor de cadena no vacío que contenga al menos un carácter.  <br/> |
|**classFactory** <br/> |El nombre completo, incluido el espacio de nombres, de la clase que implementa el generador del agente que crea instancias del agente. Este atributo debe contener el nombre completo de la clase que implementa el generador del agente que crea instancias del agente. Esta clase debe derivarse de la clase [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) o [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) .  <br/> |
|**assemblyPath** <br/> |La ruta de acceso completa, incluido el nombre de archivo, del ensamblado que contiene el código para el agente. Este atributo requiere un valor de cadena no vacío que contenga al menos un carácter.  <br/> |
|**enabled** <br/> |Un valor booleano que indica si está habilitado el agente. El valor es **true** si el agente está habilitado; de lo contrario, el valor es **false**. Este atributo es obligatorio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[agentList](agentlist.md) <br/> |Contiene un elemento **Agent** para cada agente instalado.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |Este archivo no define un espacio de nombres.  <br/> |
|Nombre de esquema  <br/> |No disponible.  <br/> |
|Archivo de validación  <br/> |No disponible.  <br/> |
|Puede estar vacío  <br/> |Falso.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos del archivo de configuración de agentes para Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

