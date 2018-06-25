---
title: agente
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
ms.openlocfilehash: 3895095ed4e469cdb9fec489ba6b6e228779a9c8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763344"
---
# <a name="agent"></a>agente
  
**Se aplica a:** Exchange Server 2013
  
El elemento de **agente** contiene información de configuración acerca de un agente instalado. 
  
- [configuración](configuration.md) 
- [mexRuntime](mexruntime.md)
- [agentList](agentlist.md)
- [agente](agent.md)
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |El nombre que se especificó cuando se ha instalado el agente. Este atributo requiere un valor de cadena no vacía que contiene un máximo de 64 caracteres.  <br/> |
|**baseType** <br/> |El nombre completo, incluido el espacio de nombres, de la clase desde la que se deriva el agente. Este atributo requiere un valor de cadena no vacía que contiene al menos un carácter.  <br/> |
|**classFactory** <br/> |El nombre completo, incluido el espacio de nombres, de la clase que implementa el generador de agentes que crea instancias del agente. Este atributo debe contener el nombre completo de la clase que implementa el generador de agentes que crea instancias del agente. Esta clase debe derivar de la clase de la [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) o [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) .  <br/> |
|**assemblyPath** <br/> |La ruta de acceso completa, incluido el nombre de archivo del ensamblado que contiene el código para el agente. Este atributo requiere un valor de cadena no vacía que contiene al menos un carácter.  <br/> |
|**habilitado** <br/> |Un valor booleano que indica si el agente está habilitado. El valor es **true** si está habilitado el agente; de lo contrario, el valor es **false**. Este atributo es necesario.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[agentList](agentlist.md) <br/> |Contiene un elemento de **agente** para cada agente instalado.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |Este archivo no define un espacio de nombres.  <br/> |
|Nombre de esquema  <br/> |No está disponible.  <br/> |
|Archivo de validación  <br/> |No está disponible.  <br/> |
|Puede estar vacío  <br/> |Falso.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos del archivo de configuración de los agentes para Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

