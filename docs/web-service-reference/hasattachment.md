---
title: HasAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de152be6-fc2f-48bc-a05d-1211935da20a
description: El elemento HasAttachment especifica un valor booleano para indicar si el elemento tiene datos adjuntos.
ms.openlocfilehash: dfe163e0850e835784a43984a34c89f14bfbc59b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835798"
---
# <a name="hasattachment"></a><span data-ttu-id="5efed-103">HasAttachment</span><span class="sxs-lookup"><span data-stu-id="5efed-103">HasAttachment</span></span>

<span data-ttu-id="5efed-104">El elemento **HasAttachment** especifica un valor booleano para indicar si el elemento tiene datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="5efed-104">The **HasAttachment** element specifies a Boolean value to indicate whether the item has attachments.</span></span> 
  
```XML
<HasAttachment> true | false </HasAttachment
```

 <span data-ttu-id="5efed-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="5efed-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5efed-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5efed-106">Attributes and elements</span></span>

<span data-ttu-id="5efed-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5efed-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5efed-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5efed-108">Attributes</span></span>

<span data-ttu-id="5efed-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5efed-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5efed-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5efed-110">Child elements</span></span>

<span data-ttu-id="5efed-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5efed-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5efed-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5efed-112">Parent elements</span></span>

|<span data-ttu-id="5efed-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5efed-113">**Element**</span></span>|<span data-ttu-id="5efed-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5efed-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5efed-115">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="5efed-115">SearchPreviewItem</span></span>](searchpreviewitem.md) <br/> |<span data-ttu-id="5efed-116">Especifica los primeros 256 caracteres de un elemento de buzón de correo para vista previa sin abrir el elemento.</span><span class="sxs-lookup"><span data-stu-id="5efed-116">Specifies the first 256 characters of a mailbox item for preview without opening the item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5efed-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5efed-117">Text value</span></span>

<span data-ttu-id="5efed-118">Un valor de texto de **true** para el elemento **HasAttachment** indica que el elemento tiene datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="5efed-118">A text value of **true** for the **HasAttachment** element indicates that the item has an attachment.</span></span> <span data-ttu-id="5efed-119">Un valor de **false** indica que el elemento no tiene datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="5efed-119">A value of **false** indicates that the item does not have an attachment.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5efed-120">Notas</span><span class="sxs-lookup"><span data-stu-id="5efed-120">Remarks</span></span>

<span data-ttu-id="5efed-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5efed-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5efed-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5efed-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5efed-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5efed-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5efed-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5efed-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5efed-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5efed-125">Schema Name</span></span>  <br/> |<span data-ttu-id="5efed-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="5efed-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="5efed-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5efed-127">Validation File</span></span>  <br/> |<span data-ttu-id="5efed-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5efed-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="5efed-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5efed-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="5efed-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="5efed-130">See also</span></span>



- [<span data-ttu-id="5efed-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="5efed-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

