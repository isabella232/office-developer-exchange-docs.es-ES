---
title: FilterHtmlContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FilterHtmlContent
api_type:
- schema
ms.assetid: 2f9358a0-de1d-4544-9aa0-d9f6519f3b5f
description: El elemento FilterHtmlContent especifica si se filtra los potencialmente peligrosas contenido HTML de un elemento o datos adjuntos.
ms.openlocfilehash: db181eff9586061d728a5e4ef55a78f4955b5713
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764601"
---
# <a name="filterhtmlcontent"></a><span data-ttu-id="f11d2-103">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="f11d2-103">FilterHtmlContent</span></span>

<span data-ttu-id="f11d2-104">El elemento **FilterHtmlContent** especifica si se filtra los potencialmente peligrosas contenido HTML de un elemento o datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="f11d2-104">The **FilterHtmlContent** element specifies whether potentially unsafe HTML content is filtered from an item or attachment.</span></span> 
  
```xml
<FilterHtmlContent>true or false</FilterHtmlContent>
```

 <span data-ttu-id="f11d2-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="f11d2-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f11d2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f11d2-106">Attributes and elements</span></span>

<span data-ttu-id="f11d2-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f11d2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f11d2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f11d2-108">Attributes</span></span>

<span data-ttu-id="f11d2-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f11d2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f11d2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f11d2-110">Child elements</span></span>

<span data-ttu-id="f11d2-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f11d2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f11d2-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f11d2-112">Parent elements</span></span>

|<span data-ttu-id="f11d2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f11d2-113">**Element**</span></span>|<span data-ttu-id="f11d2-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f11d2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f11d2-115">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="f11d2-115">AttachmentShape</span></span>](attachmentshape.md) <br/> | <span data-ttu-id="f11d2-116">Identifica las propiedades adicionales para devolver en una respuesta a una solicitud de [GetAttachment](getattachment.md) .</span><span class="sxs-lookup"><span data-stu-id="f11d2-116">Identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/><br/>  <span data-ttu-id="f11d2-117">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="f11d2-117">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/GetAttachment/AttachmentShape` <br/> |
|[<span data-ttu-id="f11d2-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="f11d2-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="f11d2-119">Identifica las propiedades de elemento y el contenido que desea incluir en una respuesta GetItem, FindItem o SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="f11d2-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> <br/> <span data-ttu-id="f11d2-120">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="f11d2-120">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetItem/ItemShape`<br/> <br/>  `/FindItem/ItemShape`<br/> <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f11d2-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f11d2-121">Text value</span></span>

<span data-ttu-id="f11d2-122">Este elemento puede ser **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="f11d2-122">This element can be either **true** or **false**.</span></span> <span data-ttu-id="f11d2-123">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="f11d2-123">The default value is **false**.</span></span> <span data-ttu-id="f11d2-124">Esto es un tipo de datos Boolean.</span><span class="sxs-lookup"><span data-stu-id="f11d2-124">This is a Boolean data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f11d2-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f11d2-125">Remarks</span></span>

<span data-ttu-id="f11d2-126">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="f11d2-126">This element is optional.</span></span>
  
<span data-ttu-id="f11d2-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.</span><span class="sxs-lookup"><span data-stu-id="f11d2-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f11d2-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f11d2-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f11d2-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f11d2-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f11d2-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f11d2-130">Schema Name</span></span>  <br/> |<span data-ttu-id="f11d2-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f11d2-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="f11d2-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f11d2-132">Validation File</span></span>  <br/> |<span data-ttu-id="f11d2-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f11d2-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f11d2-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f11d2-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="f11d2-135">False</span><span class="sxs-lookup"><span data-stu-id="f11d2-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f11d2-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f11d2-136">See also</span></span>

- [<span data-ttu-id="f11d2-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f11d2-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

