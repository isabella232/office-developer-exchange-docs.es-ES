---
title: Contactos
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContactsView
api_type:
- schema
ms.assetid: 8534f44b-a5af-4a9f-9621-23a3eff5f9d8
description: El elemento de contactos define una búsqueda de elementos de contacto basándose en los nombres para mostrar alfabético.
ms.openlocfilehash: e578eb4dd0042b8c478e883c7fa54d7f2e984229
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763810"
---
# <a name="contactsview"></a>Contactos

El elemento de **contactos** define una búsqueda de elementos de contacto basándose en los nombres para mostrar alfabético. 
  
[FindItem](finditem.md)
  
[Contactos](contactsview.md)
  
```xml
<ContactsView MaxEntriesReturned="" InitialName="" FinalName="" />
```

**ContactsViewType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Describe el número máximo de resultados a devolver en la respuesta [FindItem](finditem.md) .  <br/> |
|**InitialName** <br/> |Define el nombre de la lista de contactos para devolver en la respuesta. Si el nombre inicial especificado no está en la lista de contactos, el siguiente nombre alfabético como se define en el contexto de la referencia cultural se devolverán, excepto si el nombre del siguiente procede después de **FinalName**. Si se omite el atributo **InitialName** , la respuesta contendrá una lista de contactos que comienza por el primer nombre de la lista de contactos. Este atributo es opcional.  <br/> |
|**FinalName** <br/> |Define el nombre del último en la lista de contactos para devolver en la respuesta. Si se omite el atributo **FinalName** , la respuesta contendrá todos los contactos posteriores en el criterio de ordenación especificado. Si el nombre final especificado no está en la lista de contactos, el siguiente nombre alfabético como se define en el contexto de la referencia cultural se excluirá.  <br/><br/>Por ejemplo, si FinalName = "Nombre", pero nombre no está en la lista de contactos, contactos que tienen nombres de nombre1 para mostrar o nombre no se incluirán.  <br/><br/>Este atributo es opcional.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar elementos en un buzón de correo.<br/><br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="example"></a>Ejemplo

El siguiente ejemplo de una solicitud, muestra cómo buscar los contactos a tres primeros los comenzando por el contacto que tiene el nombre para mostrar de Kelly Rollin.
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación FindItem](finditem-operation.md)
- [Buscar elementos](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

