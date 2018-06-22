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
description: El elemento FolderShape identifica las propiedades de carpeta para incluir en una respuesta GetFolder, FindFolder o SyncFolderHierarchy.
ms.openlocfilehash: 8ebdd70ef13ee9f0cce9020b9212576cba782be4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764698"
---
# <a name="foldershape"></a><span data-ttu-id="53ff8-103">FolderShape</span><span class="sxs-lookup"><span data-stu-id="53ff8-103">FolderShape</span></span>

<span data-ttu-id="53ff8-104">El elemento **FolderShape** identifica las propiedades de carpeta para incluir en una respuesta [GetFolder](getfolder.md), [FindFolder](findfolder.md)o [SyncFolderHierarchy](syncfolderhierarchy.md) .</span><span class="sxs-lookup"><span data-stu-id="53ff8-104">The **FolderShape** element identifies the folder properties to include in a [GetFolder](getfolder.md), [FindFolder](findfolder.md), or [SyncFolderHierarchy](syncfolderhierarchy.md) response.</span></span> 
  
```xml
<FolderShape>
   <BaseShape/>
   <AdditionalProperties/>
</FolderShape>
```

 <span data-ttu-id="53ff8-105">**FolderResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="53ff8-105">**FolderResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="53ff8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="53ff8-106">Attributes and elements</span></span>

<span data-ttu-id="53ff8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="53ff8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53ff8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="53ff8-108">Attributes</span></span>

<span data-ttu-id="53ff8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="53ff8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="53ff8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="53ff8-110">Child elements</span></span>

|<span data-ttu-id="53ff8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="53ff8-111">**Element**</span></span>|<span data-ttu-id="53ff8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53ff8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53ff8-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="53ff8-113">BaseShape</span></span>](baseshape.md) <br/> |<span data-ttu-id="53ff8-114">Identifica la configuración básica de propiedades se devuelven en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="53ff8-114">Identifies the basic configuration of properties to return in a response.</span></span>  <br/> |
|[<span data-ttu-id="53ff8-115">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="53ff8-115">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="53ff8-116">Identifica las propiedades adicionales para devolver en una respuesta.</span><span class="sxs-lookup"><span data-stu-id="53ff8-116">Identifies additional properties to return in a response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="53ff8-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="53ff8-117">Parent elements</span></span>

|<span data-ttu-id="53ff8-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="53ff8-118">**Element**</span></span>|<span data-ttu-id="53ff8-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53ff8-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53ff8-120">FindFolder</span><span class="sxs-lookup"><span data-stu-id="53ff8-120">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="53ff8-121">Define una solicitud para identificar las carpetas de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="53ff8-121">Defines a request to identify folders in a mailbox.</span></span>  <br/> <span data-ttu-id="53ff8-122">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="53ff8-122">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
|[<span data-ttu-id="53ff8-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="53ff8-123">GetFolder</span></span>](getfolder.md) <br/> |<span data-ttu-id="53ff8-124">Define una solicitud para obtener una carpeta desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="53ff8-124">Defines a request to get a folder from the Exchange store.</span></span>  <br/> <span data-ttu-id="53ff8-125">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="53ff8-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetFolder` <br/> |
|[<span data-ttu-id="53ff8-126">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="53ff8-126">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md) <br/> |<span data-ttu-id="53ff8-127">Define una solicitud para sincronizar una jerarquía de carpetas en un cliente.</span><span class="sxs-lookup"><span data-stu-id="53ff8-127">Defines a request to synchronize a folder hierarchy on a client.</span></span>  <br/> <span data-ttu-id="53ff8-128">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="53ff8-128">The following is the XPath expression to this element:</span></span>  <br/>  `/SyncFolderHierarchy` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53ff8-129">Notas</span><span class="sxs-lookup"><span data-stu-id="53ff8-129">Remarks</span></span>

<span data-ttu-id="53ff8-130">El elemento **FolderShape** es un elemento secundario necesario del elemento [FindFolder](findfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="53ff8-130">The **FolderShape** element is a required child element of the [FindFolder](findfolder.md) element.</span></span> 
  
<span data-ttu-id="53ff8-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="53ff8-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="53ff8-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53ff8-132">Example</span></span>

<span data-ttu-id="53ff8-133">El siguiente ejemplo de una solicitud, muestra cómo buscar todas las carpetas que se encuentra en el primer nivel de la carpeta Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="53ff8-133">The following example of a request demonstrates how to find all folders located in the first level of the Inbox folder.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="53ff8-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="53ff8-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53ff8-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="53ff8-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="53ff8-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="53ff8-136">Schema Name</span></span>  <br/> |<span data-ttu-id="53ff8-137">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="53ff8-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="53ff8-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="53ff8-138">Validation File</span></span>  <br/> |<span data-ttu-id="53ff8-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="53ff8-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="53ff8-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="53ff8-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="53ff8-141">False</span><span class="sxs-lookup"><span data-stu-id="53ff8-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53ff8-142">Ver también</span><span class="sxs-lookup"><span data-stu-id="53ff8-142">See also</span></span>



[<span data-ttu-id="53ff8-143">FindFolder</span><span class="sxs-lookup"><span data-stu-id="53ff8-143">FindFolder</span></span>](findfolder.md)

