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
description: El elemento RequestedServerVersion especifica la versión del servidor destino de una llamada al método de detección automática.
ms.openlocfilehash: ff63c82943bdd3476a4284f5aa2075fc9c0194b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467910"
---
# <a name="requestedserverversion-soap"></a>RequestedServerVersion (SOAP)

El elemento **RequestedServerVersion** especifica la versión del servidor destino de una llamada al método de **detección automática** . 
  
```XML
<RequestedServerVersion/>
```

 **ExchangeVersion**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

Ninguna.
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **RequestedServerVersion** especifica la versión del servidor a la que se dirige una llamada al método de **detección automática** . En la siguiente tabla se enumeran las versiones de servidor válidas. 
  
|**Valor de texto**|**Descripción**|
|:-----|:-----|
|Exchange2007_SP1  <br/> |Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
|Exchange2010  <br/> |Exchange Server 2010.  <br/> |
|Exchange2010_SP1  <br/> |Exchange Server 2010 Service Pack 1 (SP1).  <br/> |
|Exchange2010_SP2  <br/> |Exchange Server 2010 Service Pack 2 (SP2).  <br/> |
|Exchange2013  <br/> |Exchange Server 2013. El campo Exchange2013 se aplica a los clientes de Exchange Online y versiones de Exchange que comienzan con Exchange Server 2013.  <br/> |
|Exchange2013_SP1  <br/> |Exchange Server 2013 Service Pack 1 (SP1). El campo Exchange2013_SP1 se aplica a los clientes de Exchange Online y versiones de Exchange que comienzan con Exchange Server 2013 SP1.  <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento **RequestedServerVersion** se establece en el encabezado SOAP. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   

