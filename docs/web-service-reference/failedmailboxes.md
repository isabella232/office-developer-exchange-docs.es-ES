---
title: FailedMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f34fb6f6-057e-4ae3-8e10-bc92112eafba
description: El elemento FailedMailboxes especifica una matriz de buzones en los que se produjo un error en la búsqueda.
ms.openlocfilehash: 10f10d3f2ac4379d7ddcb3a13019d17a17bb676a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461957"
---
# <a name="failedmailboxes"></a><span data-ttu-id="577c2-103">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="577c2-103">FailedMailboxes</span></span>

<span data-ttu-id="577c2-104">El elemento **FailedMailboxes** especifica una matriz de buzones en los que se produjo un error en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="577c2-104">The **FailedMailboxes** element specifies an array of mailboxes that failed on search.</span></span> 
  
```XML
<FailedMailboxes>
    <FailedMailbox/>
<FailedMailboxes>
```

 <span data-ttu-id="577c2-105">**ArrayOfFailedSearchMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="577c2-105">**ArrayOfFailedSearchMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="577c2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="577c2-106">Attributes and elements</span></span>

<span data-ttu-id="577c2-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="577c2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="577c2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="577c2-108">Attributes</span></span>

<span data-ttu-id="577c2-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="577c2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="577c2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="577c2-110">Child elements</span></span>

|<span data-ttu-id="577c2-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="577c2-111">**Element**</span></span>|<span data-ttu-id="577c2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="577c2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="577c2-113">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="577c2-113">FailedMailbox</span></span>](failedmailbox.md) <br/> |<span data-ttu-id="577c2-114">Especifica el mensaje de error de un buzón en el que se produjo un error en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="577c2-114">Specifies the error message for a mailbox that failed on search.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="577c2-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="577c2-115">Parent elements</span></span>

|<span data-ttu-id="577c2-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="577c2-116">**Element**</span></span>|<span data-ttu-id="577c2-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="577c2-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="577c2-118">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="577c2-118">SearchMailboxesResult</span></span>](searchmailboxesresult.md) <br/> |<span data-ttu-id="577c2-119">Contiene el resultado de la solicitud **SearchMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="577c2-119">Contains the result of the **SearchMailboxes** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="577c2-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="577c2-120">Remarks</span></span>

<span data-ttu-id="577c2-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="577c2-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="577c2-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="577c2-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="577c2-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="577c2-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="577c2-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="577c2-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="577c2-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="577c2-125">Schema Name</span></span>  <br/> |<span data-ttu-id="577c2-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="577c2-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="577c2-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="577c2-127">Validation File</span></span>  <br/> |<span data-ttu-id="577c2-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="577c2-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="577c2-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="577c2-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="577c2-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="577c2-130">See also</span></span>



- [<span data-ttu-id="577c2-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="577c2-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

