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
description: El elemento PhoneCallState especifica el estado actual de una llamada de teléfono.
ms.openlocfilehash: d2088b9b2811befe80684188d49c8034c577cc55
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468533"
---
# <a name="phonecallstate"></a>PhoneCallState

El elemento **PhoneCallState** especifica el estado actual de una llamada de teléfono. 
  
```xml
<PhoneCallState>Idle or Connecting or Alerted or Connected or Disconnected or Incoming or Transferring or Forwarding</PhoneCallState>
```

 **PhoneCallStateType**
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

En la siguiente tabla se enumeran los valores posibles para el elemento **PhoneCallState** . 
  
**Valores del elemento PhoneCallState**

|**Valor**|**Descripción**|
|:-----|:-----|
|Usado  <br/> |Estado de la llamada inicial.  <br/> |
|Conectando  <br/> |El sistema está llamando a esta llamada.  <br/> |
|Alertas  <br/> |La llamada está en estado de alerta (el teléfono está sonando).  <br/> |
|Conectado  <br/> |La llamada está en estado conectado.  <br/> |
|Desconectado  <br/> |La llamada está desconectada.  <br/> |
|Entra  <br/> |La llamada es entrante.  <br/> |
|Transferencia  <br/> |La llamada se está transfiriendo a otro destino.  <br/> |
|Reenvío  <br/> |La llamada se está reenviando a otro destino.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio/EWS/del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

