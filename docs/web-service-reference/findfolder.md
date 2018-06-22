---
title: FindFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindFolder
api_type:
- schema
ms.assetid: b8a59740-d978-454c-9629-a10792385ba0
description: El elemento FindFolder define una solicitud para buscar las carpetas en un buzón de correo.
ms.openlocfilehash: d41283547c443e38e2e87379a7224df9c89f901d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764617"
---
# <a name="findfolder"></a><span data-ttu-id="a985b-103">FindFolder</span><span class="sxs-lookup"><span data-stu-id="a985b-103">FindFolder</span></span>

<span data-ttu-id="a985b-104">El elemento **FindFolder** define una solicitud para buscar las carpetas en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a985b-104">The **FindFolder** element defines a request to find folders in a mailbox.</span></span> 
  
```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <IndexedPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

 <span data-ttu-id="a985b-105">**FindFolderType**</span><span class="sxs-lookup"><span data-stu-id="a985b-105">**FindFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a985b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a985b-106">Attributes and elements</span></span>

<span data-ttu-id="a985b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a985b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a985b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a985b-108">Attributes</span></span>

|<span data-ttu-id="a985b-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="a985b-109">**Attribute**</span></span>|<span data-ttu-id="a985b-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a985b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a985b-111">Cruce seguro del</span><span class="sxs-lookup"><span data-stu-id="a985b-111">Traversal</span></span>  <br/> |<span data-ttu-id="a985b-112">Define cómo se realiza una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a985b-112">Defines how a search is performed.</span></span> <span data-ttu-id="a985b-113">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="a985b-113">This attribute is required.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="a985b-114">Valores de atributo recorrido</span><span class="sxs-lookup"><span data-stu-id="a985b-114">Traversal attribute values</span></span>

|<span data-ttu-id="a985b-115">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a985b-115">**Value**</span></span>|<span data-ttu-id="a985b-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a985b-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a985b-117">Superficial</span><span class="sxs-lookup"><span data-stu-id="a985b-117">Shallow</span></span>  <br/> |<span data-ttu-id="a985b-118">Indica a la operación de FindFolder para buscar sólo la carpeta identificada y devolver sólo la carpeta identificadores para los elementos que no se han eliminado.</span><span class="sxs-lookup"><span data-stu-id="a985b-118">Instructs the FindFolder operation to search only the identified folder and to return only the folder IDs for items that have not been deleted.</span></span> <span data-ttu-id="a985b-119">Esto se denomina un recorrido superficial.</span><span class="sxs-lookup"><span data-stu-id="a985b-119">This is called a shallow traversal.</span></span>  <br/> |
|<span data-ttu-id="a985b-120">Profunda</span><span class="sxs-lookup"><span data-stu-id="a985b-120">Deep</span></span>  <br/> |<span data-ttu-id="a985b-121">Indica a la operación de FindFolder para buscar en todas las carpetas secundarias de la carpeta principal identificado y devolver sólo la carpeta identificadores para los elementos que no se han eliminado.</span><span class="sxs-lookup"><span data-stu-id="a985b-121">Instructs the FindFolder operation to search in all child folders of the identified parent folder and to return only the folder IDs for items that have not been deleted.</span></span> <span data-ttu-id="a985b-122">Esto se denomina un recorrido profundo.</span><span class="sxs-lookup"><span data-stu-id="a985b-122">This is called a deep traversal.</span></span>  <br/> |
|<span data-ttu-id="a985b-123">SoftDeleted</span><span class="sxs-lookup"><span data-stu-id="a985b-123">SoftDeleted</span></span>  <br/> |<span data-ttu-id="a985b-124">Indica a la operación FindFolder para realizar una búsqueda de recorrido superficial de los elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="a985b-124">Instructs the FindFolder operation to perform a shallow traversal search for deleted items.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a985b-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a985b-125">Child elements</span></span>

|<span data-ttu-id="a985b-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="a985b-126">**Element**</span></span>|<span data-ttu-id="a985b-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a985b-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a985b-128">FolderShape</span><span class="sxs-lookup"><span data-stu-id="a985b-128">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="a985b-129">Identifica las propiedades de carpeta para incluir en una respuesta FindFolder.</span><span class="sxs-lookup"><span data-stu-id="a985b-129">Identifies the folder properties to include in a FindFolder response.</span></span>  <br/> |
|[<span data-ttu-id="a985b-130">IndexedPageFolderView</span><span class="sxs-lookup"><span data-stu-id="a985b-130">IndexedPageFolderView</span></span>](indexedpagefolderview.md) <br/> |<span data-ttu-id="a985b-131">Describe cómo paginada elemento de información se devuelve en una respuesta FindFolder.</span><span class="sxs-lookup"><span data-stu-id="a985b-131">Describes how paged item information is returned in a FindFolder response.</span></span> <span data-ttu-id="a985b-132">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="a985b-132">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a985b-133">FractionalPageFolderView</span><span class="sxs-lookup"><span data-stu-id="a985b-133">FractionalPageFolderView</span></span>](fractionalpagefolderview.md) <br/> |<span data-ttu-id="a985b-134">Describe donde se inicia la vista de página y devuelve el número máximo de carpetas en una solicitud FindFolder.</span><span class="sxs-lookup"><span data-stu-id="a985b-134">Describes where the paged view starts and the maximum number of folders returned in a FindFolder request.</span></span> <span data-ttu-id="a985b-135">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="a985b-135">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a985b-136">Restriction</span><span class="sxs-lookup"><span data-stu-id="a985b-136">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="a985b-137">Define una restricción o una consulta que se usa para filtrar las carpetas en una operación FindFolder.</span><span class="sxs-lookup"><span data-stu-id="a985b-137">Defines a restriction or query that is used to filter folders in a FindFolder operation.</span></span> <span data-ttu-id="a985b-138">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="a985b-138">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a985b-139">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="a985b-139">ParentFolderIds</span></span>](parentfolderids.md) <br/> |<span data-ttu-id="a985b-140">Identifica las carpetas para la operación FindFolder buscar.</span><span class="sxs-lookup"><span data-stu-id="a985b-140">Identifies folders for the FindFolder operation to search.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a985b-141">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a985b-141">Parent elements</span></span>

<span data-ttu-id="a985b-142">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a985b-142">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a985b-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a985b-143">Remarks</span></span>

<span data-ttu-id="a985b-144">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="a985b-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="a985b-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a985b-145">Example</span></span>

<span data-ttu-id="a985b-146">El siguiente ejemplo de una solicitud de FindFolder muestra cómo formar una solicitud para buscar todas las carpetas que se encuentra en una bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="a985b-146">The following example of a FindFolder request shows how to form a request to find all the folders located in an Inbox.</span></span>
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="a985b-147">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a985b-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a985b-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a985b-148">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a985b-149">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a985b-149">Schema Name</span></span>  <br/> |<span data-ttu-id="a985b-150">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a985b-150">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a985b-151">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a985b-151">Validation File</span></span>  <br/> |<span data-ttu-id="a985b-152">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a985b-152">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a985b-153">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a985b-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="a985b-154">False</span><span class="sxs-lookup"><span data-stu-id="a985b-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a985b-155">Ver también</span><span class="sxs-lookup"><span data-stu-id="a985b-155">See also</span></span>



[<span data-ttu-id="a985b-156">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="a985b-156">FindFolder operation</span></span>](findfolder-operation.md)

