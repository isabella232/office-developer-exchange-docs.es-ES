---
title: RequestedServerVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: cf3f9d7a-2add-4457-b009-2929220f90b5
description: El elemento RequestedServerVersion especifica la versión del servidor a la que un método de detección automática llama a destinos.
ms.openlocfilehash: 0690481523ab48497c40338a8808dfa2ed9b0e99
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540562"
---
# <a name="requestedserverversion-soap"></a>RequestedServerVersion (SOAP)

El **elemento RequestedServerVersion** especifica la versión del servidor a la que un **método de detección** automática llama a destinos. 
  
```XML
<RequestedServerVersion/>
```

 **ExchangeVersion**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento RequestedServerVersion** especifica la versión del servidor a la que un **método de** detección automática llama a destinos. En la tabla siguiente se enumeran las versiones de servidor válidas. 
  
|**Valor de texto**|**Descripción**|
|:-----|:-----|
|Exchange2007_SP1  <br/> |Exchange Server 2007 Service Pack 1 (SP1).  <br/> |
|Exchange2010  <br/> |Exchange Server 2010.  <br/> |
|Exchange2010_SP1  <br/> |Exchange Server 2010 Service Pack 1 (SP1).  <br/> |
|Exchange2010_SP2  <br/> |Exchange Server 2010 Service Pack 2 (SP2).  <br/> |
|Exchange2013  <br/> |Exchange Server 2013. El campo Exchange2013 se aplica a los clientes que tienen como destino Exchange Online y versiones de Exchange a partir Exchange Server 2013.  <br/> |
|Exchange2013_SP1  <br/> |Exchange Server 2013 Service Pack 1 (SP1). El Exchange2013_SP1 se aplica a los clientes que tienen como destino Exchange Online y versiones de Exchange a partir de Exchange Server 2013 SP1.  <br/> |
   
## <a name="remarks"></a>Comentarios

El **elemento RequestedServerVersion** se establece en el encabezado SOAP. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   

