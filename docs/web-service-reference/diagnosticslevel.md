---
title: DiagnosticsLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DiagnosticsLevel
api_type:
- schema
ms.assetid: 66794226-f5e0-44f0-8a0e-1f194bb0ba0f
description: El elemento DiagnosticsLevel representa la información de tiempo y rendimiento que se usará para derivar el informe.
ms.openlocfilehash: c7e74f324385ca76a58872e2e735ea2c5d926a53
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519803"
---
# <a name="diagnosticslevel"></a>DiagnosticsLevel

El **elemento DiagnosticsLevel** representa la información de tiempo y rendimiento que se usará para derivar el informe. 
  
```XML
<DiagnosticsLevel/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |Contiene criterios para los tipos de mensajes que se deben buscar.  <br/> |
|[GetMessageTrackingReport](getmessagetrackingreport.md) <br/> |Contiene la solicitud de la [operación GetMessageTrackingReport para](getmessagetrackingreport-operation.md) recuperar el informe de seguimiento de mensajes completo del identificador especificado.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, se requiere un valor de texto que representa una cadena.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetMessageTrackingReport](getmessagetrackingreport-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

