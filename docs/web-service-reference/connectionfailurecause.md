---
title: ConnectionFailureCause
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectionFailureCause
api_type:
- schema
ms.assetid: d2160c8a-015c-4964-b7f7-93478764a173
description: El elemento ConnectionFailureCause especifica la razón de una desconexión de una llamada telefónica.
ms.openlocfilehash: 54b4f5b89efdb42ef82dbef8f1af14a39c0ccc6a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763774"
---
# <a name="connectionfailurecause"></a>ConnectionFailureCause

El elemento **ConnectionFailureCause** especifica la razón de una desconexión de una llamada telefónica. 
  
```xml
<ConnectionFailureCause>None or UserBusy or NoAnswer or Unavailable or Other</ConnectionFailureCause>
```

 **ConnectionFailureCauseType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[PhoneCallInformation](phonecallinformation.md) <br/> |Especifica la información de estado para una llamada de teléfono.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumera los valores posibles para el elemento **ConnectionFailureCause** . 
  
**Valores de elemento ConnectionFailureCause**

|**Valor**|**Descripción**|
|:-----|:-----|
|None  <br/> |Estado de llamada no está desconectado o no se conoce la razón por la desconexión.  <br/> |
|UserBusy  <br/> |La línea de terceros llamada estaba ocupada.  <br/> |
|NoAnswer  <br/> |El receptor no ha respondido.  <br/> |
|No disponible  <br/> |El número de receptor no estaba disponible.  <br/> |
|Otro  <br/> |Denominaba por otros motivos desconectar.  <br/> |
   
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

