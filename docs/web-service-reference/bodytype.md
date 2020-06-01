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
description: El elemento BodyType identifica cómo se da formato al texto del cuerpo en la respuesta.
ms.openlocfilehash: 448d20ac54b09a2f4f6a273a1099519371ac7f5b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465950"
---
# <a name="bodytype"></a><span data-ttu-id="66a20-103">BodyType</span><span class="sxs-lookup"><span data-stu-id="66a20-103">BodyType</span></span>

<span data-ttu-id="66a20-104">El elemento **BodyType** identifica cómo se da formato al texto del cuerpo en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66a20-104">The **BodyType** element identifies how the body text is formatted in the response.</span></span> 
  
```xml
<BodyType>Best or HTML or Text</BodyType>
```

<span data-ttu-id="66a20-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="66a20-105">**BodyTypeResponseType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="66a20-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="66a20-106">Attributes and elements</span></span>

<span data-ttu-id="66a20-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="66a20-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66a20-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="66a20-108">Attributes</span></span>

<span data-ttu-id="66a20-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="66a20-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="66a20-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="66a20-110">Child elements</span></span>

<span data-ttu-id="66a20-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="66a20-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="66a20-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="66a20-112">Parent elements</span></span>

|<span data-ttu-id="66a20-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="66a20-113">**Element**</span></span>|<span data-ttu-id="66a20-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="66a20-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66a20-115">ItemShape</span><span class="sxs-lookup"><span data-stu-id="66a20-115">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="66a20-116">Identifica el contenido y las propiedades de los elementos que se van a incluir en una respuesta GetItem, FindItem o SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="66a20-116">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/><br/><span data-ttu-id="66a20-117">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="66a20-117">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape`<br/><br/>`/FindItem/ItemShape`<br/><br/>`/SyncFolderItems/ItemShape` <br/> |
|[<span data-ttu-id="66a20-118">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="66a20-118">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="66a20-119">Identifica las propiedades adicionales de elementos extendidos que se van a devolver en una respuesta a una solicitud [GetAttachment](getattachment.md) .</span><span class="sxs-lookup"><span data-stu-id="66a20-119">Identifies additional extended item properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/><br/><span data-ttu-id="66a20-120">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="66a20-120">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="66a20-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="66a20-121">Text value</span></span>

<span data-ttu-id="66a20-122">En la siguiente tabla se enumeran los valores posibles para el elemento **BodyType** .</span><span class="sxs-lookup"><span data-stu-id="66a20-122">The following table lists the possible values for the **BodyType** element.</span></span> 
  
|<span data-ttu-id="66a20-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="66a20-123">**Value**</span></span>|<span data-ttu-id="66a20-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="66a20-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="66a20-125">Procedimientos</span><span class="sxs-lookup"><span data-stu-id="66a20-125">Best</span></span>  <br/> |<span data-ttu-id="66a20-126">La respuesta devolverá el contenido más enriquecido disponible del texto del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="66a20-126">The response will return the richest available content of body text.</span></span> <span data-ttu-id="66a20-127">Esto es útil si es desconocido si el contenido es de texto o HTML.</span><span class="sxs-lookup"><span data-stu-id="66a20-127">This is useful if it is unknown whether the content is text or HTML.</span></span><br/><br/> <span data-ttu-id="66a20-128">El cuerpo devuelto será Text si el cuerpo almacenado es texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="66a20-128">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="66a20-129">De lo contrario, la respuesta devolverá HTML si el cuerpo almacenado está en formato HTML o RTF.</span><span class="sxs-lookup"><span data-stu-id="66a20-129">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span><br/><br/> <span data-ttu-id="66a20-130">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="66a20-130">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="66a20-131">HTML</span><span class="sxs-lookup"><span data-stu-id="66a20-131">HTML</span></span>  <br/> |<span data-ttu-id="66a20-132">La respuesta devolverá un cuerpo del elemento como HTML.</span><span class="sxs-lookup"><span data-stu-id="66a20-132">The response will return an item body as HTML.</span></span>  <br/> |
|<span data-ttu-id="66a20-133">Texto</span><span class="sxs-lookup"><span data-stu-id="66a20-133">Text</span></span>  <br/> |<span data-ttu-id="66a20-134">La respuesta devolverá un cuerpo del elemento como texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="66a20-134">The response will return an item body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66a20-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="66a20-135">Remarks</span></span>

<span data-ttu-id="66a20-136">Para identificar el tipo de cuerpo devuelto en la respuesta, compruebe el atributo **BodyType** del elemento [Body](body.md) .</span><span class="sxs-lookup"><span data-stu-id="66a20-136">You can identify the type of body returned in the response by checking the **BodyType** attribute of the [Body](body.md) element.</span></span> <span data-ttu-id="66a20-137">El atributo **BodyType** identificará el cuerpo como HTML o texto.</span><span class="sxs-lookup"><span data-stu-id="66a20-137">The **BodyType** attribute will identify the body as either HTML or text.</span></span> 
  
<span data-ttu-id="66a20-138">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="66a20-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="66a20-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="66a20-139">Example</span></span>

<span data-ttu-id="66a20-140">El siguiente ejemplo de una solicitud muestra dónde se usa un elemento **BodyType** .</span><span class="sxs-lookup"><span data-stu-id="66a20-140">The following example of a request shows where a **BodyType** element is used.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="66a20-141">El atributo ID se ha abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="66a20-141">The Id attribute has been shortened to preserve readability.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66a20-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="66a20-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66a20-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="66a20-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="66a20-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="66a20-144">Schema Name</span></span>  <br/> |<span data-ttu-id="66a20-145">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="66a20-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="66a20-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="66a20-146">Validation File</span></span>  <br/> |<span data-ttu-id="66a20-147">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="66a20-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="66a20-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="66a20-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="66a20-149">Falso</span><span class="sxs-lookup"><span data-stu-id="66a20-149">False</span></span>  <br/> |
   

