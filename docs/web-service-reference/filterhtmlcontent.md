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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462678"
---
# <a name="filterhtmlcontent"></a><span data-ttu-id="65d35-103">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="65d35-103">FilterHtmlContent</span></span>

<span data-ttu-id="65d35-104">El elemento **FilterHtmlContent** especifica si el contenido HTML potencialmente no seguro se filtra desde un elemento o datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="65d35-104">The **FilterHtmlContent** element specifies whether potentially unsafe HTML content is filtered from an item or attachment.</span></span> 
  
```xml
<FilterHtmlContent>true or false</FilterHtmlContent>
```

 <span data-ttu-id="65d35-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="65d35-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="65d35-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="65d35-106">Attributes and elements</span></span>

<span data-ttu-id="65d35-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="65d35-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65d35-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="65d35-108">Attributes</span></span>

<span data-ttu-id="65d35-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="65d35-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="65d35-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="65d35-110">Child elements</span></span>

<span data-ttu-id="65d35-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="65d35-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="65d35-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="65d35-112">Parent elements</span></span>

|<span data-ttu-id="65d35-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="65d35-113">**Element**</span></span>|<span data-ttu-id="65d35-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65d35-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65d35-115">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="65d35-115">AttachmentShape</span></span>](attachmentshape.md) <br/> | <span data-ttu-id="65d35-116">Identifica las propiedades adicionales que se van a devolver en una respuesta a una solicitud [GetAttachment](getattachment.md) .</span><span class="sxs-lookup"><span data-stu-id="65d35-116">Identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/><br/>  <span data-ttu-id="65d35-117">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="65d35-117">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/GetAttachment/AttachmentShape` <br/> |
|[<span data-ttu-id="65d35-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="65d35-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="65d35-119">Identifica el contenido y las propiedades de los elementos que se van a incluir en una respuesta GetItem, FindItem o SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="65d35-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> <br/> <span data-ttu-id="65d35-120">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="65d35-120">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetItem/ItemShape`<br/> <br/>  `/FindItem/ItemShape`<br/> <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="65d35-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="65d35-121">Text value</span></span>

<span data-ttu-id="65d35-122">Este elemento puede ser **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="65d35-122">This element can be either **true** or **false**.</span></span> <span data-ttu-id="65d35-123">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="65d35-123">The default value is **false**.</span></span> <span data-ttu-id="65d35-124">Se trata de un tipo de datos Boolean.</span><span class="sxs-lookup"><span data-stu-id="65d35-124">This is a Boolean data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="65d35-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="65d35-125">Remarks</span></span>

<span data-ttu-id="65d35-126">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="65d35-126">This element is optional.</span></span>
  
<span data-ttu-id="65d35-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con el rol de servidor acceso de clientes instalado.</span><span class="sxs-lookup"><span data-stu-id="65d35-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65d35-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="65d35-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65d35-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="65d35-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="65d35-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="65d35-130">Schema Name</span></span>  <br/> |<span data-ttu-id="65d35-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="65d35-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="65d35-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="65d35-132">Validation File</span></span>  <br/> |<span data-ttu-id="65d35-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="65d35-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="65d35-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="65d35-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="65d35-135">Falso</span><span class="sxs-lookup"><span data-stu-id="65d35-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65d35-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="65d35-136">See also</span></span>

- [<span data-ttu-id="65d35-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="65d35-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

