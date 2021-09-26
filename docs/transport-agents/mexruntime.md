---
title: mexRuntime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- mexRuntime
api_type:
- schema
ms.assetid: eabb2f12-10a7-4ce2-ae4b-9c04010c765f
description: 'Last modified: September 17, 2015'
ms.openlocfilehash: c7ae630a01ac0339433a7c78859c06006efab4b5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546913"
---
# <a name="mexruntime"></a>mexRuntime
  
**Se aplica a:** Exchange Server 2013
  
El **elemento mexRuntime** contiene elementos que definen la información de configuración para la supervisión de agentes y la información de configuración para smtp y agentes de enrutamiento que están instalados. 
  
- [configuración](configuration.md)  
- [mexRuntime](mexruntime.md)
  
```XML
<mexRuntime>
   <monitoring/>
   <agentList/>
</mexRuntime>
```

**mexRuntimeType (complexType)**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[supervisión](monitoring.md) <br/> |Contiene información de configuración que define cómo y cuándo el transporte supervisa los agentes que están instalados.  <br/> |
|[agentList](agentlist.md) <br/> |Contiene un [elemento de](agent.md) agente para cada agente instalado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[configuración](configuration.md) <br/> |Elemento raíz del archivo de configuración de agentes.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |Este archivo no define un espacio de nombres.  <br/> |
|Nombre de esquema  <br/> |No disponible.  <br/> |
|Archivo de validación  <br/> |No disponible.  <br/> |
|Puede estar vacío  <br/> |Falso.  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Elementos de archivo de configuración de agentes para Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

