---
title: DataType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DataType
api_type:
- schema
ms.assetid: 267fe5aa-f9b1-4d4c-ac11-0f2e50ec2627
description: El elemento DataType describe el tipo de datos que comparte una carpeta compartida.
ms.openlocfilehash: a7df8d38e10f0ab31038d790d8f35208d1be66d5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458834"
---
# <a name="datatype"></a>DataType

El elemento **DataType** describe el tipo de datos que comparte una carpeta compartida. 
  
```xml
<DataType>Calendar or Contacts</DataType>
```

**SharingDataType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetSharingFolder](getsharingfolder.md) <br/> |Define una solicitud para obtener el identificador de carpeta local de una carpeta compartida especificada.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumeran los valores posibles para el elemento **DataType** . 
  
**Valores del elemento DataType**

|**Valor**|**Descripción**|
|:-----|:-----|
|Calendar  <br/> |Indica que la carpeta compartida contiene información del calendario.  <br/> |
|Contactos  <br/> |Indica que la carpeta compartida contiene información de contacto.  <br/> |
   
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

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

