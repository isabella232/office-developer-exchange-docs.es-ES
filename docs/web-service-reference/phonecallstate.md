---
title: PhoneCallState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PhoneCallState
api_type:
- schema
ms.assetid: ac009eb3-6334-49ce-82be-48fe83577f9c
description: El elemento PhoneCallState especifica el estado actual de una llamada telefónica.
ms.openlocfilehash: 8c0b8357b58826f18f05eb0fedc0865be1623c2b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528305"
---
# <a name="phonecallstate"></a>PhoneCallState

El **elemento PhoneCallState** especifica el estado actual de una llamada telefónica. 
  
```xml
<PhoneCallState>Idle or Connecting or Alerted or Connected or Disconnected or Incoming or Transferring or Forwarding</PhoneCallState>
```

 **PhoneCallStateType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PhoneCallInformation](phonecallinformation.md) <br/> |Especifica la información de estado de una llamada telefónica.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la tabla siguiente se enumeran los valores posibles para el **elemento PhoneCallState.** 
  
**Valores del elemento PhoneCallState**

|**Valor**|**Descripción**|
|:-----|:-----|
|Inactivo  <br/> |Estado inicial de la llamada.  <br/> |
|Conectando  <br/> |El sistema está marcando esta llamada.  <br/> |
|Alertado  <br/> |La llamada está en estado de alerta (el teléfono está sonando).  <br/> |
|Conectados  <br/> |La llamada está en el estado conectado.  <br/> |
|Desconectado  <br/> |La llamada está desconectada.  <br/> |
|Entrante  <br/> |La llamada es entrante.  <br/> |
|Transferencia  <br/> |La llamada se transfiere a otro destino.  <br/> |
|Reenvío  <br/> |La llamada se reenvía a otro destino.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio /ews/ del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

