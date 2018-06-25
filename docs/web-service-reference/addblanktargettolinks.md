---
title: AddBlankTargetToLinks
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 30180298-2501-4369-9b8f-2f7663f02336
description: El elemento AddBlankTargetToLinks especifica que el atributo de destino en los vínculos HTML están configuradas para abrir una nueva ventana.
ms.openlocfilehash: 8a47e44d89bcc84bc0e8b61d45f18ff3182f7870
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763390"
---
# <a name="addblanktargettolinks"></a><span data-ttu-id="76ceb-103">AddBlankTargetToLinks</span><span class="sxs-lookup"><span data-stu-id="76ceb-103">AddBlankTargetToLinks</span></span>

<span data-ttu-id="76ceb-104">El elemento **AddBlankTargetToLinks** especifica que el atributo de destino en los vínculos HTML están configuradas para abrir una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="76ceb-104">The **AddBlankTargetToLinks** element specifies that the target attribute in HTML links are set to open a new window.</span></span> 
  
```XML
<AddBlankTargetToLinks> true | false </AddBlankTargetToLinks>
```

<span data-ttu-id="76ceb-105">**xs: Boolean**</span><span class="sxs-lookup"><span data-stu-id="76ceb-105">**xs:Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="76ceb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="76ceb-106">Attributes and elements</span></span>

<span data-ttu-id="76ceb-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="76ceb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76ceb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="76ceb-108">Attributes</span></span>

<span data-ttu-id="76ceb-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="76ceb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="76ceb-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="76ceb-110">Child elements</span></span>

<span data-ttu-id="76ceb-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="76ceb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="76ceb-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="76ceb-112">Parent elements</span></span>

|<span data-ttu-id="76ceb-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="76ceb-113">**Element**</span></span>|<span data-ttu-id="76ceb-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="76ceb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76ceb-115">ItemShape</span><span class="sxs-lookup"><span data-stu-id="76ceb-115">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="76ceb-116">Identifica las propiedades de elemento y el contenido que desea incluir en un **GetItem**, **FindItem**, **GetConversationItems** o respuesta **SyncFolderItems** .</span><span class="sxs-lookup"><span data-stu-id="76ceb-116">Identifies the item properties and content to include in a **GetItem**, **FindItem**, **GetConversationItems** or **SyncFolderItems** response.</span></span><br/><br/>  <span data-ttu-id="76ceb-117">Los siguientes son las expresiones de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="76ceb-117">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/>  `/GetConversationItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="76ceb-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="76ceb-118">Text value</span></span>

<span data-ttu-id="76ceb-119">Un valor de texto de **true** para el elemento **AddBlankTargetToLinks** indica que todos los vínculos HTML se establecerá para abrir una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="76ceb-119">A text value of **true** for the **AddBlankTargetToLinks** element indicates that all HTML links will be set to open a new window.</span></span> <span data-ttu-id="76ceb-120">Un valor de **false** indica que los vínculos HTML se abrirán en la ventana actual.</span><span class="sxs-lookup"><span data-stu-id="76ceb-120">A value of **false** indicates that HTML links will open in the current window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="76ceb-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="76ceb-121">Remarks</span></span>

<span data-ttu-id="76ceb-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="76ceb-122">This element is optional.</span></span>
  
<span data-ttu-id="76ceb-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="76ceb-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="76ceb-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="76ceb-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="76ceb-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="76ceb-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76ceb-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="76ceb-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="76ceb-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="76ceb-127">Schema Name</span></span>  <br/> |<span data-ttu-id="76ceb-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="76ceb-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="76ceb-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="76ceb-129">Validation File</span></span>  <br/> |<span data-ttu-id="76ceb-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="76ceb-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="76ceb-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="76ceb-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="76ceb-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="76ceb-132">See also</span></span>

- [<span data-ttu-id="76ceb-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="76ceb-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

