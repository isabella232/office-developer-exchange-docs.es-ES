---
title: agent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- agent
api_type:
- schema
ms.assetid: 0bf744a5-9d79-4c82-8ea7-45fdb3f55300
description: 'Last modified: September 17, 2015'
ms.openlocfilehash: 8bcfdd9bffd4c7a15af40528fd431a99c7868637
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520972"
---
# <a name="agent"></a>agent
  
**Se aplica a:** Exchange Server 2013
  
El **elemento agent** contiene información de configuración sobre un agente instalado. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**nombre** <br/> |Nombre que se especificó cuando se instaló el agente. Este atributo requiere un valor de cadena ninguno que contenga un máximo de 64 caracteres.  <br/> |
|**baseType** <br/> |Nombre completo, incluido el espacio de nombres, de la clase de la que deriva el agente. Este atributo requiere un valor de cadena ninguno que contenga al menos un carácter.  <br/> |
|**classFactory** <br/> |Nombre completo, incluido el espacio de nombres, de la clase que implementa la fábrica de agentes que crea instancias del agente. Este atributo debe contener el nombre completo de la clase que implementa la fábrica de agentes que crea instancias del agente. Esta clase debe derivar de la [clase SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) o [RoutingAgentFactory.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)  <br/> |
|**assemblyPath** <br/> |La ruta de acceso completa, incluido el nombre de archivo, del ensamblado que contiene el código del agente. Este atributo requiere un valor de cadena ninguno que contenga al menos un carácter.  <br/> |
|**enabled** <br/> |Valor booleano que indica si el agente está habilitado. El valor es **true** si el agente está habilitado; de lo contrario, el valor es **false**. Este atributo es obligatorio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[agentList](agentlist.md) <br/> |Contiene un **elemento agent** para cada agente instalado.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |Este archivo no define un espacio de nombres.  <br/> |
|Nombre de esquema  <br/> |No disponible.  <br/> |
|Archivo de validación  <br/> |No disponible.  <br/> |
|Puede estar vacío  <br/> |Falso.  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos de archivo de configuración de agentes para Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

