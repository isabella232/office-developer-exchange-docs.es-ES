---
title: FailedMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f34fb6f6-057e-4ae3-8e10-bc92112eafba
description: El elemento FailedMailboxes especifica una matriz de buzones de correo con errores en la búsqueda.
ms.openlocfilehash: f68cc29dc9da3b1b74369aa21cde65866e42f3b8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764579"
---
# <a name="failedmailboxes"></a><span data-ttu-id="e3e3b-103">FailedMailboxes</span><span class="sxs-lookup"><span data-stu-id="e3e3b-103">FailedMailboxes</span></span>

<span data-ttu-id="e3e3b-104">El elemento **FailedMailboxes** especifica una matriz de buzones de correo con errores en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e3e3b-104">The **FailedMailboxes** element specifies an array of mailboxes that failed on search.</span></span> 
  
```XML
<FailedMailboxes>
    <FailedMailbox/>
<FailedMailboxes>
```

 <span data-ttu-id="e3e3b-105">**ArrayOfFailedSearchMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="e3e3b-105">**ArrayOfFailedSearchMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3e3b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e3e3b-106">Attributes and elements</span></span>

<span data-ttu-id="e3e3b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e3e3b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3e3b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e3e3b-108">Attributes</span></span>

<span data-ttu-id="e3e3b-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e3e3b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3e3b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e3e3b-110">Child elements</span></span>

|<span data-ttu-id="e3e3b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e3e3b-111">**Element**</span></span>|<span data-ttu-id="e3e3b-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e3e3b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3e3b-113">FailedMailbox</span><span class="sxs-lookup"><span data-stu-id="e3e3b-113">FailedMailbox</span></span>](failedmailbox.md) <br/> |<span data-ttu-id="e3e3b-114">Especifica el mensaje de error para un buzón de correo con errores en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e3e3b-114">Specifies the error message for a mailbox that failed on search.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e3e3b-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e3e3b-115">Parent elements</span></span>

|<span data-ttu-id="e3e3b-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="e3e3b-116">**Element**</span></span>|<span data-ttu-id="e3e3b-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e3e3b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3e3b-118">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="e3e3b-118">SearchMailboxesResult</span></span>](searchmailboxesresult.md) <br/> |<span data-ttu-id="e3e3b-119">Contiene el resultado de la solicitud de **SearchMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="e3e3b-119">Contains the result of the **SearchMailboxes** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3e3b-120">Notas</span><span class="sxs-lookup"><span data-stu-id="e3e3b-120">Remarks</span></span>

<span data-ttu-id="e3e3b-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e3e3b-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e3e3b-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e3e3b-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3e3b-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e3e3b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3e3b-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e3e3b-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e3e3b-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e3e3b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="e3e3b-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="e3e3b-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="e3e3b-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e3e3b-127">Validation File</span></span>  <br/> |<span data-ttu-id="e3e3b-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e3e3b-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="e3e3b-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e3e3b-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e3e3b-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="e3e3b-130">See also</span></span>



- [<span data-ttu-id="e3e3b-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e3e3b-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
