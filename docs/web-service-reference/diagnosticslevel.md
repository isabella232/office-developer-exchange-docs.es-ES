---
title: DiagnosticsLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DiagnosticsLevel
api_type:
- schema
ms.assetid: 66794226-f5e0-44f0-8a0e-1f194bb0ba0f
description: El elemento DiagnosticsLevel representa la información de tiempo y de rendimiento que se usará para derivar el informe.
ms.openlocfilehash: 3060d4f1b8449a5870d964bdfcdbf0d503905abc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467833"
---
# <a name="diagnosticslevel"></a>DiagnosticsLevel

El elemento **DiagnosticsLevel** representa la información de tiempo y de rendimiento que se usará para derivar el informe. 
  
```XML
<DiagnosticsLevel/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |Contiene los criterios para los tipos de mensajes que se van a buscar.  <br/> |
|[GetMessageTrackingReport](getmessagetrackingreport.md) <br/> |Contiene la solicitud de la [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md) para recuperar el informe completo de seguimiento de mensajes del identificador especificado.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, se necesita un valor de texto que represente una cadena.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetMessageTrackingReport](getmessagetrackingreport-operation.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

