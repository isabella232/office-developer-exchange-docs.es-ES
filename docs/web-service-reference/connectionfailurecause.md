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
description: El elemento ConnectionFailureCause especifica el motivo por el que se ha desconectado una llamada telefónica.
ms.openlocfilehash: 6385641eaee140a114906703232974d51d5ce344
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529451"
---
# <a name="connectionfailurecause"></a>ConnectionFailureCause

El elemento **ConnectionFailureCause** especifica el motivo por el que se ha desconectado una llamada telefónica. 
  
```xml
<ConnectionFailureCause>None or UserBusy or NoAnswer or Unavailable or Other</ConnectionFailureCause>
```

 **ConnectionFailureCauseType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PhoneCallInformation](phonecallinformation.md) <br/> |Especifica la información de estado de una llamada telefónica.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumeran los valores posibles para el elemento **ConnectionFailureCause** . 
  
**Valores del elemento ConnectionFailureCause**

|**Valor**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |El estado de la llamada no se desconecta o no se conoce el motivo de la desconexión.  <br/> |
|UserBusy  <br/> |La línea de parte llamada estaba ocupada.  <br/> |
|Noanswer  <br/> |La parte llamada no responde.  <br/> |
|Momentos  <br/> |El número de la parte llamada no estaba disponible.  <br/> |
|Otros  <br/> |Comodín para otros motivos de desconexión.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

