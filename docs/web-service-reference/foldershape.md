---
title: FolderShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderShape
api_type:
- schema
ms.assetid: 244f4f46-a33d-4764-92e3-1bddb4dc6a49
description: El elemento FolderShape identifica las propiedades de carpeta que se deben incluir en una respuesta GetFolder, FindFolder o SyncFolderHierarchy.
ms.openlocfilehash: f841fcc4570604c474387dfa24ec07c9d2784f62
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461348"
---
# <a name="foldershape"></a><span data-ttu-id="3e36d-103">FolderShape</span><span class="sxs-lookup"><span data-stu-id="3e36d-103">FolderShape</span></span>

<span data-ttu-id="3e36d-104">El elemento **FolderShape** identifica las propiedades de carpeta que se deben incluir en una respuesta [GetFolder](getfolder.md), [FindFolder](findfolder.md)o [SyncFolderHierarchy](syncfolderhierarchy.md) .</span><span class="sxs-lookup"><span data-stu-id="3e36d-104">The **FolderShape** element identifies the folder properties to include in a [GetFolder](getfolder.md), [FindFolder](findfolder.md), or [SyncFolderHierarchy](syncfolderhierarchy.md) response.</span></span> 
  
```xml
<FolderShape>
   <BaseShape/>
   <AdditionalProperties/>
</FolderShape>
```

 <span data-ttu-id="3e36d-105">**FolderResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="3e36d-105">**FolderResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3e36d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3e36d-106">Attributes and elements</span></span>

<span data-ttu-id="3e36d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3e36d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3e36d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3e36d-108">Attributes</span></span>

<span data-ttu-id="3e36d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3e36d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3e36d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3e36d-110">Child elements</span></span>

|<span data-ttu-id="3e36d-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3e36d-111">**Element**</span></span>|<span data-ttu-id="3e36d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3e36d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e36d-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="3e36d-113">BaseShape</span></span>](baseshape.md) <br/> |<span data-ttu-id="3e36d-114">Identifica la configuración básica de las propiedades que se van a devolver en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="3e36d-114">Identifies the basic configuration of properties to return in a response.</span></span>  <br/> |
|[<span data-ttu-id="3e36d-115">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="3e36d-115">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="3e36d-116">Identifica las propiedades adicionales que se devolverán en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="3e36d-116">Identifies additional properties to return in a response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3e36d-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3e36d-117">Parent elements</span></span>

|<span data-ttu-id="3e36d-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3e36d-118">**Element**</span></span>|<span data-ttu-id="3e36d-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3e36d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e36d-120">FindFolder</span><span class="sxs-lookup"><span data-stu-id="3e36d-120">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="3e36d-121">Define una solicitud para identificar las carpetas en un buzón.</span><span class="sxs-lookup"><span data-stu-id="3e36d-121">Defines a request to identify folders in a mailbox.</span></span>  <br/> <span data-ttu-id="3e36d-122">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="3e36d-122">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
|[<span data-ttu-id="3e36d-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="3e36d-123">GetFolder</span></span>](getfolder.md) <br/> |<span data-ttu-id="3e36d-124">Define una solicitud para obtener una carpeta del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3e36d-124">Defines a request to get a folder from the Exchange store.</span></span>  <br/> <span data-ttu-id="3e36d-125">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="3e36d-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetFolder` <br/> |
|[<span data-ttu-id="3e36d-126">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="3e36d-126">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md) <br/> |<span data-ttu-id="3e36d-127">Define una solicitud para sincronizar una jerarquía de carpetas en un cliente.</span><span class="sxs-lookup"><span data-stu-id="3e36d-127">Defines a request to synchronize a folder hierarchy on a client.</span></span>  <br/> <span data-ttu-id="3e36d-128">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="3e36d-128">The following is the XPath expression to this element:</span></span>  <br/>  `/SyncFolderHierarchy` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e36d-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3e36d-129">Remarks</span></span>

<span data-ttu-id="3e36d-130">El elemento **FolderShape** es un elemento secundario necesario del elemento [FindFolder](findfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="3e36d-130">The **FolderShape** element is a required child element of the [FindFolder](findfolder.md) element.</span></span> 
  
<span data-ttu-id="3e36d-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="3e36d-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="3e36d-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3e36d-132">Example</span></span>

<span data-ttu-id="3e36d-133">El siguiente ejemplo de una solicitud muestra cómo buscar todas las carpetas que se encuentran en el primer nivel de la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="3e36d-133">The following example of a request demonstrates how to find all folders located in the first level of the Inbox folder.</span></span>
  
```
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

## <a name="element-information"></a><span data-ttu-id="3e36d-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3e36d-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e36d-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e36d-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3e36d-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3e36d-136">Schema Name</span></span>  <br/> |<span data-ttu-id="3e36d-137">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3e36d-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3e36d-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3e36d-138">Validation File</span></span>  <br/> |<span data-ttu-id="3e36d-139">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3e36d-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3e36d-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3e36d-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="3e36d-141">Falso</span><span class="sxs-lookup"><span data-stu-id="3e36d-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3e36d-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e36d-142">See also</span></span>



[<span data-ttu-id="3e36d-143">FindFolder</span><span class="sxs-lookup"><span data-stu-id="3e36d-143">FindFolder</span></span>](findfolder.md)

