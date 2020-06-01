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
description: El elemento FilterHtmlContent especifica si el contenido HTML potencialmente no seguro se filtra desde un elemento o datos adjuntos.
ms.openlocfilehash: 28e3be86b550c3f330fbb6846b64732b5674304d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462678"
---
# <a name="filterhtmlcontent"></a><span data-ttu-id="5e7a9-103">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="5e7a9-103">FilterHtmlContent</span></span>

<span data-ttu-id="5e7a9-104">El elemento **FilterHtmlContent** especifica si el contenido HTML potencialmente no seguro se filtra desde un elemento o datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="5e7a9-104">The **FilterHtmlContent** element specifies whether potentially unsafe HTML content is filtered from an item or attachment.</span></span> 
  
```xml
<FilterHtmlContent>true or false</FilterHtmlContent>
```

 <span data-ttu-id="5e7a9-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="5e7a9-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5e7a9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5e7a9-106">Attributes and elements</span></span>

<span data-ttu-id="5e7a9-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5e7a9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5e7a9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5e7a9-108">Attributes</span></span>

<span data-ttu-id="5e7a9-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5e7a9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5e7a9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5e7a9-110">Child elements</span></span>

<span data-ttu-id="5e7a9-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5e7a9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5e7a9-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5e7a9-112">Parent elements</span></span>

|<span data-ttu-id="5e7a9-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5e7a9-113">**Element**</span></span>|<span data-ttu-id="5e7a9-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5e7a9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5e7a9-115">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="5e7a9-115">AttachmentShape</span></span>](attachmentshape.md) <br/> | <span data-ttu-id="5e7a9-116">Identifica las propiedades adicionales que se van a devolver en una respuesta a una solicitud [GetAttachment](getattachment.md) .</span><span class="sxs-lookup"><span data-stu-id="5e7a9-116">Identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/><br/>  <span data-ttu-id="5e7a9-117">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="5e7a9-117">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/GetAttachment/AttachmentShape` <br/> |
|[<span data-ttu-id="5e7a9-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="5e7a9-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="5e7a9-119">Identifica el contenido y las propiedades de los elementos que se van a incluir en una respuesta GetItem, FindItem o SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="5e7a9-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> <br/> <span data-ttu-id="5e7a9-120">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="5e7a9-120">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetItem/ItemShape`<br/> <br/>  `/FindItem/ItemShape`<br/> <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5e7a9-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5e7a9-121">Text value</span></span>

<span data-ttu-id="5e7a9-122">Este elemento puede ser **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="5e7a9-122">This element can be either **true** or **false**.</span></span> <span data-ttu-id="5e7a9-123">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="5e7a9-123">The default value is **false**.</span></span> <span data-ttu-id="5e7a9-124">Se trata de un tipo de datos Boolean.</span><span class="sxs-lookup"><span data-stu-id="5e7a9-124">This is a Boolean data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5e7a9-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5e7a9-125">Remarks</span></span>

<span data-ttu-id="5e7a9-126">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="5e7a9-126">This element is optional.</span></span>
  
<span data-ttu-id="5e7a9-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con el rol de servidor acceso de clientes instalado.</span><span class="sxs-lookup"><span data-stu-id="5e7a9-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5e7a9-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5e7a9-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5e7a9-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="5e7a9-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5e7a9-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5e7a9-130">Schema Name</span></span>  <br/> |<span data-ttu-id="5e7a9-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5e7a9-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="5e7a9-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5e7a9-132">Validation File</span></span>  <br/> |<span data-ttu-id="5e7a9-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5e7a9-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5e7a9-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5e7a9-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="5e7a9-135">Falso</span><span class="sxs-lookup"><span data-stu-id="5e7a9-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5e7a9-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e7a9-136">See also</span></span>

- [<span data-ttu-id="5e7a9-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5e7a9-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

