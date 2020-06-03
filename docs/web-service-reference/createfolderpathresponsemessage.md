---
title: CreateFolderPathResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f7b3507-713d-4ccf-8518-75fa6f967d6d
description: El elemento CreateFolderPathResponseMessage especifica el mensaje de respuesta para una solicitud de CreateFolderPath.
ms.openlocfilehash: 3c0c4e98b568a6398dcd0e71a6e6931a3f47e3da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458890"
---
# <a name="createfolderpathresponsemessage"></a>CreateFolderPathResponseMessage

El elemento **CreateFolderPathResponseMessage** especifica el mensaje de respuesta para una solicitud de **CreateFolderPath** . 
  
```XML
<CreateFolderPathResponseMessage ResponseClass="">
    <Folders></Folders>
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</CreateFolderPathResponseMessage>
```

 **FolderInfoResponseMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|ResponseClass  <br/> |Indica la clase de la respuesta.  <br/> |
   
#### <a name="responseclass"></a>ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|Correcto  <br/> |Indica que se ha realizado correctamente.  <br/> |
|Advertencia  <br/> |Indica una advertencia.  <br/> |
|Error  <br/> |Indica un error.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Folders](folders-ex15websvcsotherref.md) <br/> |Contiene una matriz de carpetas que se usan en las operaciones de carpeta.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no está en uso y reservado para uso futuro.  <br/> |
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información de respuesta de error adicional.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona información de estado sobre la solicitud.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |messages. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

