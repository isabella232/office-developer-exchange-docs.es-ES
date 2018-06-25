---
title: RequestServerVersion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequestServerVersion
api_type:
- schema
ms.assetid: af4032d5-42b3-463e-9d0a-8236d78e5b75
description: El elemento RequestServerVersion contiene la información de control de versiones que identifica la versión del esquema de destino para una solicitud.
ms.openlocfilehash: 0092d90a5fc479363f6d774b793c7148ad29f21c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837143"
---
# <a name="requestserverversion"></a>RequestServerVersion

El elemento **RequestServerVersion** contiene la información de control de versiones que identifica la versión del esquema de destino para una solicitud. 
  
```XML
<RequestServerVersion Version=""/>
```

 **ExchangeVersionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|Versión  <br/> |Describe la versión de destino para la solicitud. Este atributo es necesario cuando la versión del servidor de destino es una versión de Exchange a partir de Exchange Server 2010.  <br/> |
   
#### <a name="version-attribute-values"></a>Valores de atributo de versión

|**Valor**|**Descripción**|
|:-----|:-----|
|Exchange2007  <br/> |Los archivos de esquema para la versión de lanzamiento inicial de Exchange 2007 de destino.  <br/> |
|Exchange2007_SP1  <br/> |Los archivos de esquema para Exchange 2007 Service Pack 1 (SP1), Service Pack 2 (SP2) de Exchange 2007 y Exchange 2007 Service Pack 3 (SP3) de destino.  <br/> |
|Exchange2010  <br/> |Los archivos de esquema para Exchange 2010 de destino.  <br/> |
|Exchange2010_SP1  <br/> |Los archivos de esquema para Exchange 2010 Service Pack 1 (SP1) de destino.  <br/> |
|Exchange2010_SP2  <br/> |Los archivos de esquema para Exchange 2010 Service Pack 2 (SP2) y Service Pack 3 (SP3) de Exchange 2010 de destino.  <br/> |
|Exchange2013  <br/> |Los archivos de esquema para Exchange 2013 de destino.  <br/> |
|Exchange2013_SP1  <br/> |Los archivos de esquema para Exchange 2013 Service Pack 1 (SP1) de destino.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

El elemento **RequestServerVersion** se encuentra en el encabezado SOAP. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


[Solicitudes de control de versiones](http://msdn.microsoft.com/library/76877b0a-d2e5-4c74-9295-7b445a41d46a%28Office.15%29.aspx)

