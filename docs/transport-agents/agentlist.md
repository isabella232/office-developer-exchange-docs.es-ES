---
title: agentList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- agentList
api_type:
- schema
ms.assetid: e877b7ef-e303-4270-964d-8d116ff2a865
description: 'Last modified: September 17, 2015'
ms.openlocfilehash: eadae2a22e4c844f1f2edce9211100bb9ef2776d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529359"
---
# <a name="agentlist"></a>agentList
  
**Se aplica a:** Exchange Server 2013
  
El **elemento agentList** contiene un [elemento agent](agent.md) para cada agente instalado. 
  
- [configuración](configuration.md)
- [mexRuntime](mexruntime.md)
- [agentList](agentlist.md)
  
```XML
<agentList>
      <agent/>
</agentList>
```

**agentListType (complexType)**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[agente](agent.md) <br/> |Contiene información de configuración sobre un agente instalado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[mexRuntime](mexruntime.md) <br/> |Contiene elementos que definen la información de configuración para la supervisión de agentes y la información de configuración sobre los agentes instalados.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |Este archivo no define un espacio de nombres.  <br/> |
|Nombre de esquema  <br/> |No disponible.  <br/> |
|Archivo de validación  <br/> |No disponible.  <br/> |
|Puede estar vacío  <br/> |Falso.  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos de archivo de configuración de agentes para Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

