---
title: ConnectionFailureCause
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConnectionFailureCause
api_type:
- schema
ms.assetid: d2160c8a-015c-4964-b7f7-93478764a173
description: El elemento ConnectionFailureCause especifica el motivo de una desconexión de una llamada telefónica.
ms.openlocfilehash: de2f06ae89577b0141b8555f98dba1671a228d45
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543537"
---
# <a name="connectionfailurecause"></a>ConnectionFailureCause

El **elemento ConnectionFailureCause** especifica el motivo de una desconexión de una llamada telefónica. 
  
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

En la tabla siguiente se enumeran los valores posibles para el **elemento ConnectionFailureCause.** 
  
**Valores del elemento ConnectionFailureCause**

|**Valor**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |El estado de la llamada no está desconectado o no se conoce el motivo de la desconexión.  <br/> |
|UserBusy  <br/> |La línea de grupo llamada estaba ocupada.  <br/> |
|NoAnswer  <br/> |La parte llamada no respondió.  <br/> |
|No disponible  <br/> |El número de parte llamado no estaba disponible.  <br/> |
|Otro  <br/> |Catch-all por otros motivos de desconexión.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

