---
title: mexRuntime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- mexRuntime
api_type:
- schema
ms.assetid: eabb2f12-10a7-4ce2-ae4b-9c04010c765f
description: 'Última modificación: 17 de septiembre de 2015'
ms.openlocfilehash: f192965a8375eb46d1ca5b46d3b768a3299c284d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461838"
---
# <a name="mexruntime"></a>mexRuntime
  
**Se aplica a:** Exchange Server 2013
  
El elemento **mexRuntime** contiene elementos que definen la información de configuración para la supervisión de agentes y la información de configuración para SMTP y los agentes de enrutamiento que están instalados. 
  
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
|[monitor](monitoring.md) <br/> |Contiene información de configuración que define cómo y cuándo transporte los agentes instalados.  <br/> |
|[agentList](agentlist.md) <br/> |Contiene un elemento [Agent](agent.md) para cada agente instalado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[configuración](configuration.md) <br/> |El elemento raíz del archivo de configuración de agentes.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |Este archivo no define un espacio de nombres.  <br/> |
|Nombre de esquema  <br/> |No disponible.  <br/> |
|Archivo de validación  <br/> |No disponible.  <br/> |
|Puede estar vacío  <br/> |Falso.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos del archivo de configuración de agentes para Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

