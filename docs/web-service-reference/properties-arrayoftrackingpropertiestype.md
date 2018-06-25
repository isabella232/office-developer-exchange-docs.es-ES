---
title: Propiedades (ArrayOfTrackingPropertiesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Properties
api_type:
- schema
ms.assetid: 175566d2-fd62-45a2-8518-2827912cec88
description: El elemento de propiedades contiene una lista de una o varias propiedades de seguimiento.
ms.openlocfilehash: 079d2d2c101fdeb7f26d65798048c3c6c59f3e94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836897"
---
# <a name="properties-arrayoftrackingpropertiestype"></a>Propiedades (ArrayOfTrackingPropertiesType)

El elemento de **Propiedades** contiene una lista de una o varias propiedades de seguimiento. 
  
- [FindMessageTrackingReport](findmessagetrackingreport.md)
  
- [Propiedades (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md)
  
```xml
<Properties>
   <TrackingPropertyType/>
</Properties>
```

**ArrayOfTrackingPropertiesType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[TrackingPropertyType](trackingpropertytype.md) <br/> |Representa un par de cadenas nombre y valor que se usa para crear las propiedades de los informes de seguimiento de mensajes.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |Especifica los criterios para los tipos de mensajes para buscar.  <br/> |
|[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) <br/> |Contiene el estado y el resultado de una única solicitud de [operación FindMessageTrackingReport](findmessagetrackingreport-operation.md) .  <br/> |
|[GetMessageTrackingReport](getmessagetrackingreport.md) <br/> |Contiene la solicitud para la [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md) recuperar el mensaje completo informe de seguimiento para el identificador especificado.  <br/> |
|[GetMessageTrackingReportResponse](getmessagetrackingreportresponse.md) <br/> |Contiene el resultado de una única solicitud de [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md) .  <br/> |
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |Contiene información de un solo evento de un destinatario.  <br/> |
|[MessageTrackingReport](messagetrackingreport.md) <br/> |Contiene un solo mensaje que se devuelve en una [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md).  <br/> |
|[MessageTrackingSearchResult](messagetrackingsearchresult.md) <br/> |Contiene un resultado de mensaje único para un elemento [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) .  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación FindMessageTrackingReport](findmessagetrackingreport-operation.md)
- [Operación GetMessageTrackingReport](getmessagetrackingreport-operation.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

