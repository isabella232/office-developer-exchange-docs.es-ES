---
title: RequestServerVersion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RequestServerVersion
api_type:
- schema
ms.assetid: af4032d5-42b3-463e-9d0a-8236d78e5b75
description: El elemento RequestServerVersion contiene la información de control de versiones que identifica la versión del esquema a la que se dirigirá una solicitud.
ms.openlocfilehash: 4f01d5fcc2a2e08d426efc8d1f0a193d6139a038
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541878"
---
# <a name="requestserverversion"></a>RequestServerVersion

El **elemento RequestServerVersion** contiene la información de control de versiones que identifica la versión del esquema a la que se dirigirá una solicitud. 
  
```XML
<RequestServerVersion Version=""/>
```

 **ExchangeVersionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|Versión  <br/> |Describe la versión de destino de la solicitud. Este atributo es necesario cuando la versión del servidor de destino es una versión de Exchange a partir Exchange Server 2010.  <br/> |
   
#### <a name="version-attribute-values"></a>Valores de atributo Version

|**Valor**|**Descripción**|
|:-----|:-----|
|Exchange2007  <br/> |Dirigirse a los archivos de esquema para la versión de lanzamiento inicial de Exchange 2007.  <br/> |
|Exchange2007_SP1  <br/> |Dirigirse a los archivos de esquema de Exchange 2007 Service Pack 1 (SP1), Exchange 2007 Service Pack 2 (SP2) y Exchange 2007 Service Pack 3 (SP3).  <br/> |
|Exchange2010  <br/> |Dirigirse a los archivos de esquema Exchange 2010.  <br/> |
|Exchange2010_SP1  <br/> |Dirigirse a los archivos de esquema Exchange 2010 Service Pack 1 (SP1).  <br/> |
|Exchange2010_SP2  <br/> |Dirigirse a los archivos de esquema para Exchange 2010 Service Pack 2 (SP2) y Exchange 2010 Service Pack 3 (SP3).  <br/> |
|Exchange2013  <br/> |Dirigirse a los archivos de esquema Exchange 2013.  <br/> |
|Exchange2013_SP1  <br/> |Dirigirse a los archivos de esquema Exchange 2013 Service Pack 1 (SP1).  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

El **elemento RequestServerVersion** se encuentra en el encabezado SOAP. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Solicitudes de control de versiones](https://msdn.microsoft.com/library/76877b0a-d2e5-4c74-9295-7b445a41d46a%28Office.15%29.aspx)

