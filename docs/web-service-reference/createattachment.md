---
title: CreateAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAttachment
api_type:
- schema
ms.assetid: e33b403a-b7d3-48ee-8d24-6b7abf0d70bc
description: El elemento CreateAttachment define una solicitud para crear un archivo adjunto a un elemento en el almacén de Exchange.
ms.openlocfilehash: d403eb5ca15623d3a973f7b224dbcde5529cf1bc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763915"
---
# <a name="createattachment"></a>CreateAttachment

El elemento **CreateAttachment** define una solicitud para crear un archivo adjunto a un elemento en el almacén de Exchange. 
  
```xml
<CreateAttachment>
   <ParentItemId/>
   <Attachments/>
</CreateAttachment>
```

 **CreateAttachmentType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ParentItemId](parentitemid.md) <br/> |Identifica el elemento primario del almacén de Exchange que contiene los datos adjuntos creado. El elemento [ParentItemId](parentitemid.md) debe proporcionar el identificador de un intercambio real almacenar el elemento. Artículos de la tienda real se pueden recuperar mediante el uso de la [operación GetItem](getitem-operation.md); los datos adjuntos se recuperan mediante el uso de la [operación GetAttachment](getattachment-operation.md). Se produce un error si el [ParentItemId](parentitemid.md) se pasa el identificador de un archivo adjunto. Si el [ParentItemId](parentitemid.md) representa el identificador de datos adjuntos de elemento existente, la [operación CreateAttachment](createattachment-operation.md) agrega los nuevos datos adjuntos a los datos adjuntos existentes.  <br/> Este elemento es necesario para la [operación CreateAttachment](createattachment-operation.md).  <br/> |
|[Datos adjuntos](attachments-ex15websvcsotherref.md) <br/> |Contiene los elementos o archivos para adjuntar a un elemento en el almacén de Exchange.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Observaciones

Un elemento de los datos adjuntos no existe como un elemento del almacén. Sólo existe como datos adjuntos a un elemento o en otro objeto attachment. Datos adjuntos de elemento sólo se pueden recuperar mediante el uso de la solicitud de [GetAttachment](getattachment.md) . 
  
Pueden crearse los siguientes datos adjuntos de elemento:
  
- Elemento
    
- Message
    
- CalendarItem
    
- Contacto
    
- Tarea
    
- MeetingMessage
    
- MeetingRequest
    
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo crear y adjuntar un elemento a otro elemento en el almacén de Exchange.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <ParentItemId Id="ASkAS"/>
      <Attachments>
        <t:ItemAttachment>
          <t:Name>MyAttachment</t:Name>
          <t:Message>
            <t:ItemClass>IPM>Note</t:ItemClass>
            <t:Subject>My attachment subject</t:Subject>
            <t:Body BodyType="Text">My attachment body</t:Body>
          </t:Message>
        </t:ItemAttachment>
      </Attachments>
    </CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación CreateAttachment](createattachment-operation.md)
  
[Operación DeleteAttachment](deleteattachment-operation.md)
  
[Operación GetAttachment](getattachment-operation.md)

