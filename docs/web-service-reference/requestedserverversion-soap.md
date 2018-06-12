---
title: RequestedServerVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: cf3f9d7a-2add-4457-b009-2929220f90b5
description: El elemento RequestedServerVersion especifica que un método de detección automática de llamadas los objetivos de la versión del servidor.
ms.openlocfilehash: 6b9d31f3b7bca087652f04e4943becc5ac4e68e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837132"
---
# <a name="requestedserverversion-soap"></a>RequestedServerVersion (SOAP)

El elemento **RequestedServerVersion** especifica que un método de **detección automática** de llamadas los objetivos de la versión del servidor. 
  
```XML
<RequestedServerVersion/>
```

 **ExchangeVersion**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **RequestedServerVersion** especifica que un método de **detección automática** de llamadas los objetivos de la versión del servidor. En la siguiente tabla se enumera las versiones de servidor válido. 
  
|**Valor de texto**|**Descripción**|
|:-----|:-----|
|Exchange2007_SP1  <br/> |Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
|Exchange2010  <br/> |Exchange Server 2010.  <br/> |
|Exchange2010_SP1  <br/> |Exchange Server 2010 Service Pack 1 (SP1).  <br/> |
|Exchange2010_SP2  <br/> |Exchange Server 2010 Service Pack 2 (SP2).  <br/> |
|Exchange2013  <br/> |Exchange Server 2013. El campo Exchange2013 es aplicable para los clientes que estén destinados a Exchange Online y versiones de Exchange a partir de Exchange Server 2013.  <br/> |
|Exchange2013_SP1  <br/> |Exchange Server 2013 Service Pack 1 (SP1). El campo Exchange2013_SP1 es aplicable para los clientes que estén destinados a Exchange Online y versiones de Exchange a partir de Exchange Server 2013 SP1.  <br/> |
   
## <a name="remarks"></a>Notas

El elemento **RequestedServerVersion** está establecido en el encabezado SOAP. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |True  <br/> |
   

