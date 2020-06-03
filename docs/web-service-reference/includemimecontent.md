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
ms.openlocfilehash: 6198e4bef2dc59e6e56a8d3cbe463dad13e544e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457196"
---
# <a name="includemimecontent"></a><span data-ttu-id="0374f-103">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="0374f-103">IncludeMimeContent</span></span>

<span data-ttu-id="0374f-104">El elemento **IncludeMimeContent** especifica si se devuelve el contenido de extensiones multipropósito de correo Internet (MIME) de un elemento o datos adjuntos en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0374f-104">The **IncludeMimeContent** element specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item or attachment is returned in the response.</span></span> 
  
```xml
<IncludeMimeContent>true or false</IncludeMimeContent>
```

 <span data-ttu-id="0374f-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="0374f-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0374f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0374f-106">Attributes and elements</span></span>

<span data-ttu-id="0374f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0374f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0374f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0374f-108">Attributes</span></span>

<span data-ttu-id="0374f-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0374f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0374f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0374f-110">Child elements</span></span>

<span data-ttu-id="0374f-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0374f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0374f-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0374f-112">Parent elements</span></span>

|<span data-ttu-id="0374f-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0374f-113">**Element**</span></span>|<span data-ttu-id="0374f-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0374f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0374f-115">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="0374f-115">AttachmentShape</span></span>](attachmentshape.md) <br/> | <span data-ttu-id="0374f-116">Identifica las propiedades adicionales que se van a devolver en una respuesta a una solicitud [GetAttachment](getattachment.md) .</span><span class="sxs-lookup"><span data-stu-id="0374f-116">Identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/> <br/> <span data-ttu-id="0374f-117">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="0374f-117">The following is the XPath expression to this element:</span></span>  <br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
|[<span data-ttu-id="0374f-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="0374f-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="0374f-119">Identifica el contenido y las propiedades de los elementos que se van a incluir en una respuesta GetItem, FindItem o SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="0374f-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> <br/> <span data-ttu-id="0374f-120">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="0374f-120">The following are the XPath expressions to this element:</span></span><br/>  <br/>  `/GetItem/ItemShape` <br/><br/>  `/FindItem/ItemShape` <br/><br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0374f-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0374f-121">Text value</span></span>

<span data-ttu-id="0374f-122">Este elemento puede ser **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="0374f-122">This element can be either **true** or **false**.</span></span> <span data-ttu-id="0374f-123">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="0374f-123">The default value is **false**.</span></span> <span data-ttu-id="0374f-124">Se trata de un tipo de datos Boolean.</span><span class="sxs-lookup"><span data-stu-id="0374f-124">This is a Boolean data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0374f-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0374f-125">Remarks</span></span>

<span data-ttu-id="0374f-126">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="0374f-126">This element is optional.</span></span>
  
<span data-ttu-id="0374f-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="0374f-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="0374f-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0374f-128">Example</span></span>

<span data-ttu-id="0374f-129">El siguiente ejemplo de una solicitud muestra cómo establecer el elemento **IncludeMimeContent** .</span><span class="sxs-lookup"><span data-stu-id="0374f-129">The following example of a request demonstrates a how to set the **IncludeMimeContent** element.</span></span> 
  
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

<span data-ttu-id="0374f-130">El atributo de identificador de datos adjuntos se trunca para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="0374f-130">The attachment Id attribute is truncated to preserve readability.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0374f-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0374f-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0374f-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="0374f-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0374f-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0374f-133">Schema Name</span></span>  <br/> |<span data-ttu-id="0374f-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0374f-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="0374f-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0374f-135">Validation File</span></span>  <br/> |<span data-ttu-id="0374f-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="0374f-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0374f-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0374f-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="0374f-138">Falso</span><span class="sxs-lookup"><span data-stu-id="0374f-138">False</span></span>  <br/> |
   

