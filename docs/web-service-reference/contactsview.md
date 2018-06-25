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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763810"
---
# <a name="contactsview"></a><span data-ttu-id="38a1d-103">Contactos</span><span class="sxs-lookup"><span data-stu-id="38a1d-103">ContactsView</span></span>

<span data-ttu-id="38a1d-104">El elemento de **contactos** define una búsqueda de elementos de contacto basándose en los nombres para mostrar alfabético.</span><span class="sxs-lookup"><span data-stu-id="38a1d-104">The **ContactsView** element defines a search for contact items based on alphabetical display names.</span></span> 
  
[<span data-ttu-id="38a1d-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="38a1d-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="38a1d-106">Contactos</span><span class="sxs-lookup"><span data-stu-id="38a1d-106">ContactsView</span></span>](contactsview.md)
  
```xml
<ContactsView MaxEntriesReturned="" InitialName="" FinalName="" />
```

<span data-ttu-id="38a1d-107">**ContactsViewType**</span><span class="sxs-lookup"><span data-stu-id="38a1d-107">**ContactsViewType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="38a1d-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="38a1d-108">Attributes and elements</span></span>

<span data-ttu-id="38a1d-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="38a1d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38a1d-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="38a1d-110">Attributes</span></span>

|<span data-ttu-id="38a1d-111">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="38a1d-111">**Attribute**</span></span>|<span data-ttu-id="38a1d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="38a1d-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="38a1d-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="38a1d-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="38a1d-114">Describe el número máximo de resultados a devolver en la respuesta [FindItem](finditem.md) .</span><span class="sxs-lookup"><span data-stu-id="38a1d-114">Describes the maximum number of results to return in the [FindItem](finditem.md) response.</span></span>  <br/> |
|<span data-ttu-id="38a1d-115">**InitialName**</span><span class="sxs-lookup"><span data-stu-id="38a1d-115">**InitialName**</span></span> <br/> |<span data-ttu-id="38a1d-116">Define el nombre de la lista de contactos para devolver en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38a1d-116">Defines the first name in the contacts list to return in the response.</span></span> <span data-ttu-id="38a1d-117">Si el nombre inicial especificado no está en la lista de contactos, el siguiente nombre alfabético como se define en el contexto de la referencia cultural se devolverán, excepto si el nombre del siguiente procede después de **FinalName**.</span><span class="sxs-lookup"><span data-stu-id="38a1d-117">If the specified initial name is not in the contacts list, the next alphabetical name as defined by the cultural context will be returned, except if the next name comes after **FinalName**.</span></span> <span data-ttu-id="38a1d-118">Si se omite el atributo **InitialName** , la respuesta contendrá una lista de contactos que comienza por el primer nombre de la lista de contactos.</span><span class="sxs-lookup"><span data-stu-id="38a1d-118">If the **InitialName** attribute is omitted, the response will contain a list of contacts that starts with the first name in the contact list.</span></span> <span data-ttu-id="38a1d-119">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="38a1d-119">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="38a1d-120">**FinalName**</span><span class="sxs-lookup"><span data-stu-id="38a1d-120">**FinalName**</span></span> <br/> |<span data-ttu-id="38a1d-121">Define el nombre del último en la lista de contactos para devolver en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38a1d-121">Defines the last name in the contacts list to return in the response.</span></span> <span data-ttu-id="38a1d-122">Si se omite el atributo **FinalName** , la respuesta contendrá todos los contactos posteriores en el criterio de ordenación especificado.</span><span class="sxs-lookup"><span data-stu-id="38a1d-122">If the **FinalName** attribute is omitted, the response will contain all subsequent contacts in the specified sort order.</span></span> <span data-ttu-id="38a1d-123">Si el nombre final especificado no está en la lista de contactos, el siguiente nombre alfabético como se define en el contexto de la referencia cultural se excluirá.</span><span class="sxs-lookup"><span data-stu-id="38a1d-123">If the specified final name is not in the contacts list, the next alphabetical name as defined by the cultural context will be excluded.</span></span>  <br/><br/><span data-ttu-id="38a1d-124">Por ejemplo, si FinalName = "Nombre", pero nombre no está en la lista de contactos, contactos que tienen nombres de nombre1 para mostrar o nombre no se incluirán.</span><span class="sxs-lookup"><span data-stu-id="38a1d-124">For example, if FinalName="Name", but Name is not in the contacts list, contacts that have display names of Name1 or NAME will not be included.</span></span>  <br/><br/><span data-ttu-id="38a1d-125">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="38a1d-125">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="38a1d-126">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="38a1d-126">Child elements</span></span>

<span data-ttu-id="38a1d-127">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="38a1d-127">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="38a1d-128">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="38a1d-128">Parent elements</span></span>

|<span data-ttu-id="38a1d-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="38a1d-129">**Element**</span></span>|<span data-ttu-id="38a1d-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="38a1d-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38a1d-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="38a1d-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="38a1d-132">Define una solicitud para buscar elementos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="38a1d-132">Defines a request to find items in a mailbox.</span></span><br/><br/> <span data-ttu-id="38a1d-133">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="38a1d-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38a1d-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="38a1d-134">Remarks</span></span>

<span data-ttu-id="38a1d-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="38a1d-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="38a1d-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="38a1d-136">Example</span></span>

<span data-ttu-id="38a1d-137">El siguiente ejemplo de una solicitud, muestra cómo buscar los contactos a tres primeros los comenzando por el contacto que tiene el nombre para mostrar de Kelly Rollin.</span><span class="sxs-lookup"><span data-stu-id="38a1d-137">The following example of a request demonstrates how to find the first three contacts starting with the contact that has the display name of Kelly Rollin.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="38a1d-138">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="38a1d-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38a1d-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="38a1d-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="38a1d-140">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="38a1d-140">Schema Name</span></span>  <br/> |<span data-ttu-id="38a1d-141">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="38a1d-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="38a1d-142">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="38a1d-142">Validation File</span></span>  <br/> |<span data-ttu-id="38a1d-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="38a1d-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="38a1d-144">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="38a1d-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="38a1d-145">False</span><span class="sxs-lookup"><span data-stu-id="38a1d-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38a1d-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="38a1d-146">See also</span></span>

- [<span data-ttu-id="38a1d-147">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="38a1d-147">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="38a1d-148">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="38a1d-148">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

