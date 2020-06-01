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
description: El elemento FindFolder define una solicitud para buscar carpetas en un buzón.
ms.openlocfilehash: 248047206a661afe723543e52c51b57847148423
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462580"
---
# <a name="findfolder"></a><span data-ttu-id="6f106-103">FindFolder</span><span class="sxs-lookup"><span data-stu-id="6f106-103">FindFolder</span></span>

<span data-ttu-id="6f106-104">El elemento **FindFolder** define una solicitud para buscar carpetas en un buzón.</span><span class="sxs-lookup"><span data-stu-id="6f106-104">The **FindFolder** element defines a request to find folders in a mailbox.</span></span> 
  
```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <IndexedPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <FractionalPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

<span data-ttu-id="6f106-105">**FindFolderType**</span><span class="sxs-lookup"><span data-stu-id="6f106-105">**FindFolderType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6f106-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6f106-106">Attributes and elements</span></span>

<span data-ttu-id="6f106-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6f106-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f106-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6f106-108">Attributes</span></span>

|<span data-ttu-id="6f106-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="6f106-109">**Attribute**</span></span>|<span data-ttu-id="6f106-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f106-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6f106-111">Transversal</span><span class="sxs-lookup"><span data-stu-id="6f106-111">Traversal</span></span>  <br/> |<span data-ttu-id="6f106-112">Define cómo se realiza una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6f106-112">Defines how a search is performed.</span></span> <span data-ttu-id="6f106-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6f106-113">This attribute is required.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="6f106-114">Valores de atributo de recorrido</span><span class="sxs-lookup"><span data-stu-id="6f106-114">Traversal attribute values</span></span>

|<span data-ttu-id="6f106-115">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6f106-115">**Value**</span></span>|<span data-ttu-id="6f106-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f106-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6f106-117">Profunda</span><span class="sxs-lookup"><span data-stu-id="6f106-117">Shallow</span></span>  <br/> |<span data-ttu-id="6f106-118">Indica a la operación FindFolder que busque sólo en la carpeta identificada y que devuelva sólo los identificadores de la carpeta para los elementos que no se han eliminado.</span><span class="sxs-lookup"><span data-stu-id="6f106-118">Instructs the FindFolder operation to search only the identified folder and to return only the folder IDs for items that have not been deleted.</span></span> <span data-ttu-id="6f106-119">Esto se denomina recorrido superficial.</span><span class="sxs-lookup"><span data-stu-id="6f106-119">This is called a shallow traversal.</span></span>  <br/> |
|<span data-ttu-id="6f106-120">Gran</span><span class="sxs-lookup"><span data-stu-id="6f106-120">Deep</span></span>  <br/> |<span data-ttu-id="6f106-121">Indica a la operación FindFolder que busque en todas las carpetas secundarias de la carpeta principal identificada y que devuelva sólo los identificadores de carpeta de los elementos que no se han eliminado.</span><span class="sxs-lookup"><span data-stu-id="6f106-121">Instructs the FindFolder operation to search in all child folders of the identified parent folder and to return only the folder IDs for items that have not been deleted.</span></span> <span data-ttu-id="6f106-122">Esto se denomina recorrido profundo.</span><span class="sxs-lookup"><span data-stu-id="6f106-122">This is called a deep traversal.</span></span>  <br/> |
|<span data-ttu-id="6f106-123">SoftDeleted</span><span class="sxs-lookup"><span data-stu-id="6f106-123">SoftDeleted</span></span>  <br/> |<span data-ttu-id="6f106-124">Indica a la operación FindFolder que realice una búsqueda de recorrido superficial para los elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="6f106-124">Instructs the FindFolder operation to perform a shallow traversal search for deleted items.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6f106-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6f106-125">Child elements</span></span>

|<span data-ttu-id="6f106-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6f106-126">**Element**</span></span>|<span data-ttu-id="6f106-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f106-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f106-128">FolderShape</span><span class="sxs-lookup"><span data-stu-id="6f106-128">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="6f106-129">Identifica las propiedades de carpeta que se deben incluir en una respuesta FindFolder.</span><span class="sxs-lookup"><span data-stu-id="6f106-129">Identifies the folder properties to include in a FindFolder response.</span></span>  <br/> |
|[<span data-ttu-id="6f106-130">IndexedPageFolderView</span><span class="sxs-lookup"><span data-stu-id="6f106-130">IndexedPageFolderView</span></span>](indexedpagefolderview.md) <br/> |<span data-ttu-id="6f106-131">Describe cómo se devuelve la información de elementos paginados en una respuesta FindFolder.</span><span class="sxs-lookup"><span data-stu-id="6f106-131">Describes how paged item information is returned in a FindFolder response.</span></span> <span data-ttu-id="6f106-132">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="6f106-132">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="6f106-133">FractionalPageFolderView</span><span class="sxs-lookup"><span data-stu-id="6f106-133">FractionalPageFolderView</span></span>](fractionalpagefolderview.md) <br/> |<span data-ttu-id="6f106-134">Describe dónde se inicia la vista paginada y el número máximo de carpetas que se devuelven en una solicitud FindFolder.</span><span class="sxs-lookup"><span data-stu-id="6f106-134">Describes where the paged view starts and the maximum number of folders returned in a FindFolder request.</span></span> <span data-ttu-id="6f106-135">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="6f106-135">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="6f106-136">Restriction</span><span class="sxs-lookup"><span data-stu-id="6f106-136">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="6f106-137">Define una restricción o consulta que se usa para filtrar las carpetas en una operación FindFolder.</span><span class="sxs-lookup"><span data-stu-id="6f106-137">Defines a restriction or query that is used to filter folders in a FindFolder operation.</span></span> <span data-ttu-id="6f106-138">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="6f106-138">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="6f106-139">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="6f106-139">ParentFolderIds</span></span>](parentfolderids.md) <br/> |<span data-ttu-id="6f106-140">Identifica las carpetas para la operación FindFolder que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="6f106-140">Identifies folders for the FindFolder operation to search.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6f106-141">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6f106-141">Parent elements</span></span>

<span data-ttu-id="6f106-142">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6f106-142">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6f106-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6f106-143">Remarks</span></span>

<span data-ttu-id="6f106-144">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="6f106-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="6f106-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f106-145">Example</span></span>

<span data-ttu-id="6f106-146">El siguiente ejemplo de una solicitud FindFolder muestra cómo crear una solicitud para buscar todas las carpetas que se encuentran en una bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="6f106-146">The following example of a FindFolder request shows how to form a request to find all the folders located in an Inbox.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a><span data-ttu-id="6f106-147">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6f106-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f106-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="6f106-148">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6f106-149">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6f106-149">Schema Name</span></span>  <br/> |<span data-ttu-id="6f106-150">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6f106-150">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6f106-151">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6f106-151">Validation File</span></span>  <br/> |<span data-ttu-id="6f106-152">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6f106-152">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6f106-153">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6f106-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="6f106-154">Falso</span><span class="sxs-lookup"><span data-stu-id="6f106-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f106-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f106-155">See also</span></span>

- [<span data-ttu-id="6f106-156">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="6f106-156">FindFolder operation</span></span>](findfolder-operation.md)

