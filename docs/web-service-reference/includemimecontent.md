---
title: IncludeMimeContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IncludeMimeContent
api_type:
- schema
ms.assetid: 3f3c2300-55cd-41c0-900e-b470b290d52f
description: El elemento IncludeMimeContent especifica si se devuelve el contenido de extensiones multipropósito de correo Internet (MIME) de un elemento o datos adjuntos en la respuesta.
ms.openlocfilehash: ddd6988be93231ac7c574a2e19c9ba4b562c7d0e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835903"
---
# <a name="includemimecontent"></a><span data-ttu-id="25ce0-103">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="25ce0-103">IncludeMimeContent</span></span>

<span data-ttu-id="25ce0-104">El elemento **IncludeMimeContent** especifica si se devuelve el contenido de extensiones multipropósito de correo Internet (MIME) de un elemento o datos adjuntos en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="25ce0-104">The **IncludeMimeContent** element specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item or attachment is returned in the response.</span></span> 
  
```xml
<IncludeMimeContent>true or false</IncludeMimeContent>
```

 <span data-ttu-id="25ce0-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="25ce0-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="25ce0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="25ce0-106">Attributes and elements</span></span>

<span data-ttu-id="25ce0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="25ce0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25ce0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="25ce0-108">Attributes</span></span>

<span data-ttu-id="25ce0-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="25ce0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25ce0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="25ce0-110">Child elements</span></span>

<span data-ttu-id="25ce0-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="25ce0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="25ce0-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="25ce0-112">Parent elements</span></span>

|<span data-ttu-id="25ce0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="25ce0-113">**Element**</span></span>|<span data-ttu-id="25ce0-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="25ce0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25ce0-115">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="25ce0-115">AttachmentShape</span></span>](attachmentshape.md) <br/> | <span data-ttu-id="25ce0-116">Identifica las propiedades adicionales para devolver en una respuesta a una solicitud de [GetAttachment](getattachment.md) .</span><span class="sxs-lookup"><span data-stu-id="25ce0-116">Identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/> <br/> <span data-ttu-id="25ce0-117">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="25ce0-117">The following is the XPath expression to this element:</span></span>  <br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
|[<span data-ttu-id="25ce0-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="25ce0-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="25ce0-119">Identifica las propiedades de elemento y el contenido que desea incluir en una respuesta GetItem, FindItem o SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="25ce0-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> <br/> <span data-ttu-id="25ce0-120">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="25ce0-120">The following are the XPath expressions to this element:</span></span><br/>  <br/>  `/GetItem/ItemShape` <br/><br/>  `/FindItem/ItemShape` <br/><br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="25ce0-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="25ce0-121">Text value</span></span>

<span data-ttu-id="25ce0-122">Este elemento puede ser **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="25ce0-122">This element can be either **true** or **false**.</span></span> <span data-ttu-id="25ce0-123">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="25ce0-123">The default value is **false**.</span></span> <span data-ttu-id="25ce0-124">Esto es un tipo de datos Boolean.</span><span class="sxs-lookup"><span data-stu-id="25ce0-124">This is a Boolean data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="25ce0-125">Notas</span><span class="sxs-lookup"><span data-stu-id="25ce0-125">Remarks</span></span>

<span data-ttu-id="25ce0-126">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="25ce0-126">This element is optional.</span></span>
  
<span data-ttu-id="25ce0-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="25ce0-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="25ce0-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="25ce0-128">Example</span></span>

<span data-ttu-id="25ce0-129">El siguiente ejemplo de una solicitud, muestra un procedimiento para establecer el elemento **IncludeMimeContent** .</span><span class="sxs-lookup"><span data-stu-id="25ce0-129">The following example of a request demonstrates a how to set the **IncludeMimeContent** element.</span></span> 
  
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
        <t:IncludeMimeContent>true</t:IncludeMimeContent>
        <t:BodyType>Best</t:BodyType>
      </AttachmentShape>
      <AttachmentIds>
        <t:AttachmentId Id="ASkAS="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="25ce0-130">El atributo de identificador de datos adjuntos se trunca para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="25ce0-130">The attachment Id attribute is truncated to preserve readability.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="25ce0-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="25ce0-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25ce0-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="25ce0-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="25ce0-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="25ce0-133">Schema Name</span></span>  <br/> |<span data-ttu-id="25ce0-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="25ce0-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="25ce0-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="25ce0-135">Validation File</span></span>  <br/> |<span data-ttu-id="25ce0-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="25ce0-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="25ce0-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="25ce0-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="25ce0-138">False</span><span class="sxs-lookup"><span data-stu-id="25ce0-138">False</span></span>  <br/> |
   

