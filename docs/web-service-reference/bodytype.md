---
title: BodyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BodyType
api_type:
- schema
ms.assetid: d42ec77b-fb9f-404a-9bf2-1801e8744676
description: El elemento BodyType identifica cómo se da el formato de texto del cuerpo en la respuesta.
ms.openlocfilehash: f8be2e96390b40faa367cf0d34c533accc3b8afb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763653"
---
# <a name="bodytype"></a><span data-ttu-id="02634-103">BodyType</span><span class="sxs-lookup"><span data-stu-id="02634-103">BodyType</span></span>

<span data-ttu-id="02634-104">El elemento **BodyType** identifica cómo se da el formato de texto del cuerpo en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="02634-104">The **BodyType** element identifies how the body text is formatted in the response.</span></span> 
  
```xml
<BodyType>Best or HTML or Text</BodyType>
```

<span data-ttu-id="02634-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="02634-105">**BodyTypeResponseType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="02634-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="02634-106">Attributes and elements</span></span>

<span data-ttu-id="02634-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="02634-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02634-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="02634-108">Attributes</span></span>

<span data-ttu-id="02634-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="02634-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="02634-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="02634-110">Child elements</span></span>

<span data-ttu-id="02634-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="02634-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="02634-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="02634-112">Parent elements</span></span>

|<span data-ttu-id="02634-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="02634-113">**Element**</span></span>|<span data-ttu-id="02634-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="02634-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02634-115">ItemShape</span><span class="sxs-lookup"><span data-stu-id="02634-115">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="02634-116">Identifica las propiedades de elemento y el contenido que desea incluir en una respuesta GetItem, FindItem o SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="02634-116">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/><br/><span data-ttu-id="02634-117">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="02634-117">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape`<br/><br/>`/FindItem/ItemShape`<br/><br/>`/SyncFolderItems/ItemShape` <br/> |
|[<span data-ttu-id="02634-118">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="02634-118">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="02634-119">Identifica las propiedades de elemento extendido adicional para devolver en una respuesta a una solicitud de [GetAttachment](getattachment.md) .</span><span class="sxs-lookup"><span data-stu-id="02634-119">Identifies additional extended item properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/><br/><span data-ttu-id="02634-120">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="02634-120">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="02634-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="02634-121">Text value</span></span>

<span data-ttu-id="02634-122">En la siguiente tabla se enumera los valores posibles para el elemento **BodyType** .</span><span class="sxs-lookup"><span data-stu-id="02634-122">The following table lists the possible values for the **BodyType** element.</span></span> 
  
|<span data-ttu-id="02634-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="02634-123">**Value**</span></span>|<span data-ttu-id="02634-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="02634-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02634-125">Mejor</span><span class="sxs-lookup"><span data-stu-id="02634-125">Best</span></span>  <br/> |<span data-ttu-id="02634-126">La respuesta devolverá el contenido disponible más completa del texto del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="02634-126">The response will return the richest available content of body text.</span></span> <span data-ttu-id="02634-127">Esto es útil si se desconoce si el contenido es texto o HTML.</span><span class="sxs-lookup"><span data-stu-id="02634-127">This is useful if it is unknown whether the content is text or HTML.</span></span><br/><br/> <span data-ttu-id="02634-128">El cuerpo devuelto será texto si el cuerpo almacenado es texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="02634-128">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="02634-129">De lo contrario, la respuesta devolverá HTML si se encuentra el cuerpo almacenado en formato HTML o RTF.</span><span class="sxs-lookup"><span data-stu-id="02634-129">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span><br/><br/> <span data-ttu-id="02634-130">Éste es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="02634-130">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="02634-131">HTML</span><span class="sxs-lookup"><span data-stu-id="02634-131">HTML</span></span>  <br/> |<span data-ttu-id="02634-132">La respuesta devolverá un cuerpo del elemento como HTML.</span><span class="sxs-lookup"><span data-stu-id="02634-132">The response will return an item body as HTML.</span></span>  <br/> |
|<span data-ttu-id="02634-133">Texto</span><span class="sxs-lookup"><span data-stu-id="02634-133">Text</span></span>  <br/> |<span data-ttu-id="02634-134">La respuesta devolverá un cuerpo del elemento como texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="02634-134">The response will return an item body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02634-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="02634-135">Remarks</span></span>

<span data-ttu-id="02634-136">Puede identificar el tipo de cuerpo devuelto en la respuesta comprobando el atributo **BodyType** del elemento [Body](body.md) .</span><span class="sxs-lookup"><span data-stu-id="02634-136">You can identify the type of body returned in the response by checking the **BodyType** attribute of the [Body](body.md) element.</span></span> <span data-ttu-id="02634-137">El atributo **BodyType** identificará el cuerpo como HTML o texto.</span><span class="sxs-lookup"><span data-stu-id="02634-137">The **BodyType** attribute will identify the body as either HTML or text.</span></span> 
  
<span data-ttu-id="02634-138">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="02634-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="02634-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="02634-139">Example</span></span>

<span data-ttu-id="02634-140">El siguiente ejemplo de una solicitud de muestra donde se usa un elemento **BodyType** .</span><span class="sxs-lookup"><span data-stu-id="02634-140">The following example of a request shows where a **BodyType** element is used.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape>
        <t:BodyType>Best</t:BodyType>
      </AttachmentShape>
      <AttachmentIds>
        <t:AttachmentId Id="ASkAS="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="02634-141">El atributo Id se ha acortado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="02634-141">The Id attribute has been shortened to preserve readability.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02634-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="02634-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02634-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="02634-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="02634-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="02634-144">Schema Name</span></span>  <br/> |<span data-ttu-id="02634-145">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="02634-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="02634-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="02634-146">Validation File</span></span>  <br/> |<span data-ttu-id="02634-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="02634-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="02634-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="02634-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="02634-149">False</span><span class="sxs-lookup"><span data-stu-id="02634-149">False</span></span>  <br/> |
   

