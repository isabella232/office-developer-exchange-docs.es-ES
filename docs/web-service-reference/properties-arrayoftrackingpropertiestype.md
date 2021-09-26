---
title: Properties (ArrayOfTrackingPropertiesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Properties
api_type:
- schema
ms.assetid: 175566d2-fd62-45a2-8518-2827912cec88
description: El elemento Properties contiene una lista de una o más propiedades de seguimiento.
ms.openlocfilehash: 8232b94effe3aae5b07be12bdaf1b5e85331938f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542984"
---
# <a name="properties-arrayoftrackingpropertiestype"></a>Properties (ArrayOfTrackingPropertiesType)

El **elemento Properties** contiene una lista de una o más propiedades de seguimiento. 
  
- [FindMessageTrackingReport](findmessagetrackingreport.md)
  
- [Properties (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md)
  
```xml
<Properties>
   <TrackingPropertyType/>
</Properties>
```

**ArrayOfTrackingPropertiesType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[TrackingPropertyType](trackingpropertytype.md) <br/> |Representa un par de nombres y valores de cadenas que se usan para crear propiedades para informes de seguimiento de mensajes.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |Especifica los criterios para los tipos de mensajes que se deben buscar.  <br/> |
|[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) <br/> |Contiene el estado y el resultado de una única [solicitud de operación FindMessageTrackingReport.](findmessagetrackingreport-operation.md)  <br/> |
|[GetMessageTrackingReport](getmessagetrackingreport.md) <br/> |Contiene la solicitud de la [operación GetMessageTrackingReport para](getmessagetrackingreport-operation.md) recuperar el informe de seguimiento de mensajes completo del identificador especificado.  <br/> |
|[GetMessageTrackingReportResponse](getmessagetrackingreportresponse.md) <br/> |Contiene el resultado de una única [solicitud de operación GetMessageTrackingReport.](getmessagetrackingreport-operation.md)  <br/> |
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |Contiene información para un único evento para un destinatario.  <br/> |
|[MessageTrackingReport](messagetrackingreport.md) <br/> |Contiene un único mensaje que se devuelve en una [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md).  <br/> |
|[MessageTrackingSearchResult](messagetrackingsearchresult.md) <br/> |Contiene un único resultado de mensaje para un [elemento FindMessageTrackingReportResponse.](findmessagetrackingreportresponse.md)  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Web Services.Este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Operación FindMessageTrackingReport](findmessagetrackingreport-operation.md)
- [Operación GetMessageTrackingReport](getmessagetrackingreport-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

