---
title: Guid
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 49dcf69f-bf8d-4be6-a24c-03bbd13f4fe5
description: El elemento Guid especifica el identificador único global del buzón.
ms.openlocfilehash: 35307a706523fc5c2916767c7508dec07deb8d09
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835799"
---
# <a name="guid"></a><span data-ttu-id="f710f-103">Guid</span><span class="sxs-lookup"><span data-stu-id="f710f-103">Guid</span></span>

<span data-ttu-id="f710f-104">El elemento **Guid** especifica el identificador único global del buzón.</span><span class="sxs-lookup"><span data-stu-id="f710f-104">The **Guid** element specifies the globally unique identifier of the mailbox.</span></span> 
  
```XML
<Guid></Guid>
```

 <span data-ttu-id="f710f-105">**GuidType**</span><span class="sxs-lookup"><span data-stu-id="f710f-105">**GuidType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f710f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f710f-106">Attributes and elements</span></span>

<span data-ttu-id="f710f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f710f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f710f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f710f-108">Attributes</span></span>

<span data-ttu-id="f710f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f710f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f710f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f710f-110">Child elements</span></span>

<span data-ttu-id="f710f-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f710f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f710f-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f710f-112">Parent elements</span></span>

|<span data-ttu-id="f710f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f710f-113">**Element**</span></span>|<span data-ttu-id="f710f-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f710f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f710f-115">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="f710f-115">SearchableMailbox</span></span>](searchablemailbox.md) <br/> |<span data-ttu-id="f710f-116">Especifica un buzón de correo devuelto desde una solicitud de **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="f710f-116">Specifies a mailbox returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f710f-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f710f-117">Text value</span></span>

<span data-ttu-id="f710f-118">El valor de texto del elemento **Guid** es un valor GUID que identifica de forma exclusiva un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f710f-118">The text value of the **Guid** element is a GUID value that uniquely identifies a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f710f-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f710f-119">Remarks</span></span>

<span data-ttu-id="f710f-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f710f-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f710f-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f710f-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f710f-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f710f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f710f-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f710f-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f710f-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f710f-124">Schema Name</span></span>  <br/> |<span data-ttu-id="f710f-125">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="f710f-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="f710f-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f710f-126">Validation File</span></span>  <br/> |<span data-ttu-id="f710f-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f710f-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f710f-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f710f-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f710f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f710f-129">See also</span></span>



- [<span data-ttu-id="f710f-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f710f-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

