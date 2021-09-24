---
title: ContactsView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ContactsView
api_type:
- schema
ms.assetid: 8534f44b-a5af-4a9f-9621-23a3eff5f9d8
description: El elemento ContactsView define una búsqueda de elementos de contacto basada en nombres para mostrar alfabéticos.
ms.openlocfilehash: a96da6270d2396e5e82851dcc200f818cec5a7ed
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531102"
---
# <a name="contactsview"></a>ContactsView

El **elemento ContactsView** define una búsqueda de elementos de contacto basada en nombres para mostrar alfabéticos. 
  
[FindItem](finditem.md)
  
[ContactsView](contactsview.md)
  
```xml
<ContactsView MaxEntriesReturned="" InitialName="" FinalName="" />
```

**ContactsViewType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Describe el número máximo de resultados que se devolverán en la [respuesta FindItem.](finditem.md)  <br/> |
|**InitialName** <br/> |Define el primer nombre de la lista de contactos que se devolverá en la respuesta. Si el nombre inicial especificado no está en la lista de contactos, se devolverá el siguiente nombre alfabético definido por el contexto cultural, excepto si el siguiente nombre viene después de **FinalName**. Si se omite el atributo **InitialName,** la respuesta contendrá una lista de contactos que comienza por el nombre de la lista de contactos. Este atributo es opcional.  <br/> |
|**FinalName** <br/> |Define el apellido de la lista de contactos que se devolverá en la respuesta. Si se omite el atributo **FinalName,** la respuesta contendrá todos los contactos posteriores en el criterio de ordenación especificado. Si el nombre final especificado no está en la lista de contactos, se excluirá el siguiente nombre alfabético definido por el contexto cultural.  <br/><br/>Por ejemplo, si FinalName="Name", pero Name no está en la lista de contactos, los contactos que tengan nombres para mostrar de Name1 o NAME no se incluirán.  <br/><br/>Este atributo es opcional.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón.<br/><br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo de una solicitud se muestra cómo buscar los tres primeros contactos a partir del contacto que tiene el nombre para mostrar de Kelly Rollin.
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="contacts:DisplayName"/>
        </t:AdditionalProperties>
      </ItemShape>
      <ContactsView MaxEntriesReturned="3" InitialName="Kelly Rollin" />
      <SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="contacts:DisplayName"/>
        </t:FieldOrder>
        </SortOrder>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="contacts"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación FindItem](finditem-operation.md)
- [Buscar elementos](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

