---
title: PhoneCallState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhoneCallState
api_type:
- schema
ms.assetid: ac009eb3-6334-49ce-82be-48fe83577f9c
description: El elemento PhoneCallState especifica el estado actual de una llamada telefónica.
ms.openlocfilehash: 184a7400810711442e565d1ef37094bd63b00914
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836761"
---
# <a name="phonecallstate"></a>PhoneCallState

El elemento **PhoneCallState** especifica el estado actual de una llamada telefónica. 
  
```xml
<PhoneCallState>Idle or Connecting or Alerted or Connected or Disconnected or Incoming or Transferring or Forwarding</PhoneCallState>
```

 **PhoneCallStateType**
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

En la siguiente tabla se enumera los valores posibles para el elemento **PhoneCallState** . 
  
**Valores de elemento PhoneCallState**

|**Valor**|**Descripción**|
|:-----|:-----|
|Inactividad  <br/> |Estado de llamada inicial.  <br/> |
|Conectando  <br/> |El sistema está marcando esta llamada.  <br/> |
|Una alerta  <br/> |La llamada está en estado de alerta (teléfono está sonando).  <br/> |
|Conectado  <br/> |La llamada se encuentra en el estado de la conexión.  <br/> |
|Desconectado  <br/> |Se desconectó la llamada.  <br/> |
|Entrante  <br/> |La llamada es entrante.  <br/> |
|Transferir  <br/> |La llamada se transfiere a otro destino.  <br/> |
|Desvío de llamadas  <br/> |La llamada es se reenvíen a otro destino.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio /ews/ del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

