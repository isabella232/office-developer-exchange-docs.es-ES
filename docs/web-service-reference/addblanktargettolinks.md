---
title: AddBlankTargetToLinks
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 30180298-2501-4369-9b8f-2f7663f02336
description: El elemento AddBlankTargetToLinks especifica que el atributo de destino en vínculos HTML está configurado para abrir una nueva ventana.
ms.openlocfilehash: 1d4d36c1f4b98ebee96baea683c40527d2a9ec27
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465046"
---
# <a name="addblanktargettolinks"></a><span data-ttu-id="8915a-103">AddBlankTargetToLinks</span><span class="sxs-lookup"><span data-stu-id="8915a-103">AddBlankTargetToLinks</span></span>

<span data-ttu-id="8915a-104">El elemento **AddBlankTargetToLinks** especifica que el atributo de destino en vínculos HTML está configurado para abrir una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="8915a-104">The **AddBlankTargetToLinks** element specifies that the target attribute in HTML links are set to open a new window.</span></span> 
  
```XML
<AddBlankTargetToLinks> true | false </AddBlankTargetToLinks>
```

<span data-ttu-id="8915a-105">**XS: Boolean**</span><span class="sxs-lookup"><span data-stu-id="8915a-105">**xs:Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8915a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8915a-106">Attributes and elements</span></span>

<span data-ttu-id="8915a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8915a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8915a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8915a-108">Attributes</span></span>

<span data-ttu-id="8915a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8915a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8915a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8915a-110">Child elements</span></span>

<span data-ttu-id="8915a-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8915a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8915a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8915a-112">Parent elements</span></span>

|<span data-ttu-id="8915a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8915a-113">**Element**</span></span>|<span data-ttu-id="8915a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8915a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8915a-115">ItemShape</span><span class="sxs-lookup"><span data-stu-id="8915a-115">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="8915a-116">Identifica las propiedades de elemento y el contenido que se incluirá en una respuesta de **GetItem**, **FindItem**, **GetConversationItems** o **SyncFolderItems** .</span><span class="sxs-lookup"><span data-stu-id="8915a-116">Identifies the item properties and content to include in a **GetItem**, **FindItem**, **GetConversationItems** or **SyncFolderItems** response.</span></span><br/><br/>  <span data-ttu-id="8915a-117">Las siguientes son las expresiones XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="8915a-117">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/>  `/GetConversationItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8915a-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8915a-118">Text value</span></span>

<span data-ttu-id="8915a-119">Un valor de texto de **true** para el elemento **AddBlankTargetToLinks** indica que se establecerán todos los vínculos HTML para abrir una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="8915a-119">A text value of **true** for the **AddBlankTargetToLinks** element indicates that all HTML links will be set to open a new window.</span></span> <span data-ttu-id="8915a-120">Un valor de **false** indica que los vínculos HTML se abrirán en la ventana actual.</span><span class="sxs-lookup"><span data-stu-id="8915a-120">A value of **false** indicates that HTML links will open in the current window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8915a-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8915a-121">Remarks</span></span>

<span data-ttu-id="8915a-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="8915a-122">This element is optional.</span></span>
  
<span data-ttu-id="8915a-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8915a-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8915a-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="8915a-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8915a-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8915a-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8915a-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="8915a-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8915a-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8915a-127">Schema Name</span></span>  <br/> |<span data-ttu-id="8915a-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="8915a-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="8915a-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8915a-129">Validation File</span></span>  <br/> |<span data-ttu-id="8915a-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="8915a-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="8915a-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8915a-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="8915a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8915a-132">See also</span></span>

- [<span data-ttu-id="8915a-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8915a-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

