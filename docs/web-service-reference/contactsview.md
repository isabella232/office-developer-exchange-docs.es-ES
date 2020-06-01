---
title: ContactsView
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
description: El elemento ContactsView define una búsqueda de elementos de contacto basándose en los nombres para mostrar alfabéticos.
ms.openlocfilehash: 23c3fe13c44cdd0e5a054ecb3378bc3d633e55aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463821"
---
# <a name="contactsview"></a><span data-ttu-id="ef327-103">ContactsView</span><span class="sxs-lookup"><span data-stu-id="ef327-103">ContactsView</span></span>

<span data-ttu-id="ef327-104">El elemento **ContactsView** define una búsqueda de elementos de contacto basándose en los nombres para mostrar alfabéticos.</span><span class="sxs-lookup"><span data-stu-id="ef327-104">The **ContactsView** element defines a search for contact items based on alphabetical display names.</span></span> 
  
[<span data-ttu-id="ef327-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="ef327-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="ef327-106">ContactsView</span><span class="sxs-lookup"><span data-stu-id="ef327-106">ContactsView</span></span>](contactsview.md)
  
```xml
<ContactsView MaxEntriesReturned="" InitialName="" FinalName="" />
```

<span data-ttu-id="ef327-107">**ContactsViewType**</span><span class="sxs-lookup"><span data-stu-id="ef327-107">**ContactsViewType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ef327-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ef327-108">Attributes and elements</span></span>

<span data-ttu-id="ef327-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ef327-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef327-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="ef327-110">Attributes</span></span>

|<span data-ttu-id="ef327-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ef327-111">**Attribute**</span></span>|<span data-ttu-id="ef327-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef327-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef327-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="ef327-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="ef327-114">Describe el número máximo de resultados que se devolverá en la respuesta [FindItem](finditem.md) .</span><span class="sxs-lookup"><span data-stu-id="ef327-114">Describes the maximum number of results to return in the [FindItem](finditem.md) response.</span></span>  <br/> |
|<span data-ttu-id="ef327-115">**InitialName**</span><span class="sxs-lookup"><span data-stu-id="ef327-115">**InitialName**</span></span> <br/> |<span data-ttu-id="ef327-116">Define el primer nombre de la lista de contactos que se va a devolver en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef327-116">Defines the first name in the contacts list to return in the response.</span></span> <span data-ttu-id="ef327-117">Si el nombre inicial especificado no está en la lista de contactos, se devolverá el siguiente nombre alfabético definido por el contexto de la referencia cultural, excepto si el nombre siguiente viene después de **FinalName**.</span><span class="sxs-lookup"><span data-stu-id="ef327-117">If the specified initial name is not in the contacts list, the next alphabetical name as defined by the cultural context will be returned, except if the next name comes after **FinalName**.</span></span> <span data-ttu-id="ef327-118">Si se omite el atributo **InitialName** , la respuesta contendrá una lista de contactos que comienza con el primer nombre de la lista de contactos.</span><span class="sxs-lookup"><span data-stu-id="ef327-118">If the **InitialName** attribute is omitted, the response will contain a list of contacts that starts with the first name in the contact list.</span></span> <span data-ttu-id="ef327-119">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="ef327-119">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="ef327-120">**FinalName**</span><span class="sxs-lookup"><span data-stu-id="ef327-120">**FinalName**</span></span> <br/> |<span data-ttu-id="ef327-121">Define los apellidos de la lista de contactos para que se devuelvan en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef327-121">Defines the last name in the contacts list to return in the response.</span></span> <span data-ttu-id="ef327-122">Si se omite el atributo **FinalName** , la respuesta contendrá todos los contactos subsiguientes en el criterio de ordenación especificado.</span><span class="sxs-lookup"><span data-stu-id="ef327-122">If the **FinalName** attribute is omitted, the response will contain all subsequent contacts in the specified sort order.</span></span> <span data-ttu-id="ef327-123">Si el nombre final especificado no está en la lista de contactos, se excluirá el siguiente nombre alfabético definido por el contexto de la referencia cultural.</span><span class="sxs-lookup"><span data-stu-id="ef327-123">If the specified final name is not in the contacts list, the next alphabetical name as defined by the cultural context will be excluded.</span></span>  <br/><br/><span data-ttu-id="ef327-124">Por ejemplo, si FinalName = "Name", pero Name no está en la lista de contactos, no se incluirán los contactos que tengan nombres para mostrar de Nombre1 o nombre.</span><span class="sxs-lookup"><span data-stu-id="ef327-124">For example, if FinalName="Name", but Name is not in the contacts list, contacts that have display names of Name1 or NAME will not be included.</span></span>  <br/><br/><span data-ttu-id="ef327-125">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="ef327-125">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ef327-126">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ef327-126">Child elements</span></span>

<span data-ttu-id="ef327-127">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ef327-127">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ef327-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ef327-128">Parent elements</span></span>

|<span data-ttu-id="ef327-129">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ef327-129">**Element**</span></span>|<span data-ttu-id="ef327-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef327-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef327-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="ef327-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="ef327-132">Define una solicitud para buscar elementos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="ef327-132">Defines a request to find items in a mailbox.</span></span><br/><br/> <span data-ttu-id="ef327-133">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="ef327-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef327-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ef327-134">Remarks</span></span>

<span data-ttu-id="ef327-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ef327-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="ef327-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ef327-136">Example</span></span>

<span data-ttu-id="ef327-137">El siguiente ejemplo de una solicitud muestra cómo encontrar los tres primeros contactos que comienzan por el contacto que tiene el nombre para mostrar de Kelly Rollin.</span><span class="sxs-lookup"><span data-stu-id="ef327-137">The following example of a request demonstrates how to find the first three contacts starting with the contact that has the display name of Kelly Rollin.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="ef327-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ef327-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef327-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef327-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ef327-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ef327-140">Schema Name</span></span>  <br/> |<span data-ttu-id="ef327-141">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ef327-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ef327-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ef327-142">Validation File</span></span>  <br/> |<span data-ttu-id="ef327-143">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ef327-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ef327-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ef327-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="ef327-145">Falso</span><span class="sxs-lookup"><span data-stu-id="ef327-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef327-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef327-146">See also</span></span>

- [<span data-ttu-id="ef327-147">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="ef327-147">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="ef327-148">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="ef327-148">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

